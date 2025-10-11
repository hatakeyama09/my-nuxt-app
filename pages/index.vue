<template>
    <MainVisual />
    <Greeting />
    <Career />
    <Hobbies />
</template>

<script setup>
import MainVisual from '~/features/home/MainVisual.vue';
import Greeting from '~/features/home/Greeting.vue';
import Career from '~/features/home/Career.vue';
import Hobbies from '~/features/home/Hobbies.vue';
</script>

<style scoped>
    section {
        margin: 60px auto; /* 上下に余白 */
        max-width: 800px;  /* 横幅を整える */
        padding: 0 20px;   /* スマホでも見やすく */
    }
</style>