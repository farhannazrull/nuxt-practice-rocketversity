<template>
  <div class="app-shell">
    <header class="site-header">
      <NuxtLink to="/" class="brand">Nuxt Course</NuxtLink>
      <nav>
        <NuxtLink to="/lessons">Lessons</NuxtLink>
      </nav>
    </header>
    <main>
      <NuxtPage />
    </main>
  </div>
</template>

<style>
:root { color: #17231f; background: #f3f1e9; font-family: Georgia, serif; }
body { margin: 0; }
.app-shell { min-height: 100vh; }
.site-header { display: flex; justify-content: space-between; padding: 24px 6vw; border-bottom: 1px solid #d9ddd3; font-family: ui-monospace, monospace; }
.site-header a { color: inherit; text-decoration: none; }
.brand { font-weight: 700; }
nav { display: flex; gap: 18px; }
main { width: min(960px, 88vw); margin: 0 auto; }
</style>
