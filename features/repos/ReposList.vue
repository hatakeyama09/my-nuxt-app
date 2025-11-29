<template>
    <section>
        <SectionTitle>リポジトリ</SectionTitle>
        <div class="repos-list">
            <!-- リストを展開 -->
            <ReposCard
                v-for="(repo, index) in reposList"
                :key="index"
                :image="repo.image"
                :title="repo.title"
                :date="repo.date"
                :content="repo.content"
                :repo-name="repo.repoName"
                :repo-url="repo.repoUrl"
            />
        </div>
    </section>
</template>

<script setup>
import SectionTitle from '~/components/SectionTitle.vue';
import ReposCard from '~/components/ReposCard.vue';

// githubのリポジトリ情報を取得
const res = await fetch('https://api.github.com/users/hatakeyama09/repos');

const data = await res.json();

const reposList = [
    {
        image: "/images/self-introduction-site.png",
        title: "自己紹介サイト作成",
        date: "2025/10/25",
        content: "自己紹介サイトを作成しました！\nWeb開発の学習成果をまとめるためです。\n主にVueやCSSを使用しています。\n元々デザインがあまり得意ではないので、\n今回は統一感を持たせられるように意識して作成しました。",
        repoName: data[0].name,
        repoUrl: data[0].html_url
    }
]
</script>

<style scoped>
.repos-list {
  display: flex;              /* 縦並びでもOK */
  flex-direction: column;     /* カードを縦に並べる */
  gap: 1.5rem;                /* ← カード間の間隔を設定（例：24px） */
  margin-top: 1.5rem;         /* タイトルとの間隔 */
}
</style>