<script setup>
const lessons = [
  { id: '1-1', title: 'File-based Routing' },
  { id: '1-2', title: 'Displaying Course Lessons' },
  { id: '1-3', title: 'Nested Routes' },
]
</script>

<template>
  <section class="chapter-page">
    <div class="chapter-heading">
      <p class="eyebrow">CHAPTER 01</p>
      <h1>Building Our MVP</h1>
      <p>Chapter-level information lives in this parent route. The child page owns the lesson list.</p>
    </div>
    <NuxtPage />
    <nav class="lesson-nav" aria-label="Chapter lessons">
      <NuxtLink v-for="lesson in lessons" :key="lesson.id" :to="`/chapters/1/lessons/${lesson.id}`">
        <span>{{ lesson.id }}</span>{{ lesson.title }}
      </NuxtLink>
    </nav>
  </section>
</template>

<style scoped>
.chapter-page { padding: 12vh 0; }
.chapter-heading { max-width: 650px; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h1 { margin: 12px 0; font-size: clamp(44px, 8vw, 84px); font-weight: 500; line-height: .95; }
.chapter-heading p:last-child { color: #65716c; font-size: 20px; line-height: 1.5; }
.lesson-nav { display: grid; gap: 0; margin-top: 60px; border-top: 1px solid #cdd4c8; }
.lesson-nav a { display: flex; gap: 24px; padding: 22px 0; border-bottom: 1px solid #cdd4c8; text-decoration: none; }
.lesson-nav span { color: #607d29; font: 700 12px ui-monospace, monospace; }
</style>
