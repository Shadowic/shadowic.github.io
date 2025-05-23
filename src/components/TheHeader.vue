<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
// import { RouterLink } from 'vue-router'
import TheLogo from './icons/TheLogo.vue'

const headerLinks = ref([
  { text: 'Home', link: '#hero' },
  { text: 'History', link: '#history' },
  { text: 'Gallery', link: '#gallery' },
  { text: 'About', link: '#about' },
  { text: 'Contacts', link: '#contacts' },
])

const headerRef = ref<HTMLElement | null>(null)
const toggleButtonRef = ref<HTMLElement | null>(null)
const isMenuOpened = ref(false)

const isMobile = ref(false)
const checkScreenWidth = () => {
  isMobile.value = window.innerWidth < 768
}

const toggleBodyScroll = (enable: boolean) => {
  document.body.style.overflow = enable ? '' : 'hidden'
}

const toggleMenu = () => {
  isMenuOpened.value = !isMenuOpened.value
  headerRef.value?.classList.toggle('mobile-menu-opened')
  toggleBodyScroll(!isMenuOpened.value)
}

const closeMenu = () => {
  if (isMenuOpened.value) {
    isMenuOpened.value = false
    headerRef.value?.classList.remove('mobile-menu-opened')
    toggleBodyScroll(true)
  }
}

onMounted(() => {
  checkScreenWidth()
  window.addEventListener('resize', checkScreenWidth)
})

onUnmounted(() => {
  window.removeEventListener('resize', checkScreenWidth)
  toggleBodyScroll(true)
})
</script>

<template>
  <header
    ref="headerRef"
    class="group fixed top-0 right-0 left-0 z-10 backdrop-blur-lg"
  >
    <div class="custom-container flex justify-between items-center py-3 md:py-2">

      <div class="flex justify-center items-center h-6 md:h-12 w-auto max-w-24 relative z-1">
        <TheLogo class="w-full h-full" />
      </div>

      <!--      <nav>-->
      <!--        <RouterLink to="/">Home</RouterLink>-->
      <!--        <RouterLink to="/history">History</RouterLink>-->
      <!--        <RouterLink to="/about">About</RouterLink>-->
      <!--        <RouterLink to="/contact">Contact</RouterLink>-->
      <!--      </nav>-->
      <div class="max-sm:fixed top-0 left-0 w-full h-auto max-sm:max-h-[0] group-[.mobile-menu-opened]:max-h-[9999px] transition-all overflow-hidden">
        <nav class="flex justify-center items-center max-sm:h-[100vh] max-sm:h-[100svh] max-sm:bg-[#fafafa;]">
          <ul class="flex max-sm:flex-col gap-10">
            <li v-for="(item, id) in headerLinks" :key="id" class="transition-colors text-base text-[#706D54] hover:text-[#A08963]">
              <a :href="item.link" @click="closeMenu">{{ item.text }}</a>
            </li>
          </ul>
        </nav>
      </div>

      <span class="hidden sm:block text-base md:text-lg text-[#706D54]">
        2025
      </span>

      <div
        ref="toggleButtonRef"
        @click="toggleMenu"
        class="flex sm:hidden justify-center items-center p-2 relative z-1"
      >
        <div
          class="w-5 h-px bg-[#706D54] rounded-full transition-all before:content-[''] before:absolute before:w-5 before:h-px before:bg-[#706D54] before:rounded-full before:-translate-y-1.5 before:transition-all after:content-[''] after:absolute after:w-5 after:h-px after:bg-[#706D54] after:rounded-full after:translate-y-1.5 after:transition-all group-[.mobile-menu-opened]:h-0 group-[.mobile-menu-opened]:bg-transparent group-[.mobile-menu-opened]:before:translate-y-0 group-[.mobile-menu-opened]:before:rotate-45 group-[.mobile-menu-opened]:after:translate-y-0 group-[.mobile-menu-opened]:after:-rotate-45"
        ></div>
      </div>
    </div>
  </header>
</template>
