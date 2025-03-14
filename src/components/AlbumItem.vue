<template>
  <div class="group flex even:flex-row-reverse justify-center items-center">
    <div class="w-[500px] h-[500px] rounded-4xl overflow-hidden flex-none">
      <slot name="image"></slot>
    </div>
    <div class="flex flex-col justify-center max-w-1/2 bg-[#fdf8ef;] p-10 group-odd:-ml-12 group-even:-mr-12 z-5 rounded-2xl">
      <h3 class="text-3xl uppercase">
        <slot name="heading"></slot>
      </h3>
      <p class="text-lg">
        <slot name="description"></slot>
      </p>
    </div>
  </div>
</template>
