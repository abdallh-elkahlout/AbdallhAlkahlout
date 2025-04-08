<template>
  <h2 class="text-4xl font-bold mb-4 text-center pt-4" data-aos="fade-right">
    Experience
  </h2>
  <div class="space-y-16 py-14">
    <div class="space-y-16 py-14">
      <div
        v-for="element in Experience"
        :key="element.id"
        data-aos="fade-right"
        class="flex items-center rounded-xl bg-white/75 shadow-lg hover:shadow-xl transition-shadow duration-300"
      >
        <div class="w-1/4 p-4">
          <img
            :src="element.href"
            alt="dev"
            class="w-full h-auto rounded-lg"
          />
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

const Experience = ref([
  {
    id: 1,
    title: "Front-End Developer",
    company: "Freelance",
    duration: "September 2023 - Present",
    description:
      "Worked as a freelance Front-End Developer, designing and building responsive websites for various clients. Utilized technologies like HTML, CSS, JavaScript, and Tailwind CSS to deliver tailored solutions that meet client needs",
    href: "https://img.icons8.com/?size=100&id=118560&format=png&color=000000",
  },
  {
    id: 2,
    title: "Intern - FrontEnd Development",
    company: "Apex For IT Solution",
    duration: "July 2023 - August 2023",
    description:
      "During my internship at Apex , I contributed to developing website interfaces using [html, javascript , CSS , bootstrap]. Gained hands-on experience in teamwork, performance optimization, and adhering to quality standards. Developed practical skills in building responsive interfaces and improving user experience.",
    href: "https://img.icons8.com/?size=100&id=1l4Ua9PN0EDB&format=png&color=000000",
  },
  {
    id: 3,
    title: "Front-End Developer - Personal Projects",
    company: "Self-Initiated",
    duration: "December 2022 - Present",
    description:
      "Designed and developed a series of personal web projects to enhance my skills and explore modern front-end technologies. Built responsive and interactive applications using tools like Vue.js, Tailwind CSS, and JavaScript, focusing on clean code and user-centric design.",
    href:"https://img.icons8.com/?size=100&id=63911&format=png&color=000000",
    },
]);
</script>
