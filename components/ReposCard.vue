<template>
  <article class="repo-card">
    <img :src="image" :alt="title" class="repo-image" />

    <!-- タイトル + GitHubリンク -->
    <h3 class="repo-title">
      {{ title }}
    </h3>

    <!-- リポジトリ名（リンク付き） -->
    <p class="repo-link">
      <a :href="repoUrl" target="_blank" rel="noopener noreferrer">
        {{ repoName }}
      </a>
    </p>

    <p class="repo-date">{{ date }}</p>
    <p class="repo-content">{{ content }}</p>
  </article>
</template>

<script setup>
defineProps({
  image: String,
  title: String,
  date: String,
  content: String,

  // 追加分
  repoName: String,
  repoUrl: String
});
</script>

<style scoped>
.repo-card {
  background-color: #f9fafb;
  border-radius: 8px;
  padding: 1rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.08);
  transition: transform 0.2s;
}
.repo-card:hover {
  transform: translateY(-4px);
}
.repo-image {
  width: 100%;
  border-radius: 6px;
  margin-bottom: 0.75rem;
}
.repo-title {
  font-weight: bold;
  margin-bottom: 0.25rem;
}
.repo-link a {
  color: #2563eb;
  text-decoration: none;
  font-size: 0.95rem;
}
.repo-link a:hover {
  text-decoration: underline;
}
.repo-date {
  font-size: 0.9rem;
  color: #888;
  margin-bottom: 0.5rem;
}
.repo-content {
  font-size: 0.95rem;
  line-height: 1.4;
  white-space: pre-line;
}
</style>
