<script setup>
const route = useRoute()

const chapter = computed(() => route.params.chapter)
const lesson = computed(() => route.params.lesson)
const routeLabel = computed(() => `/courses/${chapter.value}/lessons/${lesson.value}`)

useHead(() => ({
  title: `Chapter ${chapter.value}, Lesson ${lesson.value}`,
}))
</script>

<template>
  <section class="lesson-page">
    <p class="eyebrow">DYNAMIC LESSON ROUTE</p>
    <div class="route-badge">{{ routeLabel }}</div>
    <h1>Chapter {{ chapter }} / Lesson {{ lesson }}</h1>
    <p>The values above come from the dynamic <code>[chapter]</code> and <code>[lesson]</code> route segments.</p>
    <NuxtLink class="back-link" to="/">← Try another route</NuxtLink>
  </section>
</template>

<style scoped>
.lesson-page { padding: 16vh 0; max-width: 760px; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
.route-badge { display: inline-block; margin: 24px 0; padding: 10px 12px; color: #536c20; background: #e4e9d9; font: 13px ui-monospace, monospace; }
h1 { margin: 0 0 20px; font-size: clamp(42px, 8vw, 78px); line-height: .95; font-weight: 500; }
p:not(.eyebrow) { color: #65716c; font-size: 20px; line-height: 1.5; }
code { color: #536c20; }
.back-link { display: inline-block; margin-top: 26px; color: #17231f; text-decoration: underline; text-underline-offset: 5px; }
</style>
