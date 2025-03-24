<script setup lang="ts">
import TheHero from '../components/TheHero.vue'
import TheAlbum from '../components/TheAlbum.vue'
import TheCitate from '../components/TheCitate.vue'
import TheGallery from '../components/TheGallery.vue'
import TheAbout from '../components/TheAbout.vue'
import TheContacts from '../components/TheContacts.vue'
import BorderBlock from '../components/BorderBlock.vue'
</script>

<template>
  <main>
    <TheHero id="hero" />
    <TheAlbum id="history" />
    <TheCitate />
    <TheGallery id="gallery" />
    <BorderBlock class="mt-12 md:mt-24"/>
    <TheAbout id="about" />
    <TheContacts id="contacts" />
  </main>
</template>
