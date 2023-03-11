<template>
  <div class=" flex flex-col pt-32 md:pt-0 gap-2 w-full">
    <p class="text-green sm">Hi, my name is</p>
    <p class="text-lightest-slate name font-semibold leading-[1.1]">Pius Kariuki.</p>
    <p class="text-slate by-line font-light leading-none my-6 w-full">I build things for the web.</p>
    <p class="text-slate md mt-3">
      I’m a software engineer specializing in building exceptional digital
      experiences. Currently, I’m focused on building accessible healthcare platforms products at
      <span class="text-green">Welz.</span>
    </p>
    <a
        href="mailto:piuskariuki19@gmail.com"
        class="cta mt-12  py-[0.75rem] w-44 flex items-center justify-center">Reach out!</a>
  </div>
</template>

<script setup></script>

<style>
.name{
  font-size: clamp(40px, 8vw, 80px);
}

.by-line{
  font-size: clamp(40px, 8vw, 80px);
}
</style>
