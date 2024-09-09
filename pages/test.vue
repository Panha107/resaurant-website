<!-- <template>
  <section class="w-full h-[800px] mt-[10rem] grid grid-cols-2 overflow-hidden">
    <div class="pl-36 flex flex-col justify-center gap-8">
      <h2 class="font-semibold text-[48px] leading-[68px]">
        Traditional Heritage, <br />
        Modern Result
      </h2>
      <p class="text-[16px] leading-[26px]">
        One of the reasons for poke's popularity is its versatility. While the
        traditional version remains a favorite, there are now numerous
        variations available, allowing people to customize their poke bowls
        according to their preferences.
      </p>
    </div>

    <div class="relative h-[700px]">
      <div
        class="w-[90%] h-[600px] border-4 border-[#F96540] rounded-full absolute bottom-7 -right-[50%]"
      ></div>
      <img
        src="https://s3-alpha-sig.figma.com/img/fb5e/825d/d390a7bbc6d6310566293450a6102c12?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Q3ujY0Nv4xewUUVOzZQQmTPbfzTKhOPj-CQIf7OFETY-d6ULSUwlQMF9ymnMg5-aUC0A8FUeGiqRs-OSwH2AAODgYgQZl-ejBqVQP06GRyDvUwifm8rQk6cyQJWHrEN7-VZ~3P-jbE4pehQ6qslyMuhQQvSIO0kA4mqXCmo-9lajVBUseaCFPJ47E7ZYB46a0-9nsa~IMlqpveUzN9TCw6Ed2HbB-g87cbZeFfMxMDcSZ-G1EhVp8zf2YsJcP3gtMqzuAW0qJtR23xmXkjn8WNooU0M8vuUv0RjomTbn9jwTeJ-WL~uX9CutAJDKxF3SVB-K-iLXCbquGyFshF2N1w__"
        alt="Big_bowl_image"
        class="w-[440px] h-[440px] overflow-hidden rounded-full absolute top-24 left-52"
      />
      <img
        src="https://s3-alpha-sig.figma.com/img/fb5e/825d/d390a7bbc6d6310566293450a6102c12?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Q3ujY0Nv4xewUUVOzZQQmTPbfzTKhOPj-CQIf7OFETY-d6ULSUwlQMF9ymnMg5-aUC0A8FUeGiqRs-OSwH2AAODgYgQZl-ejBqVQP06GRyDvUwifm8rQk6cyQJWHrEN7-VZ~3P-jbE4pehQ6qslyMuhQQvSIO0kA4mqXCmo-9lajVBUseaCFPJ47E7ZYB46a0-9nsa~IMlqpveUzN9TCw6Ed2HbB-g87cbZeFfMxMDcSZ-G1EhVp8zf2YsJcP3gtMqzuAW0qJtR23xmXkjn8WNooU0M8vuUv0RjomTbn9jwTeJ-WL~uX9CutAJDKxF3SVB-K-iLXCbquGyFshF2N1w__"
        alt="sm_bowl_image"
        class="w-[206px] h-[206px] rounded-full absolute -right-28 -top-2 z-20"
      />
      <img
        src="https://s3-alpha-sig.figma.com/img/fb5e/825d/d390a7bbc6d6310566293450a6102c12?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Q3ujY0Nv4xewUUVOzZQQmTPbfzTKhOPj-CQIf7OFETY-d6ULSUwlQMF9ymnMg5-aUC0A8FUeGiqRs-OSwH2AAODgYgQZl-ejBqVQP06GRyDvUwifm8rQk6cyQJWHrEN7-VZ~3P-jbE4pehQ6qslyMuhQQvSIO0kA4mqXCmo-9lajVBUseaCFPJ47E7ZYB46a0-9nsa~IMlqpveUzN9TCw6Ed2HbB-g87cbZeFfMxMDcSZ-G1EhVp8zf2YsJcP3gtMqzuAW0qJtR23xmXkjn8WNooU0M8vuUv0RjomTbn9jwTeJ-WL~uX9CutAJDKxF3SVB-K-iLXCbquGyFshF2N1w__"
        alt="sm_bowl_image"
        class="w-[206px] h-[206px] rounded-full absolute -right-28 -bottom-12"
      />
    </div>
  </section>
</template> -->

<!-- <template>
  <div>
    <login />
  </div>
</template>
<script setup>
import Login from "~/components/Login.vue";
</script> -->
<!-- <template>
  <teleport to="body">
    <div
      v-if="isOpen"
      class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50"
    >
      <div class="bg-white p-6 rounded shadow-md w-1/3">
        <h2 class="text-xl font-bold mb-4">Modal Title</h2>
        <p class="text-gray-700 mb-6">This is the modal content.</p>
        <button
          @click="closeModal"
          class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600"
        >
          Close Modal
        </button>
      </div>
    </div>
  </teleport>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);

const closeModal = () => {
  isOpen.value = false;
};

defineExpose({
  openModal: () => {
    isOpen.value = true;
  },
});
</script> -->

<!-- <template>
  <div class="flex flex-col items-center justify-center h-screen">
    Button to trigger login modal
    <button
      @click="showLogin = true"
      class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600"
    >
      Show Login
    </button>

    Login modal component with teleport
    <Login v-if="showLogin" :isVisible="showLogin" @close="showLogin = false" />
  </div>
</template>
<script setup>
import { ref } from "vue";
import Login from "~/components/Login.vue";

const showLogin = ref(false);
</script> -->

<!-- <template>
  <div>
    <iframe
      width="600"
      height="450"
      style="border: 0"
      loading="lazy"
      allowfullscreen
      referrerpolicy="no-referrer-when-downgrade"
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15684.622947588566!2d104.8994709147298!3d11.562108946603837!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3109514e3f4177c9%3A0xf1b2e815b0f2c4f1!2sPhnom%20Penh%2C%20Cambodia!5e0!3m2!1sen!2sus!4v1693476752291!5m2!1sen!2sus"
    ></iframe>
  </div>
  <button @click="clicka()">click</button>
  <div class="" v-if="active">
    <button @click="addtocard()">allllll</button>
  </div>
</template>

<script setup>
const active = ref(false);
const clicka = () => {
  active.value = !active.value;
};
const addtocard = () => {
  if (true) {
    clicka();
  }
};
</script>
=

<style lang="scss" scoped></style> -->

<template>
  <div
    class="w-[267px] h-[240px] flex flex-col items-center shadow-[3px_3px_4px_0px_#928390] rounded-lg mt-[8.25rem] relative"
  >
    <div
      class="w-[219px] h-[219px] justify-center rounded-full overflow-hidden absolute top-[-7.25rem]"
    >
      <img
        class="w-full h-full hover:scale-105 transition-all ease-in-out duration-400"
        src="https://s3-alpha-sig.figma.com/img/80cd/5907/4d9dbfcbcdb0c53cc9064e2f801f2a60?Expires=1726444800&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=X1aNBC5AgIk-jx6iOjM70kwO6Zg~LctN4GbYRy9uM8e3Cnt20vidpBFdMuet0ULBmjUvf7xvYLDZdOLwrTrPsOwt81uMTRnL-c-aqCN0U0Aing6QXMQubqIi-gArySEymIgmnRT1uWkXaU-jjvGCXZLJqzvceC54CPPRJOJsq~YTS0lYFBOGkDG0NFOVD7hLnMENLbZbj9ckJMeUBQowFIDH-RtCt1kmCe9W0~sqXqRQTjC87FmmxLln1bIS~IbZP4icnNLVCdlKOzp4OnksHnSSBx6G8jxwVSmdzsgLSu0psNTeJhkb0HGDBQYUoXvepcAeSz-PNNujzMj25qvNww__"
        alt=""
      />
    </div>
    <div class="w-full p-4 flex flex-col gap-4 mt-[7rem] border">
      <span class="text-lg font-medium">Coka Cola</span>
      <div class="flex justify-between items-center border">
        <div class="text-lg">$10</div>
        <NuxtLink
          class="text-sm p-2 bg-orange-100 text-orange-600 w-fit rounded-full cursor-pointer hover:scale-95 transition-all duration-200 ease-linear"
          >Add to cart</NuxtLink
        >
      </div>
    </div>
  </div>
</template>
