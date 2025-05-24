<template>
    <Header />
    <slot />
    <Foorer />
</template>

<script setup>
import Header from './components/header.vue';
import Foorer from './components/foorer.vue';
</script>
