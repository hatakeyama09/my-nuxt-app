<template>
  <div class="profile-wrap">
    <img
      :src="src"
      :alt="alt"
      class="profile-img"
      :style="imgSizeStyle"
      loading="lazy"
    />
    <p v-if="name" class="profile-name">{{ name }}</p>
  </div>
</template>

<script setup>
import { computed } from "vue";

const props = defineProps({
  src: { type: String, required: true },
  alt: { type: String, default: "プロフィール画像" },
  name: { type: String, default: "" },
  size: { type: [Number, String], default: 140 }, // px または "120px" のように文字列でも可
});

const imgSizeStyle = computed(() => {
  const s = typeof props.size === "number" ? `${props.size}px` : props.size;
  return { width: s, height: s };
});
</script>

<style scoped>
.profile-wrap {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 40px; /* 上の余白 */
}

/* 丸く表示するスタイル */
.profile-img {
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #ffffff; /* 白い枠 */
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.12);
  background-color: #f2f2f2;
}

/* 名前（任意表示） */
.profile-name {
  margin-top: 12px;
  font-weight: 600;
  font-size: 1rem;
  color: #222;
}

/* モバイル時に自動で少し小さくする */
@media screen and (max-width: 767px) {
  .profile-wrap { margin-top: 20px; }
  .profile-img { width: 100px !important; height: 100px !important; }
}
</style>
