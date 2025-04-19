<script setup lang="ts">
import Header from "~/layouts/header.vue";
</script>

<template>
  <div>
    <NuxtLayout>
      <Header />
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style lang="css">
body {
  margin: 0 !important; 
  padding: 0;
}
</style>
