<script setup lang="ts">
import { ref } from 'vue'

const galleryImgs = ref([
  '/images/IMG_9408.jpg', '/images/IMG_9484.jpg', '/images/IMG_9542.jpg', '/images/IMG_9408.jpg', '/images/IMG_9542.jpg', '/images/IMG_9484.jpg', '/images/IMG_9484.jpg', '/images/IMG_9408.jpg'
])

const galleryItems = ref<(HTMLElement | null)[]>([])
const dialogElem = ref<HTMLDialogElement | null>(null)
const currentImageSrc = ref('')

const disableScroll = () => {
  document.body.style.overflow = 'hidden'
}

const enableScroll = () => {
  document.body.style.overflow = ''
}

const setItemRef = (el: unknown, index: number) => {
  galleryItems.value[index] = el as HTMLElement | null
}

const handleClick = (index: number) => {
  const clickedImg = galleryItems.value[index]?.querySelector('img')
  if (clickedImg) {
    currentImageSrc.value = clickedImg.src
    dialogElem.value?.showModal()
    disableScroll()
  }
}

const closeDialog = (e?: MouseEvent) => {
  if (!e || e.target === dialogElem.value) {
    dialogElem.value?.close()
    enableScroll()
  }
}
</script>

<template>
  <section class="custom-container scroll-mt-16 md:scroll-mt-20">
    <div class="custom-gallery">
      <div
        v-for="(item, i) in galleryImgs"
        :key="i"
        :ref="(el) => setItemRef(el, i)"
        @click="handleClick(i)"
        class="custom-gallery-item"
      >
        <img alt="image" :src="item" width="125" height="125" draggable="false" class="w-full h-full object-cover" />
      </div>
    </div>
    <dialog
      ref="dialogElem"
      class="opacity-0 transition-opacity duration-300 m-auto open:opacity-100"
      @click="closeDialog"
    >
      <button
        class="group fixed top-4 right-4 md:top-10 md:right-10 w-4 h-4 md:w-8 md:h-8 p-1 outline-0 cursor-pointer"
        aria-label="Закрыть"
        @click="closeDialog()"
      >
       <span class="block absolute inset-0 m-auto w-full h-0.5 transition-colors bg-[#fbfbfb] group-hover:bg-[#c8c8c8] rounded-2xl rotate-45"></span>
       <span class="block absolute inset-0 m-auto w-full h-0.5 transition-colors bg-[#fbfbfb] group-hover:bg-[#c8c8c8] rounded-2xl -rotate-45"></span>
      </button>
      <img
        :src="currentImageSrc"
        alt="Увеличенное изображение"
        class="w-full h-auto max-w-[80vw] max-h-[80vh] object-contain"
        loading="lazy"
      />
    </dialog>
  </section>
</template>
