<script setup lang="ts">
import BorderBlock from '../components/BorderBlock.vue'
</script>

<template>
  <section class="custom-container">
    <BorderBlock />
    <blockquote class="mt-12">
      <p class="text-lg md:text-xl text-center">
        "Duis id augue a ante dignissim accumsan vitae vel nisi. Orci varius natoque penatibus et magnis dis parturient".
      </p>
    </blockquote>
    <p class="text-xl md:text-2xl text-center mt-2">—Maecenas <cite>est nisl</cite></p>
    <BorderBlock class="mt-12" />
  </section>
</template>
