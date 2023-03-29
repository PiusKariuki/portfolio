<template>
    <iframe
        class="w-screen h-screen"
        id="resume"
        :src="resume"
        title="RESUME"
 >
    </iframe>
</template>

<script setup>
import resume from "../../../../public/docs/resume.pdf"
</script>
