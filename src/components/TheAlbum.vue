<script setup lang="ts">
import AlbumItem from './AlbumItem.vue'
</script>

<template>
  <section class="max-md:px-0 custom-container scroll-mt-16 md:scroll-mt-20">
    <div class="flex flex-col gap-y-8 md:gap-y-24">
      <AlbumItem v-for="(item, index) in 3" :key="index">
        <template #image>
          <img alt="image" src="@/assets/images/IMG_9408.jpg" width="125" height="125" draggable="false" class="w-full h-full object-cover" />
        </template>
        <template #heading>Maecenas est nisl</template>
        <template #description>Duis id augue a ante dignissim accumsan vitae vel nisi. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</template>
      </AlbumItem>
    </div>
  </section>
</template>
