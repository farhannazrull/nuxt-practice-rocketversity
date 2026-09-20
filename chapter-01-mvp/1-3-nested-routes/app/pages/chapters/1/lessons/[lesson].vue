<script setup>
const route = useRoute()
const lessonTitle = computed(() => `Lesson ${route.params.lesson}`)
</script>

<template>
  <section class="lesson-display">
    <p class="eyebrow">NESTED LESSON ROUTE</p>
    <h2>{{ lessonTitle }}</h2>
    <p>This dynamic child is rendered within the Chapter 01 hierarchy.</p>
  </section>
</template>

<style scoped>
.lesson-display { margin-top: 56px; padding: 28px; background: #e4e9d9; border-left: 4px solid #c8f169; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h2 { font-size: 32px; font-weight: 500; }
p:not(.eyebrow) { color: #65716c; line-height: 1.5; }
</style>
