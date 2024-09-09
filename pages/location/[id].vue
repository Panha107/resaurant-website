<template>
  <div class="">
    <div class="w-full h-[379px]">
      <img class="h-full" src="/assets/images/section.png" alt="" />
    </div>
    <div class="w-full h-[210px]">
      <div class="middle-container flex flex-col gap-3 py-8">
        <span class="text-[32px]">{{ location?.address }}</span>
        <div class="flex gap-3 items-center mt-3">
          <div class="flex gap-2 items-center text-[16px] text-gray-700">
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
            {{ location?.street }}
          </div>
          <NuxtLink
            to="/location"
            class="text-[16px] text-[#379AE6] hover:underline transition-all ease-in-out duration-200"
            >Change Location</NuxtLink
          >
        </div>
        <div class="flex items-center justify-between">
          <div class="flex gap-2 text-[16px] text-gray-700">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="24px"
              fill="#5f6368"
            >
              <path
                d="m612-292 56-56-148-148v-184h-80v216l172 172ZM480-80q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-400Zm0 320q133 0 226.5-93.5T800-480q0-133-93.5-226.5T480-800q-133 0-226.5 93.5T160-480q0 133 93.5 226.5T480-160Z"
              />
            </svg>
            {{ location?.date }} / {{ location?.weekend }}
          </div>
          <div
            class="flex justify-center gap-3 border rounded px-3 py-1 *:text-[14px] *:text-[#765903] border-[#FCDD80]"
          >
            <button to="" class="border-r px-1 pr-3">Delivery</button>
            <button>Pickup</button>
          </div>
        </div>
      </div>
    </div>
    <div class="w-full flex flex-col gap-3 h-[1460px] mt-9">
      <div class="">
        <span class="pl-[7.4rem] text-[24px]">Menu</span>
        <div class="middle-container grid grid-cols-4 gap-4">
          <CardFood
            v-for="(item, index) in Foods.slice(0, 8)"
            :key="index.id"
            :id="item.id"
            :title="item.title"
            :description="item.description"
            :image="item.img"
            :price="item.price"
            :showMore="true"
            :linkOrder="false"
          />
        </div>
      </div>
      <div class="mt-[3.5rem]">
        <span class="pl-[7.4rem] text-[24px]">Drink</span>
        <div class="middle-container grid grid-cols-4 gap-4">
          <CardDrink
            v-for="(item, index) in drinks"
            :key="index"
            :id="item.id"
            :title="item.title"
            :price="item.price" 
            :image="item.img"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { locations } from "../../content/food/datalocation";
import { Foods } from "~/content/food/food";
import CardFood from "~/components/Food/CardFood.vue";
import { drinks } from "~/content/food/food";
import CardDrink from "~/components/Food/CardOfProduct/CardDrink.vue";
const route = useRoute();
const id = route.params.id;
const location = ref();
// watch(
//   () => route.params.id,
//   () => {
//     console.log(id);

//     location.value = locations.find((p) => p.id == id);
//     console.log(location);
//   }
// );
onMounted(() => {
  location.value = locations.find((p) => p.id == id);
  console.log(location);
});
console.log(route);
</script>

<style scoped>
.router-link-exact-active {
  color: #f6a200;
  background-color: #f6a200;
}
</style>
