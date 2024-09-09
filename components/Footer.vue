<template>
  <div class="w-ful h-[323px] bg-[#171A1F]">
    <div class="middle-container flex items-center justify-between h-full">
      <!-- right -->
      <div class="flex flex-col gap-10">
        <div class="flex items-center gap-2">
          <img src="/assets/images/logofooter.png" alt="" />
          <h2 class="text-[32px] font-sans font-bold text-white">POKE NOW.</h2>
        </div>
        <ul class="flex gap-7 *:text-base *:text-white pl-6">
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/menu">Menu</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/ourstory">Our story</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/location">Location</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/giftcard">Gift card</NuxtLink>
          </li>
        </ul>
        <div class="flex gap-2 text-sm text-white">
          <span>© 2022 Brand, Inc.</span>
          <span>• Privacy</span>
          <span>• Terms</span>
          <span>• Sitemap</span>
        </div>
      </div>
      <!-- left -->
      <div class="flex flex-col items-end gap-8">
        <div
          class="flex items-center gap-3 text-base *:font-medium cursor-pointer"
        >
          <NuxtLink
            to=""
            class="primary-button border-[#F96540] text-[#F96540]"
          >
            Order Online
          </NuxtLink>
          <NuxtLink to="" class="secondary-button bg-[#F96540] text-white">
            Book a Table
          </NuxtLink>
        </div>
        <div class="flex flex-col gap-1 text-base text-white items-end">
          <span class="">848 King Street, Mesa, AZ 85201, Boston, USA</span>
          <span class="">info@pokebar.com</span>
        </div>
        <div class="flex gap-4 items-center">
          <NuxtLink to="">
            <img src="/assets/images/tweeter.png" alt="" />
          </NuxtLink>
          <NuxtLink to="">
            <img src="/assets/images/fb.png" alt="" />
          </NuxtLink>
          <NuxtLink to="">
            <img src="/assets/images/link.png" alt="" />
          </NuxtLink>
          <NuxtLink to="">
            <img src="/assets/images/youtube.png" alt="" />
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped></style>
