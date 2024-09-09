<template>
  <div>
    <div class="w-full h-[561px] my-3">
      <div class="middle-container grid grid-cols-[55%_35%] gap-[7.1rem]">
        <div class="flex flex-col justify-center gap-6">
          <p class="text-[16px] font-semibold">Order summary</p>
          <div
            v-for="(item, index) in Foods.slice(0, 2)"
            :key="index"
            class="flex items-center justify-between"
          >
            <img
              class="w-[62px] h-[62px] rounded-full"
              :src="item.img"
              alt=""
            />
            <div class="flex flex-col gap-1">
              <span class="text-[16px]">{{ item.title }}</span>
              <p class="text-[12px]">Tuna* • Ground Spicy Tuna* • Avocado...</p>
            </div>
            <div class="flex gap-10 items-center">
              <span class="text-[16px] font-medium">${{ item.price }}</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#5f6368"
              >
                <path
                  d="M200-200h57l391-391-57-57-391 391v57Zm-80 80v-170l528-527q12-11 26.5-17t30.5-6q16 0 31 6t26 18l55 56q12 11 17.5 26t5.5 30q0 16-5.5 30.5T817-647L290-120H120Zm640-584-56-56 56 56Zm-141 85-28-29 57 57-29-28Z"
                />
              </svg>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#5f6368"
              >
                <path
                  d="M280-120q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520ZM360-280h80v-360h-80v360Zm160 0h80v-360h-80v360ZM280-720v520-520Z"
                />
              </svg>
            </div>
          </div>
        </div>
        <div>
          <div
            class="h-fit flex flex-col gap-[1rem] pl-6 p-4 border rounded-md"
          >
            <span class="text-[16px] font-medium">Payment Method</span>
            <div class="flex flex-col gap-2 *:text-xs">
              <label for="ehange" class="text-blue-600"
                >Change payment methods</label
              >
              <div
                class="flex items-center justify-between p-2 py-3 pl-4 border rounded-md bg-green-100 *:text-green-800"
              >
                <div class="flex items-center gap-2">
                  <img
                    class="w-7 h-7"
                    src="/assets/images/masterCard.svg"
                    alt=""
                  />
                  <span>Mastercard</span>
                </div>
                <span>**** 5987</span>
              </div>
            </div>
            <div class="flex flex-col gap-2">
              <span class="text-[16px]">Voucher</span>
              <div class="w-full flex gap-3 *:text-sm">
                <input
                  class="w-[80%] pl-3 p-2 border rounded-md focus:outline-none"
                  type="text"
                  placeholder="freeship"
                />
                <button class="p-2 px-3 rounded-md bg-orange-100">Apply</button>
              </div>
              <span
                class="w-fit text-xs text-orange-600 p-1 bg-orange-200 rounded-xl"
                >freeship</span
              >
            </div>
            <div class="flex flex-col gap-2">
              <span class="text-[16px] font-medium">Summary</span>
              <div
                class="flex flex-col gap-2 *:text-xs *:flex *:justify-between"
              >
                <div class="">
                  Subtotal <span class="font-medium">$35</span>
                </div>
                <div class="">Ship <span class="font-medium">$0</span></div>
                <div class="">Fee <span class="font-medium">$0</span></div>
                <div class="border-t my-3"></div>
                <div>
                  Total
                  <span class="text-xl font-semibold text-orange-600">$35</span>
                </div>
              </div>
            </div>
            <NuxtLink
              to="/purchase/purchaseSucces"
              class="flex justify-center text-[16px] text-white py-3 bg-[#F96540] rounded-full my-2"
              >Proceed to payment</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
    <div class="w-full h-[539px] flex flex-col gap-4">
      <span class="text-[24px] font-semibold pl-[7rem]"
        >You might also like</span
      >
      <div class="middle-container grid grid-cols-4 gap-4">
        <CardFood
          v-for="(item, index) in Foods.slice(0, 4)"
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
  </div>
</template>

<script setup>
import { Foods } from "~/content/food/food";
import CardFood from "~/components/Food/CardFood.vue";
</script>

<style lang="scss" scoped></style>
