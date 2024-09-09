<template>
  <div class="w-full h-fit">
    <div class="w-full h-[90%] relative">
      <div class="w-full h-full">
        <img src="/assets/images/Image.png" class="w-full" alt="" />
      </div>
      <div
        class="absolute top-[30%] left-[8%] w-[440px] px-8 py-3 flex flex-col gap-20 rounded-xl shadow-[3px_4px_4px_0px_#00000040] bg-white"
      >
        <span class="text-5xl">ASIAN INSPIRED BOWLS</span>
        <div class="flex flex-col gap-4">
          <span class="text-lg">Fresh, healthy, delicious</span>
          <button class="bg-orange-button w-fit">Order Now</button>
        </div>
      </div>
    </div>
    <div class="w-full flex justify-center py-5">
      <div class="w-[600px] flex flex-col items-center gap-10 py-5">
        <span class="text-5xl font-medium">What's poke</span>
        <p class="text-justify text-lg">
          Poke is a traditional Hawaiian dish that typically consists of diced
          raw fish (such as tuna or salmon) marinated in soy sauce and other
          flavorful ingredients. It is often served over a bed of rice and
          topped with various toppings like seaweed, cucumber, avocado, and
          sesame seeds. Poke has gained popularity worldwide and is now enjoyed
          in many different variations and flavors.
        </p>
      </div>
    </div>
  </div>
  <div class="w-full flex flex-col items-center gap-7 my-4">
    <span class="text-[48px]">Signature Bowls</span>
    <div class="middle-container grid grid-cols-4 gap-4">
      <CardFood
        v-for="(item, index) in Foods.slice(0, 4)"
        :key="index.id"
        :id="item.id"
        :title="item.title"
        :description="item.description"
        :image="item.img"
        :price="item.price"
        :showMore="false"
        :linkOrder="true"
      />
    </div>
    <button class="border-button my-4">Explore more</button>
  </div>
  <div class="w-full">
    <feedbackCustomer />
  </div>
  <div class="w-full">
    <ourLocation />
  </div>
</template>

<script setup>
import { Foods } from "~/content/food/food";
import CardFood from "~/components/Food/CardFood.vue";
import feedbackCustomer from "~/components/customer/feedbackCustomer.vue";
import ourLocation from "~/components/location/ourLocation.vue";
</script>
