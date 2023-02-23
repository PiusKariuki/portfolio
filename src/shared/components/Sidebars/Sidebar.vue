<template>
  <div class="w-screen h-screen fixed inset-0 bg-white z-50 lg:hidden">
    <!--    x-mark-->
    <svg
        @click="emits('toggleSidebar')"
        aria-hidden="true"
        class="w-12 absolute top-4 right-4 z-50"
        fill="none"
        stroke="currentColor"
        stroke-width="1.0"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg">
      <path
          d="M9.75 9.75l4.5 4.5m0-4.5l-4.5 4.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
          stroke-linecap="round"
          stroke-linejoin="round">
      </path>
    </svg>

    <div class="flex flex-col gap-8 relative content-container">
      <img alt="" class="w-12 h-12 mt-8" src="/imgs/punch.svg">
      <div class="flex w-full gap-3 items-center">
        <p class="nav-text">About Me</p>
      </div>
      <div class="flex w-full gap-3 items-center">
        <p class="nav-text">Portfolio</p>
      </div>
    </div>
    </div>


</template>

<script setup>
const emits = defineEmits(['toggleSidebar'])

</script>