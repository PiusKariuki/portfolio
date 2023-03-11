<template>
  <div class="content-container text-lightest-slate ">
    <div class="flex flex-col md:flex-row shadow-lg rounded-lg bg-green-tint w-full p-4 md:py-16 gap-3 md:justify-between">
      <div class="flex flex-col gap-6 max-w-sm">
        <p class="text-green font-light lg md:xl tracking-wide">
          Trusted by organizations all over the world including.
        </p>
        <p class="hidden md:flex md">
          I have worked and continue to work with these amazing brands and companies.
        </p>
      </div>

      <div class="grid grid-cols-2 gap-1 w-full max-w-xl">
        <img
            class="bg-white w-full object-scale-down h-32 md:h-44"
            :key="index"
            v-for="(item, index) in companies"
            :src="item" alt="">
      </div>
    </div>
  </div>
</template>

<script setup>
const companies = ['/imgs/medrite.svg', '/imgs/welz.png', '/imgs/xeron.svg', '/imgs/speeddates.jpg']
</script>

<style scoped>

</style>