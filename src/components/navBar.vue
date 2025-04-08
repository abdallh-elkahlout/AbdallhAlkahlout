<template>
  <header class="max-w-full z-20">
    <nav
      class="flex border-b-2 border-b-primary2 items-center relative p-3 justify-between md:h-16 h-28 mx-auto md:px-4 container flex-wrap md:flex-nowrap bg-white shadow-md"
    >
      <!-- logo -->
      <div class="text-3xl font-bold flex text-primary">
      <img src="../assets/logo.png" alt="" class="w-16 h-16 rounded-full overflow-hidden mb-3"></div>
      <!-- mobile toggle button -->
      <div class="md:hidden z-30">
        <button
          class="block focus:outline-none"
          @click="isMenuOpen = !isMenuOpen"
        >
          <span class="text-5xl" v-if="isMenuOpen">✕</span>
          <span class="text-5xl" v-else>☰</span>
        </button>
      </div>
      <!-- responsive Menu -->
      <div
        :class="[
          'fixed inset-0 z-20 flex flex-col items-center justify-center bg-primary md:relative md:bg-transparent md:flex md:justify-between md:flex-row md:space-x-5',
          isMenuOpen ? 'block' : 'hidden',
        ]"
      >
        <ul
          class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0 font-medium"
        >
          <li v-for="item in Menu" :key="item.name">
            <a
              :href="item.href"
              class="block transition hover:text-primary ease-linear text-2xl md:text-sm lg:text-lg text-white md:text-black"
              @click="scrollToSection(item.href)"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script setup>
import { ref } from "vue";
const isMenuOpen = ref(false);
const Menu = ref([
  { name: "Services", href: "#services" },
  { name: "Projects", href: "#projects" },
  { name: "Contact", href: "#contact" },
]);
const scrollToSection = (href) => {
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<style scoped></style>
