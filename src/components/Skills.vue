<template>
  <section>
    <div
      class="w-full bg-white border-b-5 border-y-4 border-primary2 flex flex-wrap justify-center p-2 gap-0 lg:gap-24"
    >
      <div data-aos="zoom-in-up" v-for="element in Skills" :key="element.id">
        <figure
          class="w-20 h-20 flex justify-center items-center rounded-full ml-2 mt-2"
        >
          <img
            :src="element.icon"
            alt="skill icon"
            class="w-10 h-12 absolute z-20"
          />
        </figure>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
const Skills = ref([
  {
    id: 1,
    icon: "https://img.icons8.com/fluency/48/html-5.png",
  },
  {
    id: 2,
    icon: "https://img.icons8.com/color/48/css.png",
  },
  {
    id: 3,
    icon: "https://img.icons8.com/color/48/javascript.png",
  },
  {
    id: 4,
    icon: "https://img.icons8.com/fluency/48/bootstrap.png",
  },
  {
    id: 5,
    icon: "https://img.icons8.com/color/48/tailwindcss.png",
  },
  {
    id: 6,
    icon: "https://img.icons8.com/fluency/48/vuejs.png",
  },
  {
    id: 7,
    icon: "https://img.icons8.com/fluency/48/vite.png",
  },
  {
    id: 8,
    icon: "https://static-00.iconduck.com/assets.00/vuetify-icon-1793x2048-xtqk92sz.png",
  },
]);
</script>
