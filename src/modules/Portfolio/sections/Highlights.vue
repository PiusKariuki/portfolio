<template>
  <div class="flex flex-col gap-2 pt-10 md:pt-0 w-full">
    <p class="text-green xl">Highlights</p>
    <div class="flex flex-col gap-6">
      <div
          v-for="(item, index) in highlights"
          :key="index"
           class="flex flex-col w-full shadow-lg px-[20px] py-[25px] rounded-md
           text-lightest-slate bg-light-navy gap-2">
        <img :src="item.image" alt="" class="w-10">
        <p class="xl text-green">{{item.title}}</p>
        <p class="sm lg:md tracking-wide">{{item.description}}</p>
      </div>
    </div>
  </div>
</template>

<script setup>

const highlights = [
  {
    title: "Front End Developer",
    image: "/imgs/tag.svg",
    description: "I help bring intuitive and elegant designs to life." +
        "I am a very visual person and there's nothing I admire more than a well thought out interface."
  },
  {
    title: "Back End Developer",
    image: "/imgs/cog.svg",
    description: "I build APIs and organize models to persist data for applications."
  },
]
</script>
