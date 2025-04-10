<template>
  <section id="contact">
    <h2
      class="text-4xl font-bold text-black mb-4 text-center"
      data-aos="fade-up"
    >
      Contact Me
    </h2>
    <div class="mx-auto relative rounded-lg py-6">
      <div class="grid lg:grid-cols-3 items-center">
        <!-- بيانات الاتصال -->
        <div
          class="grid sm:grid-cols-2 gap-4 relative lg:left-16 max-lg:px-4 z-20"
        >
          <div
            v-for="element in data"
            :key="element.id"
            @click="handleCardClick(element)"
            data-aos="fade-up"
            class="flex flex-col items-center justify-center rounded-lg w-full p-4 text-center bg-white cursor-pointer hover:bg-gray-100 transition"
          >
            <img :src="element.icon" alt="data" height="40" width="40" />
            <h4 class="text-gray-800 text-base font-bold mt-0">
              {{ element.title }}
            </h4>
            <p class="text-sm text-gray-500">{{ element.info }}</p>
          </div>
        </div>

        <!-- فورم الاتصال -->
        <div
          class="lg:col-span-2 bg-primary rounded-lg sm:p-10 p-4 z-10 max-lg:order-1 max-lg:mb-8"
          data-aos="fade-up"
        >
          <form id="contact-form" @submit="sendEmail">
            <div class="max-w-md mx-auto space-y-3">
              <input
                name="name"
                type="text"
                placeholder="Name"
                required
                class="w-full bg-gray-100 rounded-lg py-3 px-6 text-sm outline-none"
              />
              <input
                name="email"
                type="email"
                placeholder="Email"
                required
                class="w-full bg-gray-100 rounded-lg py-3 px-6 text-sm outline-none"
              />
              <textarea
                name="message"
                placeholder="Message"
                rows="6"
                required
                class="w-full bg-gray-100 rounded-lg py-3 px-6 text-sm outline-none"
              ></textarea>
              <button
                type="submit"
                class="px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center"
              >
                <span
                  class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-white border-2 border-transparent"
                ></span>
                <span
                  class="relative text-primary flex items-center justify-center"
                >
                  Send Message
                </span>
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";
import KhamsatIcon from "../assets/khamsat.png";
import MostaqlIcon from "../assets/mostaql.png";

// استيراد مكتبة EmailJS مباشرة
import emailjs from "emailjs-com";

// بيانات التواصل
const data = [
  {
    id: 1,
    icon: "https://img.icons8.com/?size=100&id=96403&format=png&color=000000",
    title: "call me",
    info: "+972 592122005",
  },
  {
    id: 2,
    icon: "https://img.icons8.com/?size=100&id=LKFgxAX29Ko2&format=png&color=000000",
    title: "chat to me",
    info: "abdabdallh707@gmail.com",
  },
  {
    id: 3,
    icon: "https://img.icons8.com/?size=100&id=12598&format=png&color=000000",
    title: "github",
    info: "abdallh-elkahlout",
    link: "https://github.com/abdallh-elkahlout",
  },
  {
    id: 4,
    icon: "https://img.icons8.com/?size=100&id=447&format=png&color=000000",
    title: "linkedin",
    info: "abdallh-elkahlout",
    link: "https://www.linkedin.com/in/abdallh-elkahlout-789b08234/",
  },
  {
    id: 5,
    icon: KhamsatIcon,
    title: "Khamsat",
    info: "abdallh_elkahlout",
    link: "https://khamsat.com/user/abdallh_elkahlout",
  },
  {
    id: 6,
    icon: MostaqlIcon,
    title: "Mostaql",
    info: "abdallh_kahlout",
    link: "https://mostaql.com/u/abdallh_kahlout",
  },
];

// التعامل مع الضغط على كروت البيانات
const handleCardClick = (element) => {
  if (element.title === "call me") {
    const phoneNumber = element.info.replace(/\s/g, "");
    window.location.href = `tel:${phoneNumber}`;
  } else if (element.title === "chat to me") {
    window.location.href = `mailto:${element.info}`;
  } else if (element.link) {
    window.open(element.link, "_blank");
  }
};

// ✅ إرسال الرسالة عبر EmailJS
const sendEmail = (e) => {
  e.preventDefault();

  emailjs.sendForm("service_doyg1b4", "template_6e74j8o", e.target).then(
    () => {
      alert("🚀 تم إرسال الرسالة بنجاح!");
      e.target.reset();
    },
    (error) => {
      alert("❌ حدث خطأ أثناء الإرسال: " + error.text);
    }
  );
};

// بدء مكتبة EmailJS
onMounted(() => {
  emailjs.init("ILz8KOwHyIRZ9K7Za");
});
</script>

<style scoped>
.cursor-pointer {
  cursor: pointer;
}
</style>
