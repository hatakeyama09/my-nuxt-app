<template>
  <section>
    <!-- 画像は /public/images/my-icon.png に置く -->
    <ProfileIcon
      src="/images/my-icon.png"
      alt="畠山 光人 のアイコン"
      name="畠山 光人"
      :size="180"
    />
  </section>
</template>

<script setup>
import ProfileIcon from "~/components/ProfileIcon.vue";
</script>
