<template>
  <div
    class="w-[368px] h-[517px] rounded-xl shadow-[3px_4px_4px_0px_#00000040]"
  >
    <div class="w-full h-[221px] rounded-t-xl overflow-hidden">
      <img class="h-full overflow-hidden" :src="image" alt="" />
    </div>
    <div class="p-4 flex flex-col gap-[10px]">
      <div class="h-[28vh] flex flex-col gap-[10px]">
        <span class="text-[16px] font-semibold"
          >{{ address }} <span v-if="street">{{ street }}</span></span
        >
        <div class="text-[16] text-gray-700 flex flex-col gap-1">
          <span>{{ date }}</span>
          <span>{{ weekend }}</span>
        </div>
        <div class="flex items-center gap-3">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            height="24px"
            viewBox="0 -960 960 960"
            width="24px"
            fill="#5f6368"
          >
            <path
              d="M798-120q-125 0-247-54.5T329-329Q229-429 174.5-551T120-798q0-18 12-30t30-12h162q14 0 25 9.5t13 22.5l26 140q2 16-1 27t-11 19l-97 98q20 37 47.5 71.5T387-386q31 31 65 57.5t72 48.5l94-94q9-9 23.5-13.5T670-390l138 28q14 4 23 14.5t9 23.5v162q0 18-12 30t-30 12ZM241-600l66-66-17-94h-89q5 41 14 81t26 79Zm358 358q39 17 79.5 27t81.5 13v-88l-94-19-67 67ZM241-600Zm358 358Z"
            />
          </svg>
          <span class="text-[16px] text-[#5f6368]">{{ phone }}</span>
        </div>
        <div class="flex items-center gap-3">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            height="24px"
            viewBox="0 -960 960 960"
            width="24px"
            fill="#5f6368"
          >
            <path
              d="M480-480q33 0 56.5-23.5T560-560q0-33-23.5-56.5T480-640q-33 0-56.5 23.5T400-560q0 33 23.5 56.5T480-480Zm0 294q122-112 181-203.5T720-552q0-109-69.5-178.5T480-800q-101 0-170.5 69.5T240-552q0 71 59 162.5T480-186Zm0 106Q319-217 239.5-334.5T160-552q0-150 96.5-239T480-880q127 0 223.5 89T800-552q0 100-79.5 217.5T480-80Zm0-480Z"
            />
          </svg>
          <span class="text-[16px] text-[#5f6368]">{{ email }}</span>
        </div>
      </div>
      <div class="flex gap-4 items-center my-7">
        <NuxtLink
          :to="'/location/' + id"
          class="border-normal text-red-600 border-red-700 hover:text-red-900 hover:bg-red-100 transition-all ease-in-out duration-300"
          >Delivery</NuxtLink
        >
        <NuxtLink
          class="border-normal text-[#765903] border-[#765903] hover:text-[#695b31] hover:bg-[#f7eed2] transition-all ease-in-out duration-300"
          >Pickup</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
defineProps({
  id: {
    type: Number,
    required: true,
  },
  image: {
    type: String,
    required: true,
    default: "",
  },
  address: {
    type: String,
    required: false,
    default: "",
  },
  street: {
    type: String,
    required: false,
    default: "",
  },
  date: {
    type: String,
    required: false,
    default: "",
  },
  weekend: {
    type: String,
    required: false,
    default: "",
  },
  phone: {
    type: String,
    required: true,
    default: "",
  },
  email: {
    type: String,
    required: true,
    default: "",
  },
});
</script>

<style lang="scss" scoped></style>
