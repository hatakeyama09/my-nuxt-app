<template>
  <h2 class="section-title">
    <slot />
  </h2>
</template>

<script setup>
// 特にロジックがなければ空でOK
</script>

<style scoped>
.section-title {
  margin-bottom: 16px;
  font-size: 1.5rem;
  font-weight: bold;
  border-left: 4px solid #007acc;
  padding-left: 8px;
}
</style>
