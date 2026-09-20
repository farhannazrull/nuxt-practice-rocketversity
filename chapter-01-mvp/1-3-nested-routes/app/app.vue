<template>
  <div class="app-shell">
    <header class="site-header">
      <NuxtLink to="/" class="brand">Nuxt Course / Nested Routes</NuxtLink>
      <NuxtLink to="/chapters/1">Chapter 01</NuxtLink>
    </header>
    <main><NuxtPage /></main>
  </div>
</template>

<style>
:root { color: #17231f; background: #f3f1e9; font-family: Georgia, serif; }
body { margin: 0; }
.app-shell { min-height: 100vh; }
.site-header { display: flex; justify-content: space-between; gap: 24px; padding: 24px 6vw; border-bottom: 1px solid #d9ddd3; font: 13px ui-monospace, monospace; }
a { color: inherit; text-decoration: none; }
main { width: min(960px, 88vw); margin: 0 auto; }
</style>
