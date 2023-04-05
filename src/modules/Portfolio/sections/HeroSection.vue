<template>
  <div class=" flex flex-col pt-32 md:pt-0 gap-2 w-full min-h-full">
    <p class="text-green paragraph">Hi, my name is</p>
    <p class="text-lightest-slate name font-semibold leading-[1.1]">Pius Kariuki.</p>
    <p class="text-slate h2 my-6 w-full">I am a software engineer.</p>
    <p class="text-lightest-slate paragraph  mt-3 lg:w-10/12">
      I’m currently building and maintaining accessible
      healthcare platforms at
      <span class="text-green">Welz.</span>
    </p>
    <a
        :href="emailAddress"
        class="cta mt-12 lg:mt-auto justify-self-end py-[0.75rem] w-44 flex items-center justify-center">Reach out!</a>
  </div>
</template>

<script setup>
const emailAddress = import.meta.env.VITE_EMAIL
</script>

<style>
.name{
  font-size: clamp(40px, 8vw, 80px);
}

.by-line{
  font-size: clamp(40px, 8vw, 80px);
}
</style>
