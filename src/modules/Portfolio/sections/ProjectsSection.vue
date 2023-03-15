<template>
  <div id="projects" class="content-container flex flex-col gap-6  w-full ">
    <heading  number="02" text="Featured Projects"/>
    <div class="flex flex-col w-full gap-24 lg:gap-44  py-12 ">

      <div
          v-for="(item, index) in projects"
          :key="item.link"
          class="flex flex-col relative w-full max-w-6xl">
        <div
            :style="{backgroundImage: 'url(' +item.image + ')' }"
            :class="[index % 2 == 0 ? 'lg:left-[65%]' : 'lg:left-[35%]']"
            class="absolute h-[180px] md:h-[380px] w-[87%] md:w-[92%] -top-[20px] md:-top-[30px] -translate-x-1/2 lg:top-1/2 lg:-z-10 lg:w-8/12
            lg:h-[400px] lg:-translate-y-1/2 left-1/2
            bg-cover bg-center rounded-2xl"
        />
          <div
              :class="[index % 2 == 0 ? '' : 'lg:self-end lg:items-end']"
              class="flex flex-col gap-4 text-lightest-slate bg-lightest-navy lg:bg-transparent w-full
             lg:w-8/12 px-4 pb-8 pt-[55%] lg:pt-0 rounded-2xl">
            <p class="xs text-green">Featured Project</p>
            <p class="heading font-bold tracking-wide text-white hover:text-green cursor-pointer -mt-3">
              {{ item.name }}</p>
            <div
                :class="[index % 2 == 0? 'lg:pr-[10%]' : 'lg:text-right lg:pl-[10%]']"
                class="lg:bg-light-navy lg:px-4 lg:py-8 lg:rounded-lg lg:lg leading-loose"
                v-html="item.desc"/>
            <div
                :class="[index % 2 == 0 ? 'lg:pr-[50%]' : 'lg:pl-[48%] lg:text-right lg:justify-end']"
                class="flex flex-wrap items-center gap-x-4 gap-y-1 my-2">
              <p
                  v-for="(tech, index) in item.technologies"
                  :key="index"
                  class="sm text-green font-thin cursor-pointer">{{ tech }}</p>
            </div>
            <a
                :href="item.link"
                target="_blank">
              <svg
                  aria-hidden="true"
                  class="h-6 w-6 cursor-pointer text-green" fill="none" stroke="currentColor" stroke-width="2.0"
                  viewBox="0 0 24 24"
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
import {projects} from "@/shared/data/projects.js";</script>