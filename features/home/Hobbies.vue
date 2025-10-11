<template>
  <section>
    <SectionTitle>趣味</SectionTitle>
    <div class="hobbies-container">
      <HobbyCard
        v-for="(hobby, index) in hobbies"
        :key="index"
        :name="hobby.name"
        :image="hobby.image"
      />
    </div>
  </section>
</template>

<script setup>
import SectionTitle from "~/components/SectionTitle.vue";
import HobbyCard from "~/components/HobbyCard.vue";

const hobbies = [
  { name: "音楽", image: "/images/music.jpg" },
  { name: "ゲーム", image: "/images/game.jpg" },
  { name: "辛い物を食べる", image: "/images/spicy.jpg" },
];
</script>

<style scoped>
.hobbies-container {
  display: flex;         /* 横並びにする */
  gap: 36px;             /* カード同士の間隔 */
  justify-content: center; /* 中央寄せ */
  flex-wrap: wrap;       /* 画面が狭い時は折り返す */
}
</style>
