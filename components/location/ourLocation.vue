<template>
  <div class="w-full h-[320px] ">
    <div class="middle-container bg-[#171A1F] my-5 h-[93%] relative overflow-hidden rounded-lg">
      <div class="grid grid-cols-2 gap-10 py-4">
        <!-- grid 1 -->
        <div class="flex flex-col pt-4 gap-10  pl-14">
          <span class="text-5xl text-white">Find our locations</span>
          <p class="text-lg text-white w-[95%]">
            Serving fresh fish daily at Boston Harbor Islands, Boylston St,
            Congress St, Kendall Square, Cambridge St, Haviland St.
          </p>
          <NuxtLink class="bg-orange-button w-fit">Locations & Hours</NuxtLink>
        </div>
        <!-- grid 2 -->
        <div class="flex gap-4 ">
          <div class="w-[334px] relative top-[40px] ">
            <img class="w-full rounded-full overflow-hidden" :src="picfood" alt="" />
          </div>
          <div class="w-[174px] relative left-3">
            <img class="w-full rounded-full overflow-hidden" :src="picfood2" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const picfood =
  "https://s3-alpha-sig.figma.com/img/820b/b2cc/bfffe6bcefd0db9b6b48f094c2011676?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=nVVKnKm32UpGNFBZMKSqm7pYFZ-cJ5IUULZlsTPL6DZMAyf4K~x-xb8aJWwunDfP41wqQlHoLHnMcplNW0G7CIyUu62KSuXdtM~c9gJefxC9aWa03l8Ozw~j8D~TpUciZEQb~AIazu~zqr3T1bDlbHxlc4Faa3FiLhmj9ViFNNYLUC5TWWMCTOYO6g8Z40bYajLmmnLPRwVXpORw4tZBIy9kjkl-yP19b-zMoleWpROok0LcwLFf3LL0wwEAloMOv6d~S58VzhWQxFV~S1GWjIHQuS5koUcskFUh5IUO0nBZJmrz~eukEwxVsmKZHDJelEje1M9Xl7bQkAJAz99zYg__";
const picfood2 =
  "https://s3-alpha-sig.figma.com/img/b706/24f9/1a3d9879d3871458625f81a2d01483e8?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=KcRZVtAmnnbAC5iax7i2XeZWE3pDisJGvFg3Id9REGbWRZQMmuGNoE8n0azK9QvuDloLMglg3SmgK~j8ofJ512qEvl6jhewHCJenRKwBWZ6~w7F~xZhX1y3zqA6IZRSY6RO0hM8MyLtQ-hAO-ugs8cxmL-yhO7TBp1~fSJtDYPwy1odSxFK~LYBzn9ppnbQcAk~KaHiXRA~sdWQWjBcDUX7sbPl~WiEKohmGxMnuQl3RbEHk~KQB-QkmNmKvDlwN1I27E8a0wCZe8IlFuk6tTL7CIS4tBwrZTkbeuxGvHUlwwy9tvJQYEltY0tlMZcGyCXOxpsaex5Jbuzh8jykxSw__";
</script>
