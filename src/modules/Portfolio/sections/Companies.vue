<template>
  <div class="content-container text-lightest-slate ">
    <div
        class="flex flex-col md:flex-row shadow-lg w-full rounded-lg bg-light-navy  p-4 lg:px-12 md:py-16 gap-3
        md:gap-12 md:justify-between md:items-center">
      <div class="flex flex-col gap-6 max-w-sm">
        <p class="text-green h2">
          Organizations I have worked with.
        </p>
        <p class="hidden md:flex paragraph md:my-4">
          I have worked with these brands and companies to bring amazing software solutions to life.
        </p>
        <a
            :href="links.email"
            class="cta  py-[0.75rem] w-full md:w-44 flex items-center justify-center my-4 md:my-0"
            @click="hireMe">
          Hire Me
        </a>
      </div>

      <div class="grid grid-cols-2 gap-x-1 gap-y-1 w-full lg:w-[45.5%] h-full">
        <a
            v-for="(item, index) in companies"
            :key="item.url"
            :class="item.containerStyles"
            :href="item.url"
            class="w-full h-24 md:h-28 lg:h-28 bg-lightest-navy flex justify-center items-center"
            target="_blank"
        >
          <img
              :key="index"
              :class="item.styles"
              :src="item.logo" alt="icon">
        </a>

      </div>
    </div>
  </div>
</template>

<script setup>
import {reactive} from "vue";

const links = reactive({
  email: import.meta.env.VITE_EMAIL
})

const hireMe = () => {
  gtag("event", "hire_me", {
    'section': 'companies',
  })
}

const companies = [
  {
    logo: "/imgs/companies/medrite.svg",
    styles: "w-24 lg:w-32",
    containerStyles: "rounded-tl-md",
    url: "https://medriteurgentcare.com/"
  },
  {
    logo: "/imgs/companies/welz.svg",
    styles: "w-24 lg:w-32",
    containerStyles: "rounded-tr-md",
    url: "https://www.welz.com/"
  },
  {
    logo: "/imgs/companies/xeron.svg",
    styles: "w-20 lg:w-24",
    containerStyles: "rounded-bl-md",
    url: "https://www.xeronlabs.com/"
  },
  {
    logo: "/imgs/companies/speeddates.svg",
    styles: "h-10 lg:h-14 lg:w-32",
    containerStyles: "rounded-br-md",
    url: "https://www.a-list-events.com/"
  },
]
</script>

