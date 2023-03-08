<template>
  <navbar @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen"/>
  <sidebar v-if="state.isSidebarOpen" @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen"/>
  <div class="flex w-full flex-col md:flex-row md:pt-24">
    <hero-section/>
    <highlights/>
  </div>
  <companies/>
  <about-me/>
  <work-experience/>
  <projects-section/>
</template>

<script setup>
import Navbar from "@/shared/components/Navbars/Navbar.vue";
import Sidebar from "@/shared/components/Sidebars/Sidebar.vue";
import {reactive} from "vue";
import HeroSection from "@/modules/Portfolio/sections/HeroSection.vue";
import Highlights from "@/modules/Portfolio/sections/Highlights.vue";
import AboutMe from "@/modules/Portfolio/sections/AboutMe.vue";
import Companies from "@/modules/Portfolio/sections/Companies.vue";
import WorkExperience from "@/modules/Portfolio/sections/WorkExperience.vue";
import ProjectsSection from "@/modules/Portfolio/sections/ProjectsSection.vue";

const state = reactive({
  isSidebarOpen: false
})

</script>
