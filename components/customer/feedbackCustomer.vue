<template>
  <div class="w-full h-[600px]">
    <div class="middle-container grid grid-cols-2 py-10">
      <div class="flex flex-col gap-10">
        <span class="text-5xl font-[400px]">Our happy customers</span>
        <p class="text-2xl w-[80%] h-full">
          {{ currentTestimonial.text }}
        </p>
        <span class="text-2xl font-medium">{{ currentTestimonial.name }}</span>
        <div class="flex gap-3 items-center pt-[75px]">
      
          <img
            class="w-14 h-14 rounded-full"
            v-for="(img, index) in testimonials"
            :key="index"
            :src="img.image"
            :alt="`Image of ${img.name}`"
            @click="setTestimonial(index)"
            :class="{
              'border border-red-500 bg-red-100 cursor-pointer scale-110 transition-all duration-200':
                currentIndex === index,
            }"
          />
          <button
            class="p-4 bg-red-100 rounded-full hover:scale-110 transition-transform duration-300"
            @click="nextTestimonial"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="35px"
              viewBox="0 -960 960 960"
              width="35px"
              fill="#F19E39"
            >
              <path d="M504-480 320-664l56-56 240 240-240 240-56-56 184-184Z" />
            </svg>
          </button>
        </div>
      </div>
      <div class="flex justify-end items-center">
        <img class="w-[520px] rounded-lg" :src="food" alt="Delicious Food" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const person =
  "https://s3-alpha-sig.figma.com/img/be6e/055b/b84078f59fedb0ab8eee6f0eeb77dcc2?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=OuwHa1md1SOE6jEQjNuusm9LR3afsAMQJyDn5mYLmWZyE2ds--BhucpT7rUN-o32ZRwLK0Z7KhC-1XPNWZm1rjusR0yurfYLEA9WGG9G~nQcDP0GrzyeJOjW0SbPzUl6l7KSn2lqFJvkBMK3v7nW6hAZzUhqzHS6KhkIC5TV5e0qvCWU9oALnHwokP-cM~NcmSMurlgL0jghxugjE-2I6sVnyMtWFMTaZGh8IzbCzm2vd7H3vkTg59JAi2QGAqllhY5UVeikLwn7qM~BOLd-ZZt4kxXCAde-TRr4NWoC2Q4CJPf4GCyup5mJoSwk3Rei56RDdGpT77BfVCODg~pHww__";
const person2 =
  "https://s3-alpha-sig.figma.com/img/5ab3/5d22/d3421377b7dc1728cfe1df3aa1d5117d?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=VjmcVhpSBA~JCreFaNtGobZZInbTaU4e4XsWhCmzXJabCKcPOXZ5zXqziaA1zVziIa2bABR9PE6vE9~uiXSQQYw-gdSXHBjFeQIfufDDDsy6-KIULr9DgFTTNOXlKvyT7GmOMCPtg~i0-fEbfwPrxvPK6EzyXGEEnXgmidAzjqSp11K~aOZAv6-knyBv4VJjfAu~xCGg2OcI5CZ6oOpRd0TL5xRMw3F0rgDslWiKQ0wlLeC77q9DbQ6pmMexAw2HYBsmjFRR~sPUaTa-DGqQg0IcPlfSopndNLzl-ZyvIqpAXo9qA8Irx~h8yu9c6Yckr7ouI-l0Bfx7aIkg-Cltlg__";
const person3 =
  "https://s3-alpha-sig.figma.com/img/9dec/d998/351cfde9c45fc40451723b54283aa78c?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=oYsCpemEFohtxsb1vivHpwH1u2paAxy5zN0EIUjqd5sn0WsnrBf4MBcKe-JXd2HLy9J0NYDp3OzehxbTTdKwFbHrcyDntCWlusDKDuFU0tVyRdcBbIIWbq~NGWKmtxsMtFdqj5~o2QhVpgy2WvOnI8O4WbJOMxWVUfHl~fYByBFPwp3WvYUBfYeCuAUqy0uS2kGN5z5sI~ULdFR9M2eSonnNS-TqA0sWj5Gv2ACC5ofwG6DhmDE1qtwA6YSJcunp8kPORvlh7aeRjNO4JZA-9y5EcDfXZpMUFEalmKrwKJ0NB4~r6ss3SpJcIYA-aQIeyrOkk57SIzZwxfWprsQp4w__";
const person4 =
  "https://s3-alpha-sig.figma.com/img/3b72/1d3b/57fcd3eb1a8289465f7dc29e52b574c4?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=RmufmxvbzWgz56lpoXeU~kBmawKGqq737t7tIvgomfKUMC30nD7kJbr8nBifCmUyi4t~rCPMEEgHlFSR3tlVYetPCaZP-vkTR2OZ2ga39NR7-0we8FH1kJ7puTbc6ovaU0acl-Iy6w80dRWPsZYQ3YUhJW13VmLHy88xR7~SFM5DzakkvCWW4dgQmUFXDOURp55MXeUHY4eMKUQP~s5nvVIJf8IBKO2pM9Hd9XxD2AwoYQzDO5OBoq3~dWDecHqgfqiuzICRlownaYwh2T~yTvcQx~3HqxZbNWukWMS4g3z1qNfMzq3~a6fEJpvbBGoKF8YHfSB6-izFK3dpZpL8yg__";
const food =
  "https://s3-alpha-sig.figma.com/img/dc50/6ae0/868248618f96aaa5c78d0de953ccf860?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=SrWm5Ouc6YSXJ-F0mlHyTDjqm3m7FKOgNUurzwDMZOb3GQZOsRiUGRD5GuM7xN5Xl901bIxRj7rirad~fgM1V8FgrD83wcVv0BE3UwLtNvY4J5k-m9ltjfNHN1mdUXlSJhGFljg3kaimMQpnOL~9sCTjOytVnEcE6Vg-x4u403tgk1qhfI7h-Qa5Xafrn3f97IEE9KrMcfeb4CU3Vkj2qQnEIxY-UGIThdlsvifHBoevI1dPqro~DVlr0S6IluB5VDoIoM1SxIUBHNFqjRQNygyFG2NymQSXFBZEVhtwC3kfw08NLdN07r-PtQtvnB0~G8dk6qICcpWsVes2e3Ss~g__";

interface PersonalDetail {
  name: String;
  text: String;
  image: any;
}
const testimonials: PersonalDetail[] = [
  {
    name: "Lauren Martinez",
    text: "I'm a big fan of poke bowls, and this place definitely delivers. The quality of the ingredients is top-notch, and the variety of toppings allows you to customize your bowl.",
    image: person,
  },
  {
    name: "John Doe",
    text: "Great atmosphere and friendly staff. The food was delicious, and the portions were perfect.",
    image: person2,
  },
  {
    name: "Jane Smith",
    text: "I love the fresh ingredients and the creativity in their dishes. Highly recommend!",
    image: person3,
  },
  {
    name: "Moldana Jin",
    text: "I love the fresh ingredients and the creativity in their dishes. Highly recommend!",
    image: person4,
  },
];
const currentIndex = ref(0);
const currentTestimonial = ref(testimonials[currentIndex.value]);

const nextTestimonial = () => {
  currentIndex.value = (currentIndex.value + 1) % testimonials.length;
  currentTestimonial.value = testimonials[currentIndex.value];
};

// Function to set the current testimonial based on clicked image
const setTestimonial = (index: number) => {
  currentIndex.value = index;
  currentTestimonial.value = testimonials[currentIndex.value];
};
</script>

<!-- <template>
  <div class="text-center p-6 bg-white rounded-lg shadow-md">
    <img
      :src="currentTestimonial.image"
      alt="Customer"
      class="w-24 h-24 rounded-full mx-auto mb-4"
    />
    <p class="text-lg font-semibold">{{ currentTestimonial.name }}</p>
    <p class="text-gray-600">{{ currentTestimonial.text }}</p>
    <button
      @click="nextTestimonial"
      class="mt-4 px-4 py-2 bg-blue-500 text-white rounded"
    >
      Next
    </button>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

interface Testimonial {
  name: string;
  text: string;
  image: string;
}

const testimonials: Testimonial[] = [
  {
    name: "Lauren Martinez",
    text: "I'm a big fan of poke bowls...",
    image: "/images/lauren.jpg",
  },
  {
    name: "John Doe",
    text: "The best poke bowls in town...",
    image: "/images/john.jpg",
  },
  {
    name: "Jane Smith",
    text: "Amazing variety and quality...",
    image: "/images/jane.jpg",
  },
];

const currentIndex = ref(0);
const currentTestimonial = ref(testimonials[currentIndex.value]);

const nextTestimonial = () => {
  currentIndex.value = (currentIndex.value + 1) % testimonials.length;
  currentTestimonial.value = testimonials[currentIndex.value];
};
</script> -->
