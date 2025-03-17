<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-10 flex justify-between items-center">

    <div class="flex">
      <img alt="logo" class="logo" src="@/assets/IMG_9542.jpg" width="125" height="125" />
      <HelloWorld msg="Hello world" />
    </div>

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/history">History</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
    </nav>

    <div>
      2025
    </div>

  </header>

  <transition name="fade" mode="out-in">
    <RouterView />
  </transition>

  <footer>
    <TheFooter />
  </footer>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>

<style scoped>
nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
</style>
