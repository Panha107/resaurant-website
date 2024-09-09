<template>
  <div class="">
    <div class="w-full h-[379px]">
      <img class="h-full" src="/assets/images/sectionMenu.png" alt="" />
    </div>
    <div
      class="w-full h-[1087px] flex flex-col items-center gap-7 my-[2.75rem]"
    >
      <span class="text-[52px]">Menu</span>
      <div class="middle-container grid grid-cols-4 gap-4">
        <CardFood
          v-for="(item, index) in Foods.slice(0, 8)"
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
      <button class="border-button my-4">See All</button>
    </div>
    <div class="w-full h-[3090px] flex flex-col items-center my-4">
      <span class="text-[52px]">Build your own bowl</span>
      <div class="middle-container my-9 flex flex-col gap-4">
        <div class="">
          <div class="flex items-center gap-3 mb-2">
            <span class="text-[80px] text-[#f1c2b6]">1</span>
            <div class="flex flex-col justify-center">
              <span class="text-[16px] text-[#565E6C]">Step 1</span>
              <span class="text-[24px] font-[700]">Choose a Base</span>
            </div>
          </div>
          <div class="grid grid-cols-4 gap-4">
            <CardBase
              v-for="(item, index) in bases"
              :key="index.id"
              :id="item.id"
              :title="item.title"
              :img="item.img"
            />
          </div>
        </div>
        <div class="my-[5rem]">
          <div class="flex items-center gap-3 mb-2">
            <span class="text-[80px] text-[#f1c2b6]">2</span>
            <div class="flex flex-col justify-center">
              <span class="text-[16px] text-[#565E6C]">Step 2</span>
              <span class="text-[24px] font-[700]">Pick Your Protein</span>
            </div>
          </div>
          <div class="grid grid-cols-4 gap-4">
            <CardBase
              v-for="(item, index) in proteins"
              :key="index.id"
              :id="item.id"
              :title="item.title"
              :img="item.img"
            />
          </div>
        </div>
        <div class="mb-[5rem]">
          <div class="flex items-center gap-3 mb-2">
            <span class="text-[80px] text-[#f1c2b6]">3</span>
            <div class="flex flex-col justify-center">
              <span class="text-[16px] text-[#565E6C]">Step 3</span>
              <span class="text-[24px] font-[700]">Choose Your Mix-Ins</span>
            </div>
          </div>
          <div class="grid grid-cols-4 gap-4">
            <CardBase
              v-for="(item, index) in vegetables"
              :key="index.id"
              :id="item.id"
              :title="item.title"
              :img="item.img"
            />
          </div>
        </div>
        <div class="mb-[2rem]">
          <div class="flex items-center gap-3 mb-2">
            <span class="text-[80px] text-[#f1c2b6]">4</span>
            <div class="flex flex-col justify-center">
              <span class="text-[16px] text-[#565E6C]">Step 4</span>
              <span class="text-[24px] font-[700]">Choose a Flavor</span>
            </div>
          </div>
          <div class="grid grid-cols-4 gap-4">
            <CardBase
              v-for="(item, index) in flavors"
              :key="index.id"
              :id="item.id"
              :title="item.title"
              :img="item.img"
            />
          </div>
        </div>
      </div>
      <button class="bg-orange-button">Order Now</button>
    </div>
    <div class="">
      <feedbackCustomer />
    </div>
    <div class="">
      <ourLocation />
    </div>
  </div>
</template>
<script setup>
import { Foods } from "~/content/food/food";
import { bases } from "~/content/food/food";
import { proteins } from "~/content/food/food";
import { vegetables } from "~/content/food/food";
import { flavors } from "~/content/food/food";
import CardFood from "~/components/Food/CardFood.vue";
import CardBase from "~/components/Food/CardOfProduct/CardBase.vue";
import feedbackCustomer from "~/components/customer/feedbackCustomer.vue";
import ourLocation from "~/components/location/ourLocation.vue";
</script>
