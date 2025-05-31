<template>
  <header class="self-introduction-header">
    <div class="header-contents">
      <h1>自己紹介</h1>
      <nav class="menu-item">
        <ul>
          <li><NuxtLink class="header-link" to="/">Home</NuxtLink></li>
          <li><NuxtLink class="header-link" to="/blog">Blogs</NuxtLink></li>
          <li><NuxtLink class="header-link" to="/repos">Repos</NuxtLink></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="css" scoped>

.self-introduction-header {
  background-color: #edf9fa;
  display: flex;
  justify-content: center;
}

.header-contents {
  align-items: center;
  display: flex;
  justify-content: space-between;
  max-width: 767px;
  padding: 0 20px;
  width: 100%;
}

.menu-item {
  display: flex;
  gap: 20px;
}

.menu-item ul {
  display: flex;
  gap: 20px;
  list-style: none;       /* 黒丸を消す */
  margin: 0;
  padding: 0;              /* ブラウザのデフォルト余白を削除 */
}

.header-link {
  background-color: transparent;
  border: 1px solid transparent;
  border-radius: 6px;
  color: #333;
  display: inline-block;
  padding: 8px 16px;
  text-decoration: none;
  transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
}

.header-link:hover {
  background-color: #00bcd4;
  border-color: #00bcd4;
  color: #ffffff;
}

.header-link.router-link-exact-active {
  background-color: #00bcd4;
  border-color: #00bcd4;
  color: #fff;
}

</style>
