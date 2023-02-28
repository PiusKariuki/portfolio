<template>
  <div @click="emits('toggleSidebar')" class="fixed inset-0 w-screen h-screen bg-transparent">
    <div @click.stop="" class="w-[80vw] h-screen fixed top-0 right-0 bg-light-navy z-50 lg:hidden shadow-lg shadow-navy-shadow">
      <svg
          @click="emits('toggleSidebar')"
          class="w-8 absolute top-8 text-green right-4 z-50" fill="currentColor" viewBox="0 0 16 16"
           xmlns="http://www.w3.org/2000/svg">
        <path
            d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0
            1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8 2.146 2.854Z"/>
      </svg>

      <div class="flex flex-col h-full justify-center mx-auto self-center w-1/2 gap-6 text-lightest-slate">
        <a
            v-for="(item, index) in navItems"
            :href="item.link"
            class="sm text-center">

          <p class="text-green">0{{ index + 1 }}. </p>
          <p class="">{{ item.text }}</p>
        </a>
        <button class="cta py-2 mt-4">Resume`</button>
      </div>

    </div>
  </div>


</template>

<script setup>
import {navItems} from "@/shared/data/navItems.js";

const emits = defineEmits(['toggleSidebar'])

</script>