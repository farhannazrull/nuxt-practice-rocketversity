<template>
  <section class="lesson-display">
    <p class="eyebrow">LESSON DISPLAY CHILD PAGE</p>
    <h2>Select a lesson to view its content.</h2>
    <p>This component is rendered inside the Chapter 01 parent route through <code>&lt;NuxtPage /&gt;</code>.</p>
  </section>
</template>

<style scoped>
.lesson-display { margin-top: 56px; padding: 28px; background: #e4e9d9; border-left: 4px solid #c8f169; }
.eyebrow { color: #607d29; font: 700 12px ui-monospace, monospace; letter-spacing: .12em; }
h2 { font-size: 32px; font-weight: 500; }
p:not(.eyebrow) { color: #65716c; line-height: 1.5; }
code { color: #536c20; }
</style>
