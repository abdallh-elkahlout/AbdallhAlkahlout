<template>
  <section class="relative w-full p-3 bg-primary2">
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-4 gap-4">
      <div class="order-2 md:order-1 col-span-1 rounded-3xl p-4 bg-white">
      <Experience/>
      </div>
      <div
        class="order-1 md:col-span-2 md:col-start-2 rounded-3xl p-4 bg-white relative overflow-hidden"
      >
        <mainHero />
      </div>
      <div
        class="order-3 md:order-3 md:col-span-1 md:col-start-4 rounded-3xl p-4 bg-white"
      >
      <Education/>
      </div>
    </div>
  </section>
</template>

<script setup>
import { defineAsyncComponent } from "vue";
const mainHero = defineAsyncComponent(() => import("./MainHero.vue"));
const Experience = defineAsyncComponent(() => import("./Experience.vue"));
const Education = defineAsyncComponent(() => import("./Education.vue"));
</script>

<style scoped>
.bg-primary2 {
  height: auto;
}
</style>