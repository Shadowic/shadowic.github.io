<template>
  <div class="bg-[#fdf8ef] py-20 mt-18">
    <div class="custom-container flex flex-col">
      <div class="grid grid-cols-[repeat(auto-fit,_minmax(150px,_1fr))] gap-5 [&>*:last-child]:items-end">
        <ul>
          <p class="font-bold">Duis id</p>
          <li>augue a ante</li>
          <li>dignissim</li>
          <li>accumsan</li>
        </ul>
        <ul>
          <p class="font-bold">vitae vel nisi</p>
          <li>Orci varius</li>
          <li>natoque</li>
        </ul>
        <ul>
          <p class="font-bold">penatibus</p>
          <li>et magnis</li>
          <li>dis parturient</li>
          <li>a ante dignissim</li>
        </ul>
        <form class="max-w-sm mx-auto">
          <div class="mb-5">
            <label for="name" class="block mb-2 text-sm font-medium text-gray-900">Your name</label>
            <input type="text" id="name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" required />
          </div>
          <div class="mb-5">
            <label for="email" class="block mb-2 text-sm font-medium text-gray-900">Your email</label>
            <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="name@flowbite.com" required />
          </div>
          <div class="flex items-start mb-5">
            <div class="flex items-center h-5">
              <input id="remember" type="checkbox" value="" class="w-4 h-4 border border-gray-300 rounded-sm bg-gray-50 focus:ring-3 focus:ring-blue-300" required />
            </div>
            <label for="remember" class="ms-2 text-sm font-medium text-gray-900">Remember me</label>
          </div>
          <button type="submit" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center">Submit</button>
        </form>
        <div class="flex flex-col">
          <div class="w-10 h-10 rounded-xl overflow-hidden">
            <img alt="image" src="@/assets/images/IMG_9408.jpg" width="125" height="125" draggable="false" class="w-full h-full object-cover" />
          </div>
          <div>
            <p>Follow us</p>
            <ul class="flex">
              <li>
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M22 2L11 13" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M22 2L15 22L11 13L2 9L22 2Z" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </li>
              <li>
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M22 2L11 13" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M22 2L15 22L11 13L2 9L22 2Z" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </li>
              <li>
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M22 2L11 13" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M22 2L15 22L11 13L2 9L22 2Z" stroke="#614F44" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="mx-auto mt-12">
        <ul class="flex flex-wrap gap-10">
          <li>
            <a href="/">Privacy Policy</a>
          </li>
          <li>
            <a href="/">Terms of Use</a>
          </li>
          <li>
            <a href="/">Sales and Refunds</a>
          </li>
          <li>
            <a href="/">Legal</a>
          </li>
          <li>
            <a href="/">Site Map</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
