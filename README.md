# Nuxt Practice Rocketversity

Repository hands-on untuk belajar membangun aplikasi modern dengan Nuxt, mengikuti alur course Rocketversity.

## Struktur Course

- `00-intro/nuxt3-scaffold/` - scaffold Nuxt awal dan setup instalasi.
- `chapter-01-mvp/` - membangun MVP course dengan routing, lesson, video, dan progress.
- `chapter-02-architecture/` - memahami arsitektur Nuxt: app, pages, layouts, components, dan composables.
- `chapter-03-robust/` - TypeScript, error boundary, error server, dan validasi route.
- `chapter-04-middleware-auth/` - middleware route, login, Supabase, OAuth, dan proteksi route.
- `chapter-05-server-routes/` - server routes, fetching, Prisma, database, dan Nitro/h3.
- `chapter-06-pinia/` - state management dan progress user dengan Pinia.
- `chapter-07-sales-page/` - sales page, static generation, Stripe, webhook, dan grant access.
- `course-2-nuxt2-vuejs/` - dasar JavaScript, DOM, ES6, Nuxt 2, dan Vue.js.

Setiap folder lesson disiapkan sebagai checkpoint mandiri. Implementasi lesson dapat ditambahkan tanpa mengganggu checkpoint lain.

## Menjalankan Scaffold Intro

```bash
cd 00-intro/nuxt3-scaffold
npm install
npm run dev -- -o
```

Buka `http://localhost:3000` di browser.

## Prerequisites

- Node.js `22.x` atau active LTS.
- Visual Studio Code dengan [official Vue extension](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (Volar).
- Terminal untuk menjalankan perintah Nuxt.

Alternatif tanpa instalasi lokal tersedia melalui [Nuxt StackBlitz](https://stackblitz.com/github/nuxt/starter?file=app%2Fapp.vue).

## Referensi

- [Nuxt Installation](https://nuxt.com/docs/4.x/getting-started/installation)
- [Nuxt Documentation](https://nuxt.com/docs)
- [Repository referensi](https://github.com/farhannazrull/nuxt-practice-rocketversity)
