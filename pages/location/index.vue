<template>
  <div>
    <div class="w-full h-[379px]">
      <img class="h-full" src="/assets/images/imgLocation.png" alt="" />
    </div>
    <div class="w-full h-[1290px] flex flex-col items-center my-5">
      <span class="text-[48px]">Locations & Hours</span>
      <div class="middle-container grid grid-cols-3 gap-11 my-[3.5rem]">
        <Location
          v-for="local in locations.slice(0, 6)"
          :key="local.id"
          :id="local.id"
          :image="local.image"
          :address="local.address"
          :street="local.street"
          :date="local.date"
          :weekend="local.weekend"
          :phone="local.phone"
          :email="local.email"
        />
      </div>
    </div>
    <div class="">
      <gridGallery />
    </div>
  </div>
</template>

<script setup>
import Location from "~/components/location/Location.vue";
import { locations } from "~/content/food/datalocation";
import gridGallery from "~/components/followUs/gridGallery.vue";
</script>

<style scoped>
.router-link-exact-active {
  color: #f6a200;
}
</style>
