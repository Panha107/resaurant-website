<template>
  <div
    class="w-[267px] h-[230px] flex flex-col items-center shadow-[3px_3px_4px_0px_#928390] rounded-lg mt-[8.25rem] relative"
  >
    <div
      class="w-[219px] h-[219px] justify-center rounded-full overflow-hidden absolute top-[-7.25rem]"
    >
      <img
        class="w-full h-full hover:scale-105 transition-all ease-in-out duration-400"
        :src="image"
        :alt="title"
      />
    </div>
    <div class="w-full p-4 flex flex-col gap-4 mt-[7rem]">
      <span class="text-lg font-medium">{{ title }}</span>
      <div class="flex justify-between items-center">
        <div class="text-lg">${{ price }}</div>
        <NuxtLink
          class="text-sm p-2 bg-orange-100 text-orange-600 w-fit rounded-full cursor-pointer hover:scale-95 transition-all duration-200 ease-linear"
          >Add to cart</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  id: {
    type: Number,
    Required: true,
  },
  title: {
    type: String,
    Required: true,
    default: "",
  },
  price: {
    type: Number,
    Required: true,
  },
  image: {
    type: String,
    Required: false,
    default: "",
  },
});
</script>
