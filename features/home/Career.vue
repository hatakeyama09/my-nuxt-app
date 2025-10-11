<template>
  <section class="career">
    <SectionTitle>経歴</SectionTitle>
    <div class="timeline">
      <div v-for="(item, index) in careers" :key="index" class="timeline-item">
        <div class="timeline-year">
          {{ item.year }}<br />
          <span class="timeline-month">{{ item.month }}</span>
        </div>
        <div class="timeline-content">
          <p>{{ item.event }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import SectionTitle from "~/components/SectionTitle.vue";

const careers = [
  { year: "2022年", month: "3月", event: "岩手県立花北青雲高等学校 卒業" },
  { year: "2022年", month: "4月", event: "MCL盛岡情報ビジネス&デザイン専門学校 入学" },
  { year: "2024年", month: "3月", event: "MCL盛岡情報ビジネス&デザイン専門学校 卒業" },
  { year: "2024年", month: "4月", event: "クラリスアート株式会社 入社" },
];
</script>

<style scoped>
.career {
  padding: 20px 0;
}

.timeline {
  position: relative;
  margin-left: 40px;
  padding-left: 20px;
  border-left: 3px solid #007acc; /* 青い棒 */
  margin-top: 30px;
}

.timeline-item {
  position: relative;
  margin-bottom: 30px;
}

.timeline-year {
  position: absolute;
  left: -140px;
  width: 100px;
  text-align: right;
  font-weight: bold;
  color: #007acc;
  padding-right: 10px;
  line-height: 1.2;
}

.timeline-month {
  font-size: 0.9em;
  font-weight: normal;
  color: #555;
}

.timeline-content {
  background: #f9f9f9;
  padding: 12px 16px;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}
</style>
