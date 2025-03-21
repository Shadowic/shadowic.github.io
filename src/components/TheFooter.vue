<script setup lang="ts">
import { ref, useTemplateRef } from 'vue'
import TheLogo from './icons/TheLogo.vue'

const footerLinks = ref([
  {
    title: 'Duis id',
    links: [
      { text: 'augue a ante', link: '/', external: true },
      { text: 'dignissim', link: '/', external: false },
      { text: 'accumsan', link: '/', external: true },
    ]
  },
  {
    title: 'vitae vel nisi',
    links: [
      { text: 'Orci varius', link: '/', external: true },
      { text: 'natoque', link: '/', external: false },
    ]
  },
  {
    title: 'penatibus',
    links: [
      { text: 'et magnis', link: '/', external: true },
      { text: 'dis parturient', link: '/', external: false },
      { text: 'a ante dignissim', link: '/', external: true },
    ]
  },
])

const footerSocials = ref([
  {
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="512" height="512" class="w-full h-full transition-colors"><path d="M14.2,16.261A12.133,12.133,0,0,1,7.747,9.793l3.4-3.406L4.887.122,1.716,3.292A5.9,5.9,0,0,0,0,7.5C0,14.748,9.252,24,16.5,24a5.889,5.889,0,0,0,4.207-1.716l3.171-3.171-6.265-6.265Zm5.092,4.609A3.9,3.9,0,0,1,16.5,22C10.267,22,2,13.733,2,7.5A3.907,3.907,0,0,1,3.13,4.707L4.887,2.95,8.324,6.387,5.389,9.322l.245.614a14.372,14.372,0,0,0,8.447,8.436l.606.231,2.926-2.927,3.437,3.437ZM14,2V0A10.011,10.011,0,0,1,24,10H22A8.009,8.009,0,0,0,14,2Zm0,4V4a6.006,6.006,0,0,1,6,6H18A4,4,0,0,0,14,6Z"/></svg>',
    link: '/',
    external: true
  },
  {
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="512" height="512" class="w-full h-full transition-colors"><path d="M1.444,6.669a2,2,0,0,0-.865,3.337l3.412,3.408V20h6.593l3.435,3.43a1.987,1.987,0,0,0,1.408.588,2.034,2.034,0,0,0,.51-.066,1.978,1.978,0,0,0,1.42-1.379L23.991.021ZM2,8.592l17.028-5.02L5.993,16.586v-4Zm13.44,13.424L11.413,18h-4L20.446,4.978Z"/></svg>',
    link: '/',
    external: true
  },
  {
    icon: '<svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" viewBox="0 0 24 24" width="512" height="512" class="w-full h-full transition-colors"><path style="fill-rule:evenodd;clip-rule:evenodd;" d="M20.463,3.488C18.217,1.24,15.231,0.001,12.05,0    C5.495,0,0.16,5.334,0.157,11.892c-0.001,2.096,0.547,4.142,1.588,5.946L0.057,24l6.304-1.654    c1.737,0.948,3.693,1.447,5.683,1.448h0.005c6.554,0,11.89-5.335,11.893-11.893C23.944,8.724,22.708,5.735,20.463,3.488z     M12.05,21.785h-0.004c-1.774,0-3.513-0.477-5.031-1.378l-0.361-0.214l-3.741,0.981l0.999-3.648l-0.235-0.374    c-0.99-1.574-1.512-3.393-1.511-5.26c0.002-5.45,4.437-9.884,9.889-9.884c2.64,0,5.122,1.03,6.988,2.898    c1.866,1.869,2.893,4.352,2.892,6.993C21.932,17.351,17.498,21.785,12.05,21.785z M17.472,14.382    c-0.297-0.149-1.758-0.868-2.031-0.967c-0.272-0.099-0.47-0.149-0.669,0.148s-0.767,0.967-0.941,1.166    c-0.173,0.198-0.347,0.223-0.644,0.074c-0.297-0.149-1.255-0.462-2.39-1.475c-0.883-0.788-1.48-1.761-1.653-2.059    s-0.018-0.458,0.13-0.606c0.134-0.133,0.297-0.347,0.446-0.521C9.87,9.97,9.919,9.846,10.019,9.647    c0.099-0.198,0.05-0.372-0.025-0.521C9.919,8.978,9.325,7.515,9.078,6.92c-0.241-0.58-0.486-0.501-0.669-0.51    C8.236,6.401,8.038,6.4,7.839,6.4c-0.198,0-0.52,0.074-0.792,0.372c-0.272,0.298-1.04,1.017-1.04,2.479    c0,1.463,1.065,2.876,1.213,3.074c0.148,0.198,2.095,3.2,5.076,4.487c0.709,0.306,1.263,0.489,1.694,0.626    c0.712,0.226,1.36,0.194,1.872,0.118c0.571-0.085,1.758-0.719,2.006-1.413c0.248-0.694,0.248-1.29,0.173-1.413    C17.967,14.605,17.769,14.531,17.472,14.382z"/></svg>',
    link: '/',
    external: true
  },
  {
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="512" height="512" class="w-full h-full transition-colors"><path d="M12,6a4,4,0,1,0,4,4A4,4,0,0,0,12,6Zm0,6a2,2,0,1,1,2-2A2,2,0,0,1,12,12Z"/><path d="M12,24a5.271,5.271,0,0,1-4.311-2.2c-3.811-5.257-5.744-9.209-5.744-11.747a10.055,10.055,0,0,1,20.11,0c0,2.538-1.933,6.49-5.744,11.747A5.271,5.271,0,0,1,12,24ZM12,2.181a7.883,7.883,0,0,0-7.874,7.874c0,2.01,1.893,5.727,5.329,10.466a3.145,3.145,0,0,0,5.09,0c3.436-4.739,5.329-8.456,5.329-10.466A7.883,7.883,0,0,0,12,2.181Z"/></svg>',
    link: '/',
    external: true
  },
])

const footerBottomLinks = ref([
  { text: 'Privacy Policy', link: '/', external: true },
  { text: 'Terms of Use', link: '/', external: true },
  { text: 'Sales and Refunds', link: '/', external: true },
  { text: 'Legal', link: '/', external: true },
  { text: 'Site Map', link: '/', external: true }
])

const linksRefs = useTemplateRef('footerLinks')
const socilasRefs = useTemplateRef('footerSocials')
const privaciesRefs = useTemplateRef('footerBottomLinks')
</script>

<template>
  <div class="bg-[#fdf8ef] py-12 md:py-20 mt-18">
    <div class="custom-container flex flex-col">
      <div class="grid grid-cols-[repeat(auto-fit,_minmax(100px,_1fr))] gap-5 md:[&>*:last-child]:items-end">
        <div v-for="items in footerLinks" :key="items.id" ref="linksRefs">
          <p class="text-base md:text-lg font-bold">{{ items.title }}</p>
          <ul>
            <li v-for="item in items.links" :key="item.id" class="text-sm md:text-base mt-2 hover:text-[#706D54]">
              <a
                :href="item.link"
                :target="item.external ? '_blank' : undefined"
              >
                {{ item.text }}
              </a>
            </li>
          </ul>
        </div>
        <form class="max-sm:col-span-full max-sm:mt-6 max-sm:w-full mx-auto">
          <div class="mb-5">
            <label for="name" class="block mb-2 text-sm font-medium text-gray-900">Your name</label>
            <input type="text" id="name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" required />
          </div>
          <div class="mb-5">
            <label for="email" class="block mb-2 text-sm font-medium text-gray-900">Your email</label>
            <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" placeholder="name@flowbite.com" required />
          </div>
          <div class="flex items-start mb-5">
            <div class="flex items-center h-5">
              <input id="remember" type="checkbox" value="" class="w-4 h-4 border border-gray-300 rounded-sm bg-gray-50 focus:ring-3 focus:ring-[#706D54]" required />
            </div>
            <label for="remember" class="ms-2 text-sm font-medium text-gray-900">Remember me</label>
          </div>
          <button type="submit" class="text-white bg-[#706D54] hover:bg-[#A08963] focus:ring-4 focus:outline-none focus:ring-[#706D54] font-medium rounded-lg text-sm w-full px-4 py-2 text-center transition-colors cursor-pointer">Submit</button>
        </form>
        <div class="flex flex-col mt-6">
          <div class="w-20 overflow-hidden">
            <TheLogo class="w-full h-auto" />
          </div>
          <div class="mt-7">
            <p class="text-base">Follow us</p>
            <ul class="flex gap-7 mt-4">
              <li v-for="item in footerSocials" :key="item.id" ref="socilasRefs" class="flex-none w-5 h-5">
                <a
                  :href="item.link"
                  :target="item.external ? '_blank' : undefined"
                  class="[&>svg]:fill-[#706D54] hover:[&>svg]:fill-[#A08963]"
                  v-html="item.icon"
                >
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="mx-auto mt-12">
        <ul class="flex flex-wrap justify-center gap-4 md:gap-10">
          <li v-for="item in footerBottomLinks" :key="item.id" ref="privaciesRefs" class="text-sm hover:text-[#706D54]">
            <a
              :href="item.link"
              :target="item.external ? '_blank' : undefined"
            >
              {{ item.text }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
