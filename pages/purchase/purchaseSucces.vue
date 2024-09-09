<template>
  <div class="flex flex-col items-center my-8 gap-8">
    <div class="relative inline-block">
      <div
        class="w-[295px] h-[295px] rounded-full overflow-hidden border border-gray-300"
      >
        <img
          src="/assets/images/paySuccess.png"
          alt="Food Image"
          class="w-full h-full object-cover"
        />
      </div>

      <div class="absolute bottom-2 right-8 bg-green-500 rounded p-2">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5 text-white"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            fill-rule="evenodd"
            d="M16.707 5.293a1 1 0 00-1.414 0L9 11.586 5.707 8.293a1 1 0 10-1.414 1.414l4 4a1 1 0 001.414 0l7-7a1 1 0 000-1.414z"
            clip-rule="evenodd"
          />
        </svg>
      </div>
    </div>
    <p class="text-[32px] font-semibold">Thank you for your purchase!</p>
    <p class="text-[14px] text-gray-400">Food is on its way to you</p>
    <div class="w-[560px] h-[651px] border rounded-lg p-6">
      <div class="flex flex-col gap-4 border-b pb-4">
        <div class="flex justify-between">
          <div class="flex gap-3 items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#F96540"
            >
              <path
                d="M216-96q-29.7 0-50.85-21.5Q144-139 144-168v-528q0-29 21.15-50.5T216-768h72v-96h72v96h240v-96h72v96h72q29.7 0 50.85 21.5Q816-725 816-696v528q0 29-21.15 50.5T744-96H216Zm0-72h528v-360H216v360Zm0-432h528v-96H216v96Zm0 0v-96 96Zm264.21 216q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Zm-156 0q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Zm312 0q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Zm-156 144q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Zm-156 0q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Zm312 0q-15.21 0-25.71-10.29t-10.5-25.5q0-15.21 10.29-25.71t25.5-10.5q15.21 0 25.71 10.29t10.5 25.5q0 15.21-10.29 25.71t-25.5 10.5Z"
              />
            </svg>
            <span class="text-[16px] text-gray-500">Date</span>
          </div>
          <span class="text-[14px]">27/04/2023</span>
        </div>
        <div class="flex justify-between">
          <div class="flex gap-3 items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#F96540"
            >
              <path
                d="M480-480q-60 0-102-42t-42-102q0-60 42-102t102-42q60 0 102 42t42 102q0 60-42 102t-102 42ZM192-192v-96q0-23 12.5-43.5T239-366q55-32 116.29-49 61.29-17 124.5-17t124.71 17Q666-398 721-366q22 13 34.5 34t12.5 44v96H192Zm72-72h432v-24q0-5.18-3.03-9.41-3.02-4.24-7.97-6.59-46-28-98-42t-107-14q-55 0-107 14t-98 42q-5 4-8 7.72-3 3.73-3 8.28v24Zm216.21-288Q510-552 531-573.21t21-51Q552-654 530.79-675t-51-21Q450-696 429-674.79t-21 51Q408-594 429.21-573t51 21Zm-.21-72Zm0 360Z"
              />
            </svg>
            <span class="text-[16px] text-gray-500">Customer</span>
          </div>
          <span class="text-[16px] font-medium">John Miller</span>
        </div>
        <div class="flex justify-between">
          <div class="flex gap-3 items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#F96540"
            >
              <path
                d="M552-432q-50 0-85-35t-35-85q0-50 35-85t85-35q50 0 85 35t35 85q0 50-35 85t-85 35Zm-288 96q-29.7 0-50.85-21.17Q192-378.33 192-408.06v-288.22Q192-726 213.15-747T264-768h576q29.7 0 50.85 21.17Q912-725.67 912-695.94v288.22Q912-378 890.85-357T840-336H264Zm72-72h432q0-30 21.15-51.12 21.15-21.11 50.85-21.11V-624q-29.7 0-50.85-21.15Q768-666.3 768-696H336q0 30-21.15 51.12-21.15 21.11-50.85 21.11V-480q29.7 0 50.85 21.15Q336-437.7 336-408Zm456 216H120q-29.7 0-50.85-21.15Q48-234.3 48-264v-408h72v408h672v72ZM264-408v-288 288Z"
              />
            </svg>
            <span class="text-[16px] text-gray-500">Payment Method</span>
          </div>
          <div class="w-8 h-8">
            <img
              class="w-full h-full"
              src="/assets/images/masterCard.svg"
              alt=""
            />
          </div>
        </div>
      </div>
      <div class="flex flex-col gap-4 mt-5 border-b pb-4">
        <div class="flex justify-between">
          <div class="flex gap-3 items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#F96540"
            >
              <path
                d="M144-96v-768l56 45 56-45 56 45 56-45 56 45 56-45 56 45 56-45 56 45 56-45 56 45 56-45v768l-56-45-56 45-56-45-56 45-56-45-56 45-56-45-56 45-56-45-56 45-56-45-56 45Zm144-216h384v-72H288v72Zm0-132h384v-72H288v72Zm0-132h384v-72H288v72Zm-72 360h528v-528H216v528Zm0-528v528-528Z"
              />
            </svg>
            <span class="text-[16px] text-gray-500">Order Number</span>
          </div>
          <span class="text-[14px]">586789963</span>
        </div>
        <div class="flex justify-between">
          <div class="flex gap-3 items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#F96540"
            >
              <path
                d="M446-216h67v-47q49-8 81-42t32-79q0-45-27.5-77T514-514q-61-22-80.5-37.5T414-592q0-20 17.5-33t45.5-13q28 0 49 13.5t28 36.5l59-25q-12-33-38.5-55.5T513-697v-47h-66v48q-45 10-72 38.5T348-591q0 45 30.5 76.5T475-460q45 16 65.5 34t20.5 42q0 26-21 43.5T488-323q-33 0-58.5-22T395-402l-62 26q12 42 42 71.5t71 40.5v48Zm34 120q-79 0-149-30t-122.5-82.5Q156-261 126-331T96-480q0-80 30-149.5t82.5-122Q261-804 331-834t149-30q80 0 149.5 30t122 82.5Q804-699 834-629.5T864-480q0 79-30 149t-82.5 122.5Q699-156 629.5-126T480-96Zm0-72q130 0 221-91t91-221q0-130-91-221t-221-91q-130 0-221 91t-91 221q0 130 91 221t221 91Zm0-312Z"
              />
            </svg>
            <span class="text-[16px] text-gray-500">Total</span>
          </div>
          <span class="text-[14px]">$35</span>
        </div>
      </div>
      <div class="mt-5 flex flex-col gap-4">
        <span class="text-[14px]">Order Line</span>
        <div
          v-for="(item, index) in Foods.slice(0, 2)"
          :key="index"
          class="flex justify-between items-center"
        >
          <div class="flex gap-4 w-[50vh]">
            <img
              class="w-[94px] h-[94px] rounded-full"
              :src="item.img"
              alt=""
            />
            <div class="flex flex-col justify-center gap-1">
              <span class="text-[16px] font-semibold">{{ item.title }}</span>
              <span class="line-clamp-1 text-[11px] text-gray-400">{{
                item.description
              }}</span>
              <div
                class="text-[14px] w-fit rounded-full px-3 py-1 bg-slate-200"
              >
                x1
              </div>
            </div>
          </div>
          <span class="text-[16px] font-semibold">${{ item.price }}</span>
        </div>
      </div>
      <div class="flex mt-9">
        <NuxtLink
          to="/"
          class="w-full text-center py-2 bg-orange-500 text-white rounded-full"
          >Back to home</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<script setup>
import { Foods } from "~/content/food/food";
</script>

<style lang="scss" scoped></style>
