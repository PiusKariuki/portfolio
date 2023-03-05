<template>
  <navbar @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen"/>
  <sidebar @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen" v-if="state.isSidebarOpen"/>
  <div class="flex w-full flex-col md:flex-row md:pt-24">
    <hero-section />
    <highlights />
  </div>

</template>

<script setup>
import Navbar from "@/shared/components/Navbars/Navbar.vue";
import Sidebar from "@/shared/components/Sidebars/Sidebar.vue";
import {reactive} from "vue";
import HeroSection from "@/modules/Portfolio/components/Hero/HeroSection.vue";
import Highlights from "@/modules/Portfolio/components/Highlights/Highlights.vue";

const state = reactive({
  isSidebarOpen: false
})

</script>
