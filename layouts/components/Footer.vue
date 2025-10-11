<template>
  <footer class="footer">
    <div class="footer-left">© 2025 hatakeyama.mitsuhito</div>
    <div class="footer-right">
      <nav class="footer-nav">
        <a href="/">Home</a>
        <a href="/blog">Blogs</a>
        <a href="/repos">Repos</a>
      </nav>
    </div>
  </footer>
</template>

<style lang="css" scoped>
.footer {
  align-items: center;
  background-color: #edf9fa;
  border-top: 1px solid #ddd;
  bottom: 0;
  display: flex;
  font-size: 16px;
  justify-content: space-between;
  padding-bottom: 10px;
  padding-top: 10px;
  position: fixed;
  width: 100%;
  z-index: 1000;
}

.footer-left {
  margin-left: 20px;
  text-align: left;
}

.footer-right {
  display: flex;
  margin-right: 20px;
  text-align: right;
}

.footer-nav {
  display: flex;
  gap: 20px;
}

.footer-nav a {
  color: #333;
  margin-left: 15px;
  text-decoration: none;
}

.footer-nav a:hover {
  text-decoration: underline;
}
</style>
