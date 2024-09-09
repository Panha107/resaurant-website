<template>
  <div
    class="w-[267px] h-[296px] flex flex-col items-center shadow-[3px_3px_4px_0px_#928390] rounded-lg mt-[8.25rem] relative"
  >
    <div
      class="w-[219px] h-[219px] justify-center rounded-full overflow-hidden absolute top-[-7.25rem]"
    >
      <img
        class="w-full h-full hover:scale-105 transition-all ease-in-out duration-400"
        :src="image"
        alt=""
      />
    </div>
    <div class="p-4 flex flex-col gap-4 mt-[7rem]">
      <div class="h-[15vh]">
        <span class="text-lg font-medium">{{ title }}</span>
        <p class="text-xs text-gray-600">
          {{ description }}
        </p>
      </div>
      <div class="flex justify-between items-center">
        <span v-if="showMore" class="text-lg">${{ price }}</span>
        <NuxtLink
          v-if="linkOrder"
          class="text-sm p-2 bg-orange-100 text-orange-600 w-fit rounded-full cursor-pointer hover:scale-95 transition-all duration-200 ease-linear"
          >Order Now</NuxtLink
        >
        <NuxtLink
        to="/purchase/orderReview"
          v-if="showMore && !showOrderLink"
          class="text-sm p-2 bg-orange-100 text-orange-600 w-fit rounded-full cursor-pointer hover:scale-95 transition-all duration-200 ease-linear"
          >Add to cart</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<script setup>
// import Footer from "~/components/Footer.vue";
import { ref } from "vue";
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: false,
    default: "",
  },
  image: {
    type: String,
    required: false,
  },
  price: {
    type: Number,
    required: false,
    default: 0,
  },
  showMore: {
    type: Boolean,
    required: false,
    default: false,
  },
  linkOrder: {
    type: Boolean,
    required: false,
    default: false,
  },
});
</script>

<style lang="scss" scoped></style>
