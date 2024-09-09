<template>
  <div class="w-full h-[950px] overflow-hidden">
    <div class="w-full flex gap-[6.25rem]">
      <div class="w-[50%] pl-[8%] flex flex-col mt-[2.5rem] gap-4">
        <span class="text-[48px]">Give the Perfect Gift</span>
        <span class="text-[16px] text-gray-400"
          >Get a voucher for yourself or gift one to a friend
        </span>
        <div class="flex flex-col gap-3 w-full">
          <span class="text-[20px] font-medium">What kind of gift is it?</span>
          <div class="flex gap-[1.5rem] w-full">
            <div
              class="border border-[#BD4C31] rounded-xl p-4 flex items-center w-full gap-3"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="25px"
                viewBox="0 -960 960 960"
                width="25px"
                fill="#BD4C31"
              >
                <path
                  d="M160-80v-440H80v-240h208q-5-9-6.5-19t-1.5-21q0-50 35-85t85-35q23 0 43 8.5t37 23.5q17-16 37-24t43-8q50 0 85 35t35 85q0 11-2 20.5t-6 19.5h208v240h-80v440H160Zm400-760q-17 0-28.5 11.5T520-800q0 17 11.5 28.5T560-760q17 0 28.5-11.5T600-800q0-17-11.5-28.5T560-840Zm-200 40q0 17 11.5 28.5T400-760q17 0 28.5-11.5T440-800q0-17-11.5-28.5T400-840q-17 0-28.5 11.5T360-800ZM160-680v80h280v-80H160Zm280 520v-360H240v360h200Zm80 0h200v-360H520v360Zm280-440v-80H520v80h280Z"
                />
              </svg>
              <div class="flex flex-col gap-1 w-full">
                <span class="text-[18px] font-medium">For one individual</span>
                <span class="text-[12px]"
                  >Send a gift card to one recipient</span
                >
              </div>
            </div>
            <div
              class="border border-[#8a8a8a] rounded-xl p-4 flex items-center w-full gap-3"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="25px"
                viewBox="0 -960 960 960"
                width="25px"
                fill="#999999"
              >
                <path
                  d="M350-63q-46 0-82.5-24T211-153q-16 21-40.5 32.5T120-109q-51 0-85.5-35T0-229q0-43 28-77.5T99-346q-14-20-21.5-42.5T70-436q0-40 20.5-75t57.5-57q5 18 13.5 38.5T181-494q-14 11-22 26.5t-8 32.5q0 56 46 69t87 21l19 32q-11 32-19 54.5t-8 40.5q0 30 21.5 52.5T350-143q38 0 63-34t41-80q16-46 24.5-93t13.5-72l78 21q-9 45-22 103t-36.5 110.5Q488-135 449.5-99T350-63ZM120-189q17 0 28.5-11.5T160-229q0-17-11.5-28.5T120-269q-17 0-28.5 11.5T80-229q0 17 11.5 28.5T120-189Zm284-158q-46-41-83.5-76.5t-64.5-69q-27-33.5-41.5-67T200-629q0-65 44.5-109.5T354-783q4 0 7 .5t7 .5q-4-10-6-20t-2-21q0-50 35-85t85-35q50 0 85 35t35 85q0 11-2 20.5t-6 19.5h14q60 0 102 38.5t50 95.5q-18-3-40.5-3t-41.5 2q-7-23-25.5-38T606-703q-35 0-54.5 20.5T498-623h-37q-35-41-54.5-60.5T354-703q-32 0-53 21t-21 53q0 23 13 47.5t36.5 52q23.5 27.5 57 58.5t74.5 67l-57 57Zm76-436q17 0 28.5-11.5T520-823q0-17-11.5-28.5T480-863q-17 0-28.5 11.5T440-823q0 17 11.5 28.5T480-783ZM609-63q-22 0-43.5-6T524-88q11-14 22-33t20-35q11 7 22 10t22 3q32 0 53.5-22.5T685-219q0-19-8-41t-19-54l19-32q42-8 87.5-21t45.5-69q0-40-29.5-58T716-512q-42 0-98 16t-131 41l-21-78q78-25 139-42t112-17q69 0 121 41t52 115q0 25-7.5 47.5T861-346q43 5 71 39.5t28 77.5q0 50-34.5 85T840-109q-26 0-50.5-11.5T749-153q-20 42-56.5 66T609-63Zm232-126q17 0 28-11.5t11-28.5q0-17-11.5-29T840-270q-17 0-28.5 11.5T800-230q0 17 12 29t29 12Zm-721-40Zm360-594Zm360 593Z"
                />
              </svg>
              <div class="flex flex-col gap-1">
                <span class="text-[18px] font-medium">Group gift card</span>
                <span class="text-[12px]"
                  >Pool money from multiple <br />
                  contributors for one recipient</span
                >
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col gap-3">
          <span class="text-[20px] font-medium">eGift card amounts</span>
          <div
            class="flex w-fit p-1 justify-center text-[14px] *:border-r-white"
          >
            <button
              v-for="(price, index) in amount"
              :key="index"
              class="border border-[#FCDD80] p-2 px-6 text-[#ad9753] first:rounded-l-md last:rounded-r-md first:bg-[#FCDD80] last:border-[#FCDD80]"
            >
              {{ price }}
            </button>
          </div>
          <NuxtLink
            class="text-[16px] text-[#379AE6] font-medium cursor-pointer hover:underline hover:scale-95 transition-all ease-in-out duration-200"
            >Add Promo Code</NuxtLink
          >
        </div>
        <div class="flex flex-col gap-4">
          <span class="text-[20px] font-medium">Your details</span>
          <div class="flex flex-col gap-3">
            <input
              class="w-[70%] pl-3 border py-2 rounded-xl focus:outline-none"
              type="text"
              placeholder="Name"
            />
            <input
              class="w-[70%] pl-3 py-2 border rounded-xl focus:outline-none"
              type="text"
              placeholder="Your Email"
            />
            <textarea
              cols="30"
              rows="5"
              class="w-[70%] pl-3 border py-2 rounded-xl focus:outline-none"
              placeholder="Your Message (optional)"
            ></textarea>
          </div>
        </div>
        <div class="flex flex-col gap-3">
          <span class="text-[20px] font-medium">Delivery details</span>
          <div class="flex items-center justify-between w-[70%]">
            <span class="text-[16px]">Send this card to myself</span>
            <label class="inline-flex items-center cursor-pointer">
              <input type="checkbox" value="" class="sr-only peer" checked />
              <div
                class="relative w-11 h-6 bg-gray-200 rounded-full peer peer-focus:ring-4 dark:peer-focus:ring-[#1DD75B] peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:start-[2px] after:bg-white after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-[#1DD75B]"
              ></div>
            </label>
          </div>
        </div>
        <NuxtLink
          to="/checkout/checkoutSelect"
          class="py-2 w-[70%] text-white text-center cursor-pointer mt-4 bg-[#F96540] rounded-full"
        >
          Checkout
        </NuxtLink>
      </div>
      <div class="overflow-hidden w-[50%]">
        <Grid3x4 class="" />
      </div>
    </div>
  </div>
</template>

<script setup>
const amount = ["$25", "$35", "$50", "$100", "Custom"];
import Grid3x4 from "~/components/followUs/Grid3x4.vue";
// import Grid3x4 from "~/components/followUs/Grid3x4.vue";
</script>

<style lang="scss" scoped></style>
