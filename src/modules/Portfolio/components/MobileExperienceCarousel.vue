<template>
  <div class="flex flex-col gap-2 w-full mt-7 md:hidden">
    <div
        class="flex items-center  relative transition overflow-x-scroll parent"
        role="tablist"
    >
      <div class="absolute w-32 indicator h-[2px] z-10 my-auto bottom-0 left-0 rounded-full bg-green shadow-md"/>
      <button
          v-for="place in places"
          :id="place.id"
          :key="place.id"
          :aria-controls="place.name"
          :class="[state.selectedWorkplaceID === place.id ? 'bg-light-navy': ' border-light-navy']"
          class="relative block h-10 px-6 tab  whitespace-nowrap transition duration-[400ms] border-b-2"
          role="tab"
          @click="state.selectedWorkplaceID = place.id">
        <span class="text-lightest-slate">{{ place.name }}</span>
      </button>
    </div>
    <div class="flex flex-col text-lightest-slate px-6">
      <p class="font-medium xxl">
        {{ selectedPlaceDetails.position }}
        <span class="text-green md">@ {{ selectedPlaceDetails.name }}</span>
      </p>
      <p class="xs text-light-slate">{{ selectedPlaceDetails.duration }}</p>
      <div class="flex flex-col gap-4 w-full py-4">
        <div
            v-for="(role, index) in selectedPlaceDetails.roles"
            class="flex w-full gap-2 flex-shrink-0 items-start">
          <svg
              class="text-green w-3 h-7"
              fill="currentColor"
              viewBox="0 0 16 16"
              xmlns="http://www.w3.org/2000/svg">
            <path
                d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"/>
          </svg>
          <p class="md w-full">{{role}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import {computed, onMounted, reactive} from "vue";
import {places} from "@/shared/data/placesWorked.js";

const state = reactive({
  selectedWorkplaceID: places[0].id,
  indicator: "",
  tabs: "",
  panels: ""
})


const selectedPlaceDetails = computed(() =>
    places.find(item => item.id === state.selectedWorkplaceID)
)

onMounted(() => {
  state.tabs = document.querySelectorAll(".tab")
  state.indicator = document.querySelector(".indicator")
  state.panels = document.querySelectorAll(".tab-panel")

  state.indicator.style.width = state.tabs[0].getBoundingClientRect().width + 'px'
  state.indicator.style.left = state.tabs[0].getBoundingClientRect().left - state.tabs[0].parentElement.getBoundingClientRect().left + 'px'


  state.tabs.forEach(tab => {

    tab.addEventListener('click', () => {
      state.indicator.style.width = tab.getBoundingClientRect().width + 'px'
      state.indicator.style.left = tab.offsetLeft + 'px'

      let tabTarget = tab.getAttribute("aria-controls")

      state.panels.forEach(panel => {
        let panelId = panel.getAttribute("id")

        if (tabTarget === panelId) {
          panel.classList.remove("invisible", "opacity-0")
          panel.classList.add("visible", 'opacity-100')
        } else {
          panel.classList.add("invisible", 'opacity-0')
        }

      })
    })
  })


})


</script>

<style scoped>
.indicator {
  transition: left .4s;
}
</style>
