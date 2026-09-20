<template>
  <section class="hero">
    <p class="eyebrow">LESSON 1-2 / FILE-BASED ROUTING</p>
    <h1>Build a course lesson catalog.</h1>
    <p>Nuxt maps files in the pages directory to routes. This home page is the starting point for the course.</p>
    <NuxtLink class="button" to="/lessons">View lessons</NuxtLink>
  </section>
</template>

<style scoped>
.hero { padding: 15vh 0; max-width: 680px; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h1 { font-size: clamp(42px, 8vw, 84px); line-height: .95; font-weight: 500; }
p:not(.eyebrow) { color: #65716c; font-size: 20px; line-height: 1.5; }
.button { display: inline-block; margin-top: 20px; padding: 14px 18px; color: #17231f; background: #c8f169; border: 1px solid #17231f; text-decoration: none; }
</style>
