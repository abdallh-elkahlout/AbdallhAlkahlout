<template>
  <div class="min-h-screen">
    <Suspense>
      <template #default>
        <div class="bg-primary2">
          <heroSection />
          <Skills />
          <Services />
          <Projects />
          <Contact />
          <Footer />
          <backToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>

<script setup>
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init({ duration: 2000, delay: 200 });
import { defineAsyncComponent } from "vue";
import LoadingSpinner from "./components/LoadingSpinner.vue";

const heroSection = defineAsyncComponent(() =>
  import("./components/HeroSection.vue")
);
const Skills = defineAsyncComponent(() => import("./components/Skills.vue"));
const Services = defineAsyncComponent(() =>
  import("./components/Services.vue")
);
const Projects = defineAsyncComponent(() =>
  import("./components/Projects.vue")
);
const Contact = defineAsyncComponent(() => import("./components/Contact.vue"));
const Footer = defineAsyncComponent(() => import("./components/Footer.vue"));
const backToTop = defineAsyncComponent(() =>
  import("./components/backToTop.vue")
);
</script>
