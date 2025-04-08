<template>
  <section id="services" class="text-white mt-20">
    <h2
      class="text-4xl font-bold mb-4 text-center text-black"
      data-aos="fade-up"
    >
      My Services
    </h2>
    <div
      class="py-8 xl:px-16 px-4 sm-py-16 grid grid-cols-1 gap-6 pt-10 sm-grid-cols-2 md-gap-10 md-pt-12 lg:grid-cols-3"
    >
      <div
        class="px-[12px] mb-[24px]"
        data-aos="fade-up"
        v-for="element in services"
        :key="element.id"
      >
        <div
          class="mt-[30px] relative flex flex-col justify-center text-center rounded-[30px] bg-white"
        >
          <div class="mt-[-30px] flex justify-center relative">
            <div class="mt-[-7px] p-[15px] relative bg-[#fff] rounded-[50%]">
              <img
                :src="element.icon"
                alt="service-icon"
                class="h-[55px] w-[55px] relative z-[1]"
              />
            </div>
          </div>
          <div class="p-[15px]">
            <h3 class="uppercase font-semibold text-primary text-base mb-3">
              {{ element.name }}
            </h3>
            <p
              class="text-[14px] leading-[20px] text-gray-500 tracking-[0.03rem]"
            >
              {{ element.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
const services = ref([
  {
    id: 1,
    icon: "https://img.icons8.com/?size=100&id=49407&format=png&color=000000",
    name: "Visual Effects & Transitions",
    description:
      "Adding engaging visual effects and transitions with Vue.js and Tailwind CSS to enhance user experience",
  },
  {
    id: 2,
    icon: "https://img.icons8.com/?size=100&id=9xn9Hsa-alnl&format=png&color=000000",
    name: "Responsive Web Interfaces",
    description:
      "Crafting seamless, responsive web interfaces using Vue.js, Tailwind CSS, and JavaScript for all devices.",
  },
  {
    id: 3,
    icon: "https://img.icons8.com/?size=100&id=63911&format=png&color=000000",
    name: "Design to Code Conversion",
    description:
      "Transforming Figma or Sketch designs into interactive web interfaces with Vue.js and Tailwind CSS.",
  },
  {
    id: 4,
    icon: "https://img.icons8.com/?size=100&id=RaljsbuV3tuS&format=png&color=000000",
    name: "Single Page Applications (SPA)",
    description:
      "Building fast, interactive SPAs with Vue.js, Vuex, and JavaScript for a smooth user experience.",
  },
  {
    id: 5,
    icon: "https://img.icons8.com/?size=100&id=64810&format=png&color=000000",
    name: "Website Redesign",
    description:
      "Revamping outdated websites into modern, responsive designs using Tailwind CSS and Vue.js.",
  },
  {
    id: 6,
    icon: "https://img.icons8.com/?size=100&id=wQOC4rdvJ9jE&format=png&color=000000",
    name: "API Integration",
    description:
      "Integrating front-end interfaces with APIs using JavaScript and Vue.js for seamless data display.",
  },
  {
    id: 7,
    icon: "https://img.icons8.com/?size=100&id=46806&format=png&color=000000",
    name: "E-Commerce Interface Design",
    description:
      "Designing responsive, user-friendly e-commerce interfaces with Vue.js and Tailwind CSS.",
  },
  {
    id: 8,
    icon: "https://img.icons8.com/?size=100&id=46866&format=png&color=000000",
    name: "Reusable UI Components",
    description:
      "Designing reusable UI components with Vue.js to streamline development and ensure consistency",
  },
]);
</script>
