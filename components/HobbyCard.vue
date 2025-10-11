<template>
  <div class="hobby-card">
    <img :src="image" :alt="name" class="hobby-image" />
    <p class="hobby-name">{{ name }}</p>
  </div>
</template>

<script setup>
defineProps({
  image: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
.hobby-card {
  text-align: center;
}

.hobby-image {
  width: 150px;
  height: 150px;
  background-color: aqua; /* 仮の背景 */
  object-fit: cover;
}

.hobby-name {
  margin-top: 8px;
  font-weight: bold;
}
</style>
