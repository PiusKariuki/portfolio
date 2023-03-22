<template>
  <div class="content-container text-lightest-slate ">
    <div
        class="flex flex-col md:flex-row shadow-lg w-full rounded-lg bg-light-navy  p-4 lg:px-12 md:py-16 gap-3
        md:gap-12 md:justify-between">
      <div class="flex flex-col gap-6 max-w-sm">
        <p class="text-green h2 mb-3">
          Organizations I have worked with.
        </p>
        <p class="hidden md:flex paragraph md:mt-12">
          I have worked and continue to work with these amazing brands and companies.
        </p>
      </div>

      <div class="grid grid-cols-2 gap-x-1 gap-y-1 w-full lg:w-[45.5%]">
        <a
            :href="item.url"
            target="_blank"
            :key="item.url"
            v-for="(item, index) in companies"
            class="w-full h-24 md:h-28 lg:h-28 bg-lightest-navy flex justify-center items-center"
            :class="item.containerStyles"
        >
          <img
              :class="item.styles"
              :key="index"
              :src="item.logo" alt="icon">
        </a>

      </div>
    </div>
  </div>
</template>

<script setup>
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
    // url: "https://www.xeronlabs.com/"
  },
  {
    logo: "/imgs/companies/speeddates.svg",
    styles: "h-10 lg:h-14 lg:w-32",
    containerStyles: "rounded-br-md",
    url: "https://www.speeddateskenya.com/"
  },
]
</script>

