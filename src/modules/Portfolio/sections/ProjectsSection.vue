<template>
  <div class="content-container flex flex-col gap-6 mt-16 md:items-center">
    <heading number="03" text="Some Things I've Built" />
    <div class="flex flex-col w-full gap-8">
      <mobile-project-card class="md:hidden" />
      <desktop-project-card :is-even="true" class="hidden md:flex" />
      <desktop-project-card :is-even="false" class="hidden md:flex" />
      <desktop-project-card :is-even="true" class="hidden md:flex" />
    </div>
  </div>
</template>

<script setup>
import Heading from "@/shared/components/Heading.vue";
import MobileProjectCard from "@/modules/Portfolio/components/MobileProjectCard.vue";
import DesktopProjectCard from "@/modules/Portfolio/components/DesktopProjectCard.vue";
</script>