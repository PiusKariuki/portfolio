<template>
  <navbar @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen"/>
  <sidebar @toggleSidebar="state.isSidebarOpen = !state.isSidebarOpen" v-if="state.isSidebarOpen"/>
</template>

<script setup>
import Navbar from "@/shared/components/Navbars/Navbar.vue";
import Sidebar from "@/shared/components/Sidebars/Sidebar.vue";
import {reactive} from "vue";

const state = reactive({
  isSidebarOpen: false
})

</script>
