<template>
  <div class="content-container text-lightest-slate ">
    <div class="flex flex-col md:flex-row shadow-lg w-full rounded-lg bg-light-navy  p-4 lg:pr-20 md:py-16 gap-3  md:gap-12 md:justify-between">
      <div class="flex flex-col gap-6 max-w-sm">
        <p class="text-green h2 mb-3">
          Organizations I have worked with.
        </p>
        <p class="hidden md:flex paragraph md:mt-12">
          I have worked and continue to work with these amazing brands and companies.
        </p>
      </div>

      <div class="grid grid-cols-2 gap-1 w-full lg:w-[45.5%]">
        <img
            class="w-full object-contain h-28 lg:h-32 p-3 lg:p-6 bg-lightest-navy"
            :key="index"
            v-for="(item, index) in companies"
            :src="item" alt="">
      </div>
    </div>
  </div>
</template>

<script setup>
const companies = ['/imgs/companies/medrite.svg', '/imgs/companies/welz.svg', '/imgs/companies/xeron.svg', '/imgs/companies/speeddates.svg']
</script>

<style scoped>

</style>