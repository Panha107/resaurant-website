<template>
  <teleport to="body">
    <div
      v-if="isVisible"
      class="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50"
    >
      <div class="w-[1039px] h-[624px] rounded-lg overflow-hidden bg-white">
        <div class="grid grid-cols-[52%_45%] gap-[2.25rem]">
          <div class="p-5 flex flex-col gap-7 justify-center">
            <span class="text-[32px] font-bold">Reservation</span>
            <p class="text-[16px] text-[#323842]">
              We provide a convenient online reservation system. Simply select
              your desired date, time, and party size, and we will make sure
              that your table is ready upon your arrivals
            </p>
            <div class="*:text-[16px] flex flex-col">
              <label for="" class="font-semibold">Your name</label>
              <input
                type="text"
                placeholder="your name"
                class="py-2 pl-4 rounded-md border"
              />
            </div>
            <div class="flex gap-4">
              <div class="*:text-[16px] flex flex-col w-full">
                <label for="" class="font-semibold">Guests</label>
                <input
                  type="text"
                  class="py-2 pl-4 rounded-md border"
                  placeholder="Number of guest"
                />
              </div>
              <div class="*:text-[16px] flex flex-col w-full">
                <label for="" class="font-semibold">Restaurant</label>
                <input
                  type="text"
                  class="py-2 pl-4 rounded-md border"
                  placeholder="Your favorite place?"
                />
              </div>
            </div>
            <div class="flex gap-4">
              <div class="*:text-[16px] flex flex-col w-full">
                <label for="" class="font-semibold">Date</label>
                <input
                  type="text"
                  class="py-2 pl-4 rounded-md border"
                  placeholder="Fri 25, Sep"
                />
              </div>
              <div class="*:text-[16px] flex flex-col w-full">
                <label for="" class="font-semibold">Time</label>
                <input
                  type="text"
                  class="py-2 pl-4 rounded-md border"
                  placeholder="6:00 PM"
                />
              </div>
            </div>
            <button
              class="w-full py-2 bg-orange-600 text-white rounded-full hover:bg-black transition-all ease-in-out duration-300"
            >
              Book a table
            </button>
          </div>
          <div class="w-full h-[624px] relative">
            <img class="h-full overflow-hidden" :src="img" alt="" />
            <button
              @click="close"
              class="bg-orange-200 p-1 rounded-full hover:scale-110 transition-all ease-in-out duration-200 absolute top-[1.5rem] right-[2.25rem]"
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
        </div>
      </div>
    </div>
  </teleport>
</template>

<script setup>
const img =
  "https://s3-alpha-sig.figma.com/img/6337/1ccf/6332c59dbcd77bf72cbeb50bbc6eeaf8?Expires=1726444800&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=RFrk8-qF6I-1OPL1lAl5Xi6TzUhogEXclGJUEiES7lD4uV98JUqbcmbAIVxPkq82hqqYNDuNHUi6iooQ4cx7kjirHWq8w6Yf6IqpNmH2D~3WC3YuVjIRlmKY4pNUH6sCzQcz31fLGzv7WpnvAI4DNqNnFcfEGSLR~~aFynihhzF5QvKL2jH8gUEDCeOHtVd6sbIkASGiCTgE0q-5LFiS6y9D61LCOYw~NNIGOEm-y6~Lz2H3ItIVXr0OfWleB1c35KC32oXUPwbdnEAs~0QqUMsn0WUeLkqPzwq9mVYMksig-ptaZkseqQVJgM19n7xE0FFy~yzell0FVZwGFbYtww__";

import { defineProps, defineEmits } from "vue";
const props = defineProps({
  isVisible: Boolean,
});

const emits = defineEmits(["close"]);

function close() {
  emits("close");
}
</script>

<style lang="scss" scoped></style>
