<template>
  <header class="self-introduction-header">
    <div class="header-contents">
      <h1>自己紹介</h1>
      <div class="menu-item">
        <NuxtLink class="header-link" to="/">Home</NuxtLink>
        <NuxtLink class="header-link" to="/blog">Blogs</NuxtLink>
        <NuxtLink class="header-link" to="/repos">Repos</NuxtLink>
      </div>
    </div>
  </header>
</template>

<script setup></script>

<style scoped>
.self-introduction-header {
  display: flex;
  justify-content: center;
  background-color: #edf9fa;
}

.header-contents {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  width: 100%;
  max-width: 767px;
}

.menu-item {
  display: flex;
  gap: 20px;
  /* margin-right: 20px; */
}

.header-link {
  display: inline-block;
  padding: 8px 16px;
  text-decoration: none;
  color: #333;
  background-color: transparent;
  border: 1px solid transparent;
  border-radius: 6px;
  transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
}

.header-link:hover {
  background-color: #00bcd4;
  color: #ffffff;
  border-color: #00bcd4;
}

.header-link.router-link-exact-active {
  background-color: #00bcd4;
  color: #fff;
  border-color: #00bcd4;
}
</style>
