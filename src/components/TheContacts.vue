<template>
  <section class="custom-container grid grid-cols-1 md:grid-cols-2 gap-10">
    <div>
      <h2 class="text-lg md:text-3xl text-center">
        Class aptent taciti sociosqu
      </h2>
      <p class="text-base md:text-lg text-center mt-4">
        Maecenas id rhoncus velit. Nulla viverra urna eget ipsum cursus, sed interdum nisl facilisis. Etiam porttitor orci leo, ut commodo justo efficitur sed. Aliquam erat volutpat. Aenean mi sapien, luctus varius viverra sed, mollis ac magna.
      </p>
    </div>
    <form class="grid grid-cols-1 sm:grid-cols-2 gap-5">
      <div>
        <label for="first-name" class="block mb-2 text-sm font-medium text-gray-900">First name</label>
        <input type="text" id="first-name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" required />
      </div>
      <div>
        <label for="last-name" class="block mb-2 text-sm font-medium text-gray-900">Last name</label>
        <input type="text" id="last-name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" required />
      </div>
      <div class="sm:col-span-full">
        <label for="email" class="block mb-2 text-sm font-medium text-gray-900">Your email</label>
        <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" placeholder="name@flowbite.com" required />
      </div>
      <div class="sm:col-span-full">
        <label for="comment-area" class="block mb-2 text-sm font-medium text-gray-900">Your comment</label>
        <textarea id="comment-area" name="comment-area" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-[#706D54] focus:border-[#706D54] block w-full p-2.5 outline-[#706D54]" required />
      </div>
      <div class="sm:col-span-full flex items-start">
        <div class="flex items-center h-5">
          <input id="remember" type="checkbox" value="" class="w-4 h-4 border border-gray-300 rounded-sm bg-gray-50 focus:ring-3 focus:ring-[#706D54]" required />
        </div>
        <label for="remember" class="ms-2 text-sm font-medium text-gray-900">Remember me</label>
      </div>
      <button type="submit" class="sm:col-span-full justify-self-center sm:w-fit text-white bg-[#706D54] hover:bg-[#A08963] focus:ring-4 focus:outline-none focus:ring-[#706D54] font-medium rounded-lg text-sm max-sm:w-full px-4 sm:px-12 py-2 text-center transition-colors cursor-pointer">Submit</button>
    </form>
  </section>
</template>
