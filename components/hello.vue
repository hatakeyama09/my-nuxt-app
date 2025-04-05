<template>
    <div>
        宛先：{{ name }}
        件名：{{ messeage }}
    </div>
</template>

<script setup lang="ts">
    const props = defineProps<{
        name: string
        messeage: string
    }>()
</script>