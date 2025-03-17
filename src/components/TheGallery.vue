<template>
  <div class="container grid grid-cols-[repeat(34,_1fr)] grid-rows-[repeat(4,_150px)] gap-2 grid-flow-row-dense">
    <div v-for="(item, index) in 8" :key="index" class="nth-1:col-span-15 nth-1:row-span-2 nth-2:col-span-5 nth-2:row-span-2 nth-3:col-span-9 nth-3:row-span-4 nth-4:col-span-5 nth-4:row-span-1 nth-5:col-span-12 nth-5:row-span-2 nth-6:col-span-8 nth-6:row-span-2 nth-7:col-span-5 nth-7:row-span-2 nth-8:col-span-5 nth-8:row-span-1">
      <img alt="image" src="@/assets/images/IMG_9408.jpg" width="125" height="125" draggable="false" class="w-full h-full object-cover" />
    </div>
  </div>
</template>
