# Lesson 1-4 - Dynamic Routes

Checkpoint ini memakai dynamic route parameters untuk memakai satu komponen pada banyak chapter dan lesson.

## Route yang tersedia

- `/` - daftar contoh URL.
- `/courses/1/lessons/2` - Chapter 1, Lesson 2.
- `/courses/1/lessons/4` - Chapter 1, Lesson 4.
- `/courses/2/lessons/1` - Chapter 2, Lesson 1.

Route tersebut dipetakan dari `app/pages/courses/[chapter]/lessons/[lesson].vue`.

## Menjalankan

```bash
npm install
npm run dev
```
