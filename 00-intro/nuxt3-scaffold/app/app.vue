<script setup>
const prerequisites = [
  {
    number: '01',
    title: 'Node.js 22.x atau active LTS',
    description: 'Runtime untuk menjalankan Nuxt dan package manager npm.',
    command: 'node --version',
  },
  {
    number: '02',
    title: 'VS Code + Vue extension',
    description: 'Gunakan official Vue extension (Volar) untuk dukungan Vue dan Nuxt.',
    command: 'code --version',
  },
  {
    number: '03',
    title: 'Terminal',
    description: 'Jalankan perintah create, install, development, dan build dari terminal.',
    command: 'npm --version',
  },
]
</script>

<template>
  <div class="page-shell">
    <NuxtRouteAnnouncer />

    <header class="topbar">
      <a class="brand" href="/" aria-label="Nuxt hands-on home">
        <span class="brand-mark">N</span>
        <span>nuxt-practice</span>
      </a>
      <span class="version-pill">Nuxt 4 · JavaScript</span>
    </header>

    <main class="content">
      <section class="hero">
        <p class="eyebrow">COURSE / JAVASCRIPT FRAMEWORK</p>
        <h1>Mulai membangun dengan <em>Nuxt</em>.</h1>
        <p class="hero-copy">
          Hands-on singkat dari bagian Installation: siapkan tools, pilih cara mencoba,
          lalu jalankan project Nuxt pertamamu.
        </p>
        <div class="hero-actions">
          <a class="button button-primary" href="https://stackblitz.com/github/nuxt/starter?file=app%2Fapp.vue" target="_blank" rel="noreferrer">
            Coba di StackBlitz <span aria-hidden="true">↗</span>
          </a>
          <a class="text-link" href="https://nuxt.com/docs/4.x/getting-started/installation" target="_blank" rel="noreferrer">
            Buka dokumentasi resmi
          </a>
        </div>
      </section>

      <section class="workspace-grid" aria-label="Installation hands-on">
        <div class="section-heading">
          <p class="eyebrow">01 / CHECKLIST</p>
          <h2>Siapkan lingkungan kerja</h2>
        </div>
        <div class="checklist">
          <article v-for="item in prerequisites" :key="item.number" class="check-item">
            <span class="item-number">{{ item.number }}</span>
            <div>
              <h3>{{ item.title }}</h3>
              <p>{{ item.description }}</p>
              <code>{{ item.command }}</code>
            </div>
          </article>
        </div>
      </section>

      <section class="terminal-panel">
        <div class="section-heading section-heading-light">
          <p class="eyebrow">02 / TERMINAL</p>
          <h2>Buat project lokal</h2>
        </div>
        <div class="terminal-window">
          <div class="terminal-bar"><span></span><span></span><span></span><small>zsh · nuxt-practice</small></div>
          <pre><code><span class="prompt">$</span> npm create nuxt@latest my-nuxt-app
<span class="prompt">$</span> cd my-nuxt-app
<span class="prompt">$</span> npm run dev -- -o</code></pre>
        </div>
        <p class="terminal-note">Aplikasi akan tersedia di <strong>http://localhost:3000</strong>.</p>
      </section>
    </main>

    <footer>
      <span>Part: Javascript Framework · Nuxt 3</span>
      <a href="https://nuxt.com" target="_blank" rel="noreferrer">nuxt.com ↗</a>
    </footer>
  </div>
</template>

<style>
:root {
  --ink: #18221f;
  --muted: #65716c;
  --paper: #f3f1e9;
  --lime: #c8f169;
  --line: #d9ddd3;
  --night: #17231f;
}

* { box-sizing: border-box; }
body { margin: 0; color: var(--ink); background: var(--paper); font-family: Georgia, 'Times New Roman', serif; }
a { color: inherit; }
.page-shell { min-height: 100vh; overflow: hidden; background: radial-gradient(circle at 80% 0%, #e2e7d7 0, transparent 33%), var(--paper); }
.topbar, .content, footer { width: min(1120px, calc(100% - 48px)); margin: 0 auto; }
.topbar { display: flex; justify-content: space-between; align-items: center; padding: 28px 0; border-bottom: 1px solid var(--line); font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: 12px; letter-spacing: .04em; }
.brand { display: flex; align-items: center; gap: 10px; text-decoration: none; font-weight: 700; }
.brand-mark { display: grid; place-items: center; width: 28px; height: 28px; color: var(--night); background: var(--lime); font-weight: 900; border-radius: 50%; }
.version-pill { color: var(--muted); }
.hero { max-width: 790px; padding: 112px 0 100px; }
.eyebrow { margin: 0 0 18px; color: #78836e; font: 700 11px/1.2 ui-monospace, SFMono-Regular, Menlo, monospace; letter-spacing: .14em; }
h1, h2, h3, p { margin-top: 0; }
h1 { max-width: 760px; margin-bottom: 24px; font-size: clamp(48px, 8vw, 92px); line-height: .94; font-weight: 500; letter-spacing: 0; }
h1 em { color: #607d29; font-style: normal; }
.hero-copy { max-width: 560px; color: var(--muted); font-size: 20px; line-height: 1.45; }
.hero-actions { display: flex; align-items: center; gap: 28px; margin-top: 38px; font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: 13px; }
.button { padding: 14px 18px; text-decoration: none; border: 1px solid var(--ink); }
.button-primary { color: var(--night); background: var(--lime); box-shadow: 4px 4px 0 var(--ink); }
.text-link { text-underline-offset: 5px; }
.workspace-grid { display: grid; grid-template-columns: .8fr 1.2fr; gap: 80px; padding: 42px 0 96px; border-top: 1px solid var(--line); }
h2 { font-size: clamp(32px, 4vw, 52px); line-height: 1; font-weight: 500; }
.checklist { display: grid; gap: 0; }
.check-item { display: grid; grid-template-columns: 46px 1fr; gap: 18px; padding: 22px 0; border-top: 1px solid var(--line); }
.check-item:first-child { padding-top: 0; border-top: 0; }
.item-number { color: #809347; font: 700 12px ui-monospace, SFMono-Regular, Menlo, monospace; }
h3 { margin-bottom: 7px; font-size: 21px; font-weight: 500; }
.check-item p { margin-bottom: 12px; color: var(--muted); line-height: 1.45; }
code { padding: 4px 7px; color: #536c20; background: #e4e9d9; font: 12px ui-monospace, SFMono-Regular, Menlo, monospace; }
.terminal-panel { display: grid; grid-template-columns: .8fr 1.2fr; gap: 80px; padding: 76px 56px; color: #e9f0df; background: var(--night); }
.section-heading-light .eyebrow { color: var(--lime); }
.section-heading-light h2 { color: #f4f7e9; }
.terminal-window { overflow: hidden; background: #0e1714; border: 1px solid #405048; box-shadow: 14px 14px 0 #36453a; }
.terminal-bar { display: flex; align-items: center; gap: 6px; padding: 13px 16px; border-bottom: 1px solid #293830; }
.terminal-bar span { width: 8px; height: 8px; border-radius: 50%; background: #788b7b; }
.terminal-bar small { margin-left: 8px; color: #819187; font: 11px ui-monospace, SFMono-Regular, Menlo, monospace; }
pre { margin: 0; padding: 25px 22px; overflow-x: auto; font: 14px/2 ui-monospace, SFMono-Regular, Menlo, monospace; }
pre code { padding: 0; color: #dce9c8; background: transparent; font: inherit; }
.prompt { color: var(--lime); }
.terminal-note { grid-column: 2; margin: 26px 0 0; color: #aab7aa; font: 13px ui-monospace, SFMono-Regular, Menlo, monospace; }
.terminal-note strong { color: var(--lime); font-weight: 400; }
footer { display: flex; justify-content: space-between; padding: 30px 0 40px; color: var(--muted); font: 11px ui-monospace, SFMono-Regular, Menlo, monospace; }
footer a { color: var(--ink); }
@media (max-width: 720px) {
  .topbar, .content, footer { width: min(100% - 32px, 560px); }
  .topbar { align-items: flex-start; gap: 16px; }
  .version-pill { text-align: right; }
  .hero { padding: 74px 0 70px; }
  .hero-actions, footer { align-items: flex-start; flex-direction: column; gap: 18px; }
  .workspace-grid, .terminal-panel { grid-template-columns: 1fr; gap: 36px; }
  .terminal-panel { padding: 50px 24px; margin: 0 -16px; }
  .terminal-note { grid-column: auto; }
}
</style>
