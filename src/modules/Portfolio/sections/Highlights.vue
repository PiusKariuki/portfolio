<template>
  <div class="flex flex-col gap-2 pt-10 md:pt-0 w-full">
    <p class="text-green font-semibold xxl mb-3">Highlights</p>
    <div class="flex flex-col gap-6">
      <div
          v-for="(item, index) in highlights"
          :key="index"
           class="flex flex-col w-full shadow-lg px-[20px] py-[25px] rounded-md
           text-lightest-slate bg-light-navy gap-2">
        <img :src="item.image" alt="" class="w-10">
        <p class="xxl text-green">{{item.title}}</p>
        <div v-html="item.description" class="md lg:md tracking-wide" />
      </div>
    </div>
  </div>
</template>

<script setup>

const highlights = [
  {
    title: "Front End Developer",
    image: "/imgs/tag.svg",
    description: `<p>
                    I build intuitive and elegant interfaces.<br />I am a very visual person and there's nothing I
                    admire more than a refined interface.
                    </p>`
  },
  {
    title: "Back End Developer",
    image: "/imgs/cog.svg",
    description: "I build APIs and organize models to persist data for applications."
  },
]
</script>
