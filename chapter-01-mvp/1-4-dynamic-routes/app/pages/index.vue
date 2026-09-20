<script setup>
const examples = [
  { chapter: 1, lesson: 2, label: 'Chapter 1 / Lesson 2' },
  { chapter: 1, lesson: 4, label: 'Chapter 1 / Lesson 4' },
  { chapter: 2, lesson: 1, label: 'Chapter 2 / Lesson 1' },
]
</script>

<template>
  <section class="intro">
    <p class="eyebrow">LESSON 1-4 / DYNAMIC ROUTES</p>
    <h1>One page, many course lessons.</h1>
    <p>Dynamic segments let the same page render any chapter and lesson from the URL parameters.</p>
    <div class="route-list">
      <NuxtLink v-for="example in examples" :key="`${example.chapter}-${example.lesson}`" :to="`/courses/${example.chapter}/lessons/${example.lesson}`">
        <span>{{ example.label }}</span>
        <strong>/courses/{{ example.chapter }}/lessons/{{ example.lesson }} ↗</strong>
      </NuxtLink>
    </div>
  </section>
</template>

<style scoped>
.intro { padding: 12vh 0; max-width: 760px; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h1 { font-size: clamp(42px, 8vw, 84px); line-height: .95; font-weight: 500; }
p:not(.eyebrow) { color: #65716c; font-size: 20px; line-height: 1.5; }
.route-list { display: grid; gap: 0; margin-top: 44px; border-top: 1px solid #cdd4c8; }
.route-list a { display: grid; gap: 8px; padding: 20px 0; border-bottom: 1px solid #cdd4c8; }
.route-list span { color: #65716c; }
.route-list strong { color: #536c20; font: 13px ui-monospace, monospace; font-weight: 400; }
</style>
