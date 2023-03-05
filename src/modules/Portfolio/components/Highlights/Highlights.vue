<template>
  <div class="content-container flex flex-col gap-2 pt-10 md:pt-0">
    <p class="text-green xl">Highlights</p>
    <div class="flex flex-col gap-6">
      <div
          v-for="(item, index) in highlights"
          :key="index"
           class="flex flex-col w-full shadow-lg px-[20px] py-[25px] rounded-md
           text-lightest-slate bg-light-navy gap-2">
        <img :src="item.image" alt="" class="w-10">
        <p class="xl text-green">{{item.title}}</p>
        <p class="sm">{{item.description}}</p>
      </div>
    </div>
  </div>
</template>

<script setup>

const highlights = [
  {
    title: "Front End Developer",
    image: "/imgs/tag.svg",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut " +
        "labore " +
        "et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip" +
        " ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu " +
        "fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt" +
        " mollit anim id est laborum."
  },
  {
    title: "Back End Developer",
    image: "/imgs/cog.svg",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut " +
        "labore " +
        "et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip" +
        " ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu " +
        "fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt" +
        " mollit anim id est laborum."
  },
]
</script>
