<template>
  <div class="flex content-container justify-between items-center z-50">
    <svg
        @click="emits('toggleSidebar')"
        class="h-10"
        aria-hidden="true"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg">
      <path
          d="M3.75 9h16.5m-16.5 6.75h16.5"
          stroke-linecap="round"
          stroke-linejoin="round">
      </path>
    </svg>
    <p class="nav-text hidden">About Me</p>
    <p class="nav-text hidden">Portfolio</p>
    <img src="/imgs/punch.svg" alt="" class="h-10">
    <button class="h-10 rounded-3xl px-6  bg-slate-200 font-semibold z-50">Contact Me</button>
  </div>
</template>

<script setup>

const emits = defineEmits(['toggleSidebar'])
</script>