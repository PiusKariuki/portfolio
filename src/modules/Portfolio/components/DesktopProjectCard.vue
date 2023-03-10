<template>
  <div class="flex items-center">
    <div
        :class="[!isEven ? 'order-2': 'order-0']"
        class="flex w-6/12 bg-green-tint hover:bg-transparent rounded-lg">
      <img
          alt=""
          class="opacity-10 hover:opacity-100 bg-green-tint rounded-lg h-full"
          :src="item.image">
    </div>
    <div
        :class="[!isEven ? 'order-0 items-start -mr-[25%] text-left' : 'order-2 items-end -ml-[25%] text-right']"
        class="flex flex-col  z-10 w-6/12  gap-4">
      <p class="xs text-green">Featured Project</p>
      <p class="xxl font-bold tracking-wide text-white hover:text-green cursor-pointer -mt-3">Spotify profile</p>
      <div

          class="bg-light-navy rounded-lg flex justify-end items-center w-full hover:shadow-2xl py-4 lg:py-12 px-4 ">
        A web app for visualizing personalized Spotify data. View your top artists, top tracks, recently played tracks,
        and detailed audio information about each track. Create and save new playlists of recommended tracks based on
        your
        existing playlists and more.
      </div>
      <div class="flex items-center gap-4">
        <p
            v-for="(tech, index) in item.technologies"
            :key="index"
            class="lg text-white ">{{tech}}</p>
      </div>
      <svg
          class="h-6 w- cursor-pointer"
          aria-hidden="true" fill="none" stroke="currentColor" stroke-width="2.0" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
        <path
            d="M13.5 6H5.25A2.25 2.25 0 003 8.25v10.5A2.25 2.25 0 005.25 21h10.5A2.25 2.25 0 0018 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25"
            stroke-linecap="round"
            stroke-linejoin="round"></path>
      </svg>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(['isEven', 'item'])
</script>