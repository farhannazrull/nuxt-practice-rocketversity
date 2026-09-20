# Lesson 1-3 - Nested Routes

Checkpoint ini memisahkan konteks chapter dan tampilan lesson menggunakan nested routes.

## Route yang tersedia

- `/` - landing page lesson.
- `/chapters/1` - parent route untuk Chapter 01.
- `/chapters/1/lessons` - child page untuk lesson display.
- `/chapters/1/lessons/1-2` - dynamic child lesson route.

`app/pages/chapters/1.vue` merender child route melalui `<NuxtPage />`.

## Menjalankan

```bash
npm install
npm run dev
```
