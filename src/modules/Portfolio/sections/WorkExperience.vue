<template>
  <div class="content-container flex flex-col gap-6 my-20 lg:my-32 md:items-center">
    <heading number="02" text="Where I've Worked"/>
    <mobile-experience-carousel v-if="isMobile"/>
    <desktop-experience-carousel v-if="!isMobile"/>
  </div>
</template>

<script setup>
import Heading from "@/shared/components/Heading.vue";
import MobileExperienceCarousel from "@/modules/Portfolio/components/MobileExperienceCarousel.vue";
import DesktopExperienceCarousel from "@/modules/Portfolio/components/DesktopExperienceCarousel.vue";
import {computed} from "vue";


const isMobile = computed(()=>window.innerWidth < 768)
</script>


