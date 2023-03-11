<template>
  <div id="projects" class="content-container flex flex-col gap-6 mt-16 w-full">
    <heading class="max-w-6xl" number="02" text="Some Things I've Built"/>
    <div class="flex flex-col w-full gap-24 md:gap-44 items-center py-12 ">

      <div
          v-for="(item, index) in projects"
          :key="item.link"
          class="flex flex-col relative w-full max-w-6xl">
        <img
            :src="item.image"
            alt=""
            :class="[index % 2 == 0 ? 'md:left-[66.66%]' : 'md:left-[33.33%]']"
            class="absolute top-[13%] -translate-y-1/2 h-[40%] md:h-[400px] max-w-[90%] rounded-2xl left-1/2
             -translate-x-1/2 object-cover z-10 bg-lightest-navy md:w-8/12 md:top-1/2 md:-z-10 "
        >
        <div
            :class="[index % 2 == 0 ? '' : 'md:self-end md:items-end']"
            class="flex flex-col gap-4 text-lightest-slate bg-lightest-navy md:bg-transparent w-full
             md:w-8/12 px-4 pb-8 pt-[55%] md:pt-0 rounded-2xl">
          <p class="xs text-green">Featured Project</p>
          <p class="xxl font-bold tracking-wide text-white hover:text-green cursor-pointer -mt-3">{{item.name}}</p>
          <div
              :class="[index % 2 == 0? 'md:pr-[10%]' : 'md:text-right md:pl-[10%]']"
              class="md:bg-light-navy md:px-4 md:py-8 md:rounded-lg md:lg">
            {{item.desc}}
          </div>
          <div
              :class="[index % 2 == 0 ? 'md:pr-[50%]' : 'md:pl-[48%] text-right justify-end']"
              class="flex flex-wrap items-center gap-x-4 gap-y-1 my-2">
            <p
                v-for="(tech, index) in item.technologies"
                :key="index"
                class="lg text-white ">{{ tech }}</p>
          </div>
          <a
              target="_blank"
              :href="item.link">
            <svg
                class="h-6 w-6 cursor-pointer text-green"
                aria-hidden="true" fill="none" stroke="currentColor" stroke-width="2.0" viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg">
              <path
                  d="M13.5 6H5.25A2.25 2.25 0 003 8.25v10.5A2.25 2.25 0 005.25 21h10.5A2.25 2.25 0 0018 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25"
                  stroke-linecap="round"
                  stroke-linejoin="round"></path>
            </svg>
          </a>

        </div>

      </div>


    </div>
  </div>
</template>

<script setup>
import Heading from "@/shared/components/Heading.vue";
import {projects} from "@/shared/data/projects.js";
</script>