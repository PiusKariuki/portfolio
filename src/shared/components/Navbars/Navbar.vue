<template>
  <div class="flex content-container justify-between items-center">
    <svg
        @click="emits('toggleSidebar')"
        class="w-12"
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
    <img src="/imgs/punch.svg" alt="" class="w-12">
    <button class="rounded-3xl px-6 py-2 bg-slate-200">Contact Me</button>
  </div>
</template>

<script setup>

const emits = defineEmits(['toggleSidebar'])
</script>