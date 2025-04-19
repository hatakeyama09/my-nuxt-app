<template>
  <header class="self-introduction-header">
    <div class="header-contents">
      <h1>自己紹介</h1>
      <div class="menu-item">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/blog">Blogs</NuxtLink>
        <NuxtLink to="/repos">Repos</NuxtLink>
      </div>
    </div>
  </header>
</template>

<script setup></script>

<style scoped>
.self-introduction-header {
  background-color: #edf9fa;
}

.header-contents {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.menu-item {
  display: flex;
  gap: 20px;
}
</style>
