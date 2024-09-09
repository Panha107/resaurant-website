<template>
  <div class="w-full h-[11vh] bg-white border-b-[0.5px]">
    <div class="middle-container flex items-center justify-between h-full">
      <div class="flex items-center gap-2">
        <img src="/assets/images/logo.png" alt="logo" />
        <h2 class="text-lg font-sans font-bold">POKE NOW.</h2>
      </div>
      <div class="w-[65%] flex justify-between items-center">
        <ul class="flex gap-7 *:text-base cursor-pointer">
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/menu">Menu</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/ourStory">Our story</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/Location">Location</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/giftCard">Gift card</NuxtLink>
          </li>
        </ul>
        <div
          class="flex items-center gap-3 text-base *:font-medium cursor-pointer"
        >
          <button class="primary-button" @click="openLogin">
            Order Online
          </button>
          <button
            @click="openBooking"
            class="secondary-button bg-black text-white"
          >
            Book a Table
          </button>
        </div>
      </div>
    </div>
    <Login :isVisible="showLogin" @close="showLogin = false" />
    <Booking :isVisible="showBooking" @close="showBooking = false" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import Login from "~/pages/Login.vue";

const showLogin = ref(false);
function openLogin() {
  showLogin.value = true;
}

const showBooking = ref(false);
function openBooking() {
  showBooking.value = true;
}
</script>
<style>
.router-link-exact-active {
  color: #f6a200;
}
</style>
