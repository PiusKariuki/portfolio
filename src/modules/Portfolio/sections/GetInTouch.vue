<template>
  <div id="contact" class="content-container flex flex-col gap-6 justify-center text-center">
    <p class="h1 text-lightest-slate">Get In Touch</p>
    <p class="subtitle text-lightest-slate ">
      Got a question or have a proposal ? Let's chat. 😁
    </p>

    <a
        :href="emailAddress"
        class="cta mt-6  py-[0.75rem] w-44 flex items-center justify-center self-center">Say Hello</a>
  </div>
</template>

<script setup>


import {emailAddress} from "@/shared/data/email.js";
</script>