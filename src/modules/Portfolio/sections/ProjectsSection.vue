<template>
  <div class="content-container flex flex-col gap-6 mt-16 md:items-center">
    <heading number="03" text="Some Things I've Built" />
    <div class="flex flex-col w-full gap-8">
      <mobile-project-card />
    </div>
  </div>
</template>

<script setup>
import Heading from "@/shared/components/Heading.vue";
import MobileProjectCard from "@/modules/Portfolio/components/MobileProjectCard.vue";
</script>