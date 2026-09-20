<script setup>
const lessons = [
  { id: '1-1', title: 'File-based Routing', duration: '12 min' },
  { id: '1-2', title: 'Displaying Course Lessons', duration: '18 min' },
  { id: '1-3', title: 'Nested Routes', duration: '15 min' },
]
</script>

<template>
  <section class="lessons-page">
    <p class="eyebrow">CHAPTER 01 / BUILDING OUR MVP</p>
    <h1>Course lessons</h1>
    <div class="lesson-list">
      <article v-for="lesson in lessons" :key="lesson.id" class="lesson-card">
        <span>{{ lesson.id }}</span>
        <div>
          <h2>{{ lesson.title }}</h2>
          <p>{{ lesson.duration }}</p>
        </div>
      </article>
    </div>
  </section>
</template>

<style scoped>
.lessons-page { padding: 12vh 0; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h1 { margin-bottom: 42px; font-size: clamp(42px, 7vw, 76px); font-weight: 500; }
.lesson-list { border-top: 1px solid #cdd4c8; }
.lesson-card { display: grid; grid-template-columns: 80px 1fr; gap: 20px; padding: 24px 0; border-bottom: 1px solid #cdd4c8; }
.lesson-card > span { color: #607d29; font: 700 13px ui-monospace, monospace; }
h2 { margin: 0 0 8px; font-size: 25px; font-weight: 500; }
p { margin: 0; color: #65716c; }
</style>
