<script setup lang="ts">
import TheHero from '../components/TheHero.vue'
import TheAlbum from '../components/TheAlbum.vue'
import TheCitate from '../components/TheCitate.vue'
import TheGallery from '../components/TheGallery.vue'
import TheAbout from '../components/TheAbout.vue'
import TheCaption from '../components/TheCaption.vue'
import BorderBlock from '../components/BorderBlock.vue'
</script>

<template>
  <main>
    <TheHero />
    <TheAlbum />
    <TheCitate />
    <TheGallery />
    <BorderBlock class="mt-12 md:mt-24"/>
    <TheAbout />
    <TheCaption />
  </main>
</template>
