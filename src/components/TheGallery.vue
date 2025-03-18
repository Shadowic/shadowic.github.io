<template>
  <section class="custom-container">
    <div class="custom-gallery">
      <div v-for="(item, index) in 8" :key="index" class="custom-gallery-item">
        <img alt="image" src="@/assets/images/IMG_9408.jpg" width="125" height="125" draggable="false" class="w-full h-full object-cover" />
      </div>
    </div>
  </section>
</template>
