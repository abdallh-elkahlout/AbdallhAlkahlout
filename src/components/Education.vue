<template>
  <h2 class="text-4xl font-bold mb-4 text-center pt-4" data-aos="fade-right">
    Education
  </h2>
  <div class="space-y-16 py-14">
    <div class="space-y-16 py-14">
      <div
        v-for="element in Education"
        :key="element.id"
        data-aos="fade-right"
        class="flex items-center rounded-xl bg-white/75 shadow-lg hover:shadow-xl transition-shadow duration-300"
      >
        <div class="w-1/4 p-4">
          <img :src="element.href" alt="dev" class="w-full h-auto rounded-lg" />
        </div>
        <div class="w-3/4 pl-4 pr-6 py-4">
          <h3
            class="uppercase font-semibold text-primary text-base relative group cursor-pointer"
          >
            {{ element.title }}
            <span
              v-if="element.description"
              class="absolute hidden group-hover:flex items-center justify-center bg-gradient-to-r from-gray-800 to-gray-900 text-white text-sm p-3 rounded-lg shadow-xl -top-20 left-1/2 transform -translate-x-1/2 w-72 z-10 transition-all duration-300 opacity-0 group-hover:opacity-100 group-hover:-top-24"
            >
              {{ element.description }}
              <span
                class="absolute -bottom-2 w-4 h-4 bg-gray-900 rotate-45 transform"
              ></span>
            </span>
          </h3>
          <p class="text-gray-500">{{ element.company }}</p>
          <p class="text-gray-500">{{ element.duration }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const Education = ref([
  {
    id: 1,
    title: "Computer Science",
    company: "Alaqsa University",
    duration: "Septemper 2020 - April 2025",
    href: "https://img.icons8.com/?size=100&id=GdE2olRF4l3i&format=png&color=000000",
  },
  {
    id: 2,
    title: "Full Stack Course",
    company: "Cliver Center",
    duration: "August  2022 - November 2022",
    href: "https://img.icons8.com/?size=100&id=aNnXVGkz2Uuu&format=png&color=000000",
  },
  {
    id: 3,
    title: "React Js Bootcamp",
    company: "Gaza Sky Geeks",
    duration: "January 2023 - January 2023",
    href: "https://img.icons8.com/?size=100&id=8g6WJkjf0vaP&format=png&color=000000",
  },
]);
</script>
