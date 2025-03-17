<template>
  <div class="group flex flex-col md:flex-row md:even:flex-row-reverse justify-center items-center">
    <div class="w-full aspect-[4/3] md:w-[500px] md:h-[500px] md:rounded-4xl overflow-hidden flex-none">
      <slot name="image"></slot>
    </div>
    <div class="flex flex-col justify-center md:max-w-1/2 bg-[#fdf8ef;] px-4 py-8 md:p-10 md:group-odd:-ml-12 md:group-even:-mr-12 z-5 md:rounded-2xl">
      <h3 class="text-lg md:text-3xl uppercase">
        <slot name="heading"></slot>
      </h3>
      <p class="text-base md:text-lg mt-4">
        <slot name="description"></slot>
      </p>
    </div>
  </div>
</template>
