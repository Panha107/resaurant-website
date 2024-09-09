<template>
  <teleport to="body">
    <div
      v-if="isVisible"
      class="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50"
    >
      <div
        class="w-[1090px] h-[600px] bg-white rounded-xl shadow-lg shadow-gray-400"
      >
        <div class="w-full grid grid-cols-[40%_56%] gap-[1.75rem]">
          <div class="h-[600px] rounded-l-xl overflow-hidden">
            <img
              class="h-full object-cover"
              src="/assets/images/login.png"
              alt=""
            />
          </div>
          <div class="p-3">
            <div class="flex items-center justify-between">
              <span class="text-[32px] font-medium">Login</span>
              <button
                class="bg-orange-200 p-1 rounded-full hover:scale-110 transition-all ease-in-out duration-200"
                @click="close"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  height="24px"
                  viewBox="0 -960 960 960"
                  width="24px"
                  fill="#5f6368"
                >
                  <path
                    d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"
                  />
                </svg>
              </button>
            </div>
            <div class="flex flex-col gap-[2.25rem] pt-[3.25rem]">
              <div class="flex flex-col gap-3">
                <p class="text-[20px]">Enter your email to log in.</p>
                <input
                  class="py-2 pl-5 rounded-full bg-gray-100 focus:outline-none"
                  type="text"
                  placeholder="Enter your email"
                />
              </div>
              <button
                class="py-2 text-[16px] text-white rounded-full bg-orange-700 cursor-pointer hover:bg-orange-500 transition-all ease-in-out duration-200"
              >
                Continue
              </button>
            </div>
            <div class="mt-[3rem] flex flex-col gap-5">
              <div class="flex items-center justify-center">
                <div class="flex-1 h-px bg-gray-300"></div>
                <span class="px-4 text-gray-500 font-medium">OR</span>
                <div class="flex-1 h-px bg-gray-300"></div>
              </div>
              <p class="text-[14px] text-gray-400">
                By continuing, you agree to the updated Terms of Sale, Terms of
                Service, and Privacy Policy.
              </p>
              <div class="flex flex-col gap-3 cursor-pointer pt-6">
                <NuxtLink
                  to=""
                  class="flex gap-3 items-center justify-center py-2 rounded-full bg-gray-100 hover:bg-gray-400 transition-all ease-in-out duration-200"
                >
                  <img class="w-4 h-4" src="/assets/images/google.png" alt="" />
                  Continue with Google
                </NuxtLink>
                <NuxtLink
                  to=""
                  class="flex gap-3 items-center justify-center py-2 rounded-full bg-gray-100 hover:bg-gray-400 transition-all ease-in-out duration-200"
                >
                  <img class="w-4 h-4" src="/assets/images/social.png" alt="" />
                  Continue with Facebook
                </NuxtLink>
                <NuxtLink
                  to=""
                  class="flex gap-3 items-center justify-center py-2 rounded-full bg-gray-100 hover:bg-gray-400 transition-all ease-in-out duration-200"
                >
                  <img class="w-4 h-4" src="/assets/images/apple.png" alt="" />
                  Continue with Apple
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </teleport>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps({
  isVisible: Boolean,
});

const emit = defineEmits(["close"]);

function close() {
  emit("close");
}
</script>

<style lang="scss" scoped></style>
