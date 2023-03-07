<template>
  <div class="min-h-[80vh] flex items-center bg-gradient-to-br from-purple-200 to-indigo-400 my-20 py-20">
    <div class="max-w-3xl mx-auto px-8 sm:px-0">
      <div class="sm:w-7/12 sm-mx-auto">
        <div
            aria-label="tabs"
            class="relative w-max mx-auto h-12 grid grid-cols-3 items-center px-[3px] rounded-full
            overflow-hidden shadow-2xl shadow-900/200 transition"
            role="tablist">
          <div class="absolute w-32 indicator h-1 my-auto bottom-0 left-0 rounded-full bg-green shadow-md"/>
          <button
              @click="state.selectedTabId= 'tab-1'"
              id="tab-1"
              aria-controls="panel-1"
              aria-selected="true"
              class="relative block h-10 px-6 tab rounded-full"
              role="tab"
              tabindex="0"
          >
            <span class="text-gray-800">First Tab</span>
          </button>
          <button
              @click="state.selectedTabId= 'tab-2'"
              id="tab-2"
              aria-controls="panel-2"
              aria-selected="true"
              class="relative block h-10 px-6 tab rounded-full"
              role="tab"
             tabindex="-1"
          >
            <span class="text-gray-800">Second Tab</span>
          </button>
          <button
              @click="state.selectedTabId= 'tab-1'"
              id="tab-3"
              aria-controls="panel-3"
              aria-selected="true"
              class="relative block h-10 px-6 tab rounded-full"
              role="tab"
              tabindex="-1"
          >
            <span class="text-gray-800">Third Tab</span>
          </button>
        </div>
      </div>
      <div class="relative mt-6 rounded-3xl bg-purple-50">
        <div
            id="panel-1"
            class="tab-panel p-6 transition duration-300"
            role="tabpanel">
          <h2 class="text-xl font-semibold text-gray-800">First tab panel</h2>
          <p class="text-gray-600 mt-4">Lorem ipsum dolor sit amet consectur adip</p>
        </div>
        <div
            id="panel-2"
            class="absolute top-0 invisible opacity-0 tab-panel p-6 transition duration-300"
            role="tabpanel">
          <h2 class="text-xl font-semibold text-gray-800">Second tab panel</h2>
          <p class="text-gray-600 mt-4">Lorem ipsum dolor sit amet consectur adip</p>
        </div>
        <div
            id="panel-3"
            class="absolute top-0 invisible opacity-0 tab-panel p-6 transition duration-300"
            role="tabpanel">
          <h2 class="text-xl font-semibold text-gray-800">Third tab panel</h2>
          <p class="text-gray-600 mt-4">Lorem ipsum dolor sit amet consectur adip</p>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>

import {onMounted, reactive} from "vue";

const state = reactive({
  selectedTabId: ""
})


onMounted(() => {
  let tabs = document.querySelectorAll(".tab")
  let indicator = document.querySelector(".indicator")
  let panels = document.querySelectorAll(".tab-panel")


  indicator.style.width = tabs[0].getBoundingClientRect().width + 'px'
  indicator.style.left = tabs[0].getBoundingClientRect().left - tabs[0].parentElement.getBoundingClientRect().left + 'px'


  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      indicator.style.width = tab.getBoundingClientRect().width + 'px'
      indicator.style.left = tab.getBoundingClientRect().left - tab.parentElement.getBoundingClientRect().left + 'px'

      let tabTarget = tab.getAttribute("aria-controls")

      panels.forEach(panel =>{
        let panelId = panel.getAttribute("id")

        if(tabTarget === panelId){
          panel.classList.remove("invisible", "opacity-0")
          panel.classList.add("visible", 'opacity-100')
        }
        else{
          panel.classList.add("invisible", 'opacity-0')
        }

      })
    })
  })


})

</script>

<style scoped>
.indicator{
  transition:  left .4s;
}
</style>