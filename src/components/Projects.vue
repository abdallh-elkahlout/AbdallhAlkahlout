<template>
  <section id="projects">
    <h2
      class="text-4xl font-bold mb-4 text-center text-black"
      data-aos="fade-up"
    >
      My Projects
    </h2>
    <div
      class="py-8 px-4 sm:px-8 md:px-12 lg:px-16 grid grid-cols-1 md:grid-cols-2 gap-6 pt-10"
    >
      <div
        style="border-radius: 30px"
        data-aos="fade-up"
        v-for="element in projects"
        :key="element.id"
        class="flex flex-col md:flex-row rounded-3xl bg-white mb-6 shadow-lg"
      >
        <img
          :src="element.image"
          alt="project img"
          class="w-full md:w-1/2 h-full object-cover rounded-full md:rounded-l-lg md:rounded-t-none max-md:rounded-none"
        />
        <div
          class="flex flex-col justify-start p-4 md:p-6 space-y-4 md:space-y-6"
        >
          <span
            class="bg-primary2 w-28 text-center p-2 rounded-3xl text-black text-sm"
            >{{ element.category }}</span
          >
          <h3 class="uppercase text-base font-semibold text-primary">
            {{ element.title }}
          </h3>
          <p class="text-[14px] text-gray-500 tracking-[0.03rem] line-clamp-6">
            {{ element.description }}
          </p>
          <div
            class="flex flex-col sm:flex-row items-center gap-3 mt-auto w-full"
          >
            <button
              class="px-4 py-2 md:px-6 md:py-3 rounded-full relative group w-full sm:w-auto bg-primary text-white hover:bg-opacity-90 transition-all"
            >
              <a :href="element.webUrl" class="relative" target="_blank"
                >Live Review</a
              >
            </button>
            <button
              class="border border-primary px-4 py-2 md:px-6 md:py-3 rounded-full w-full sm:w-auto text-primary hover:bg-primary hover:text-white transition-all"
            >
              <a :href="element.gitUrl" target="_blank">Code Source</a>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
const projects = ref([
  {
    id: 1,
    image: "/school.jpg",
    title: "School Website",
    category: "Web App",
    description:
      "The website is a comprehensive interface for a school management system, featuring sections like an introduction to the school, services, educational stages, and a contact section. It was developed using Vue.js for a modern, dynamic user experience.",
    gitUrl: "https://github.com/abdallh-elkahlout/school",
    webUrl: "https://school-theta-rust.vercel.app",
  },
  {
    id: 2,
    image: "/ella.png",
    title: "Ellamart Store",
    category: "Web App",
    description:
      "Ella Store: Developed using Pinia, Vue.js, and Vuetify, it features a modern and user-friendly interface. It offers precise product categorization with dedicated pages for each category, along with full shopping cart functionalities for a seamless shopping experience.",
    gitUrl: "https://github.com/abdallh-elkahlout/ella-store",
    webUrl: "https://ella-store-smoky.vercel.app/",
  },
  {
    id: 3,
    image: "/contacts.jpg",
    title: "Contacts Manager",
    category: "Web App",
    description:
      "An advanced and user-friendly web application for contact management, developed using Vue.js. The platform enables users to effortlessly create, edit, view, and delete contact records, featuring a smart search functionality that allows filtering contacts by name.",
    gitUrl: "https://github.com/abdallh-elkahlout/contact-manager",
    webUrl: "https://contact-manager-nine-lac.vercel.app/contacts",
  },
  {
    id: 4,
    image: "/dashboard.png",
    title: "Simple Dashboard",
    category: "Web App",
    description:
      "Simple Dashboard is a minimalistic front-end design project showcasing a clean and modern user interface built with Vue.js 3 and Vuetify. It leverages Vue Router for seamless navigation between views. The project focuses on demonstrating proficiency in creating visually appealing layouts using Vuetify's component library and CSS classes, with a simple task management interface as a proof of concept. This project is ideal for showcasing front-end development skills with modern Vue.js tools",
    gitUrl: "https://github.com/abdallh-elkahlout/simple-dashboard",
    webUrl: "https://simple-dashboard-pink.vercel.app/",
  },
  {
    id: 5,
    image: "/oudi.jpg",
    title: "Oudi Perfume",
    category: "Web App",
    description:
      ' "Oudi" is a sophisticated e-commerce platform specializing in perfume sales, characterized by a clean and minimalist design crafted with HTML, CSS, JavaScript, and Bootstrap. This project was successfully developed as part of an internship program at Apex Company.',
    gitUrl: "https://github.com/abdallh-elkahlout/oudi",
    webUrl: "https://abdallh-elkahlout.github.io/oudi/",
  },
  {
    id: 6,
    image: "/store.jpg",
    title: "Store",
    category: "Web App",
    description:
      "e-commerce platform, with its prototype version designed as a perfume store to facilitate hands-on training and skill development. The project was meticulously crafted using HTML,CSS,js,Bootstrap, demonstrating a strong application of web development fundamentals.",
    gitUrl: "https://github.com/abdallh-elkahlout/store",
    webUrl: "https://abdallh-elkahlout.github.io/store/",
  },
  {
    id: 7,
    image: "/foxclore.jpg",
    title: "foxclore",
    category: "Web App",
    description:
      "The website was crafted during a front-end development training program, where a diverse set of skills was applied to deliver a visually appealing and user-friendly interface. The project was developed using HTML, CSS, and Bootstrap.",
    gitUrl: "https://github.com/abdallh-elkahlout/Foxclore",
    webUrl: "https://abdallh-elkahlout.github.io/Foxclore/",
  },
  {
    id: 8,
    image: "acne.jpg",
    title: "Acne",
    category: "Web App",
    description:
      "The website was developed during a freelance engagement as a commissioned project, designed as a single-page platform delivering comprehensive medical information on acne. It was skillfully built using HTML, CSS, and Bootstrap.",
    gitUrl: "https://github.com/abdallh-elkahlout/acne",
    webUrl: "https://abdallh-elkahlout.github.io/acne/",
  },
  {
    id: 9,
    image: "/bondi.jpg",
    title: "Bondi",
    category: "Web App",
    description:
      "The website was crafted during a front-end development training program, where a diverse set of skills was applied to deliver a visually appealing and user-friendly interface. The project was developed using HTML, CSS, and Bootstrap.",
    gitUrl: "https://github.com/abdallh-elkahlout/bondi",
    webUrl: "https://abdallh-elkahlout.github.io/bondi/",
  },
  {
    id: 10,
    image: "/bootcamp.jpg",
    title: "Frontend Bootcamp",
    category: "Web App",
    description:
      "The website was crafted during a front-end development training program, where a diverse set of skills was applied to deliver a visually appealing and user-friendly interface. The project was developed using HTML, CSS, and Bootstrap.",
    gitUrl: "https://github.com/abdallh-elkahlout/Frontend-Bootcamp",
    webUrl: "https://abdallh-elkahlout.github.io/Frontend-Bootcamp/",
  },
  {
    id: 11,
    image: "/medcare.jpg",
    title: "Medcare",
    category: "Web App",
    description:
      "A medical website developed during the initial phase of a Full Stack web development course, aimed at showcasing the skills acquired in front-end design. The website was built using only HTML and CSS, and features multiple sections presented with diverse layout styles.",
    gitUrl: "https://github.com/abdallh-elkahlout/medcare",
    webUrl: "https://abdallh-elkahlout.github.io/medcare/",
  },
]);
</script>
