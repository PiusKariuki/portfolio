<template>
  <div class="content-container flex flex-col gap-6 mt-16 md:items-center">
    <heading number="03" text="Some Things I've Built" class="max-w-6xl" />
    <div class="flex flex-col w-full gap-8 md:gap-24 items-center max-w-6xl">
      <mobile-project-card v-for="(item, index) in projects" :item="item" :key="index" class="md:hidden" />
      <desktop-project-card
          :is-even="index%2 == 0"
          :item="item"
          v-for="(item, index) in projects" :key="index" class="hidden md:flex" />
    </div>
  </div>
</template>

<script setup>
import Heading from "@/shared/components/Heading.vue";
import MobileProjectCard from "@/modules/Portfolio/components/MobileProjectCard.vue";
import DesktopProjectCard from "@/modules/Portfolio/components/DesktopProjectCard.vue";
import {projects} from "@/shared/data/projects.js";
</script>