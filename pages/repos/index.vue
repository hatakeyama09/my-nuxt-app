<template>
    <ReposList />
</template>

<script setup>
import ReposList from '~/features/repos/ReposList.vue';
</script>

<style scoped>
    section {
        margin: 60px auto; /* 上下に余白 */
        max-width: 800px;  /* 横幅を整える */
        padding: 0 20px;   /* スマホでも見やすく */
    }
</style>