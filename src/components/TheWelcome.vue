<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <WelcomeItem v-for="(item, index) in 5" :key="index">
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Here could be documentation</template>
    but not now
  </WelcomeItem>
</template>
