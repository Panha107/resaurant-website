<template>
  <div
    class="w-[267px] h-[192px] rounded-lg flex justify-center shadow-lg shadow-gray-500 relative mt-[8.25rem]"
  >
    <div
      class="w-[206px] h-[206px] rounded-full overflow-hidden absolute top-[-6.25rem]"
    >
      <img
        class="w-full h-full hover:scale-110 transition-all duration-300 ease-in-out"
        :src="img"
        alt=""
      />
    </div>
    <div class="mt-[8.5rem]">
      <span class="text-[18px]">{{ title }}</span>
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
    Required: false,
    default: "",
  },
  img: {
    type: String,
    Required: false,
    default: "",
  },
});
</script>

<style lang="scss" scoped></style>
