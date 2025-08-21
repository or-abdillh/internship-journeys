# 🎨 Materi: Pengenalan Tailwind CSS

## 🎯 Tujuan
Memberikan pemahaman dasar tentang Tailwind CSS, cara instalasi, serta konsep utility-first yang membedakan Tailwind dari framework CSS lain.

---

## 1. Apa itu Tailwind CSS?
Tailwind CSS adalah framework CSS berbasis *utility-first*.  
Alih-alih membuat class khusus (misalnya `.btn-primary`), kita langsung menulis class utility seperti `bg-blue-500 text-white px-4 py-2 rounded`.

**Kelebihan Tailwind:**
- Lebih cepat styling UI tanpa menulis CSS panjang
- Konsisten dalam desain
- Responsif dengan breakpoints bawaan
- Mudah dikustomisasi melalui konfigurasi

---

## 2. Cara Instalasi Tailwind CSS

### a. Via CDN (cara cepat untuk belajar)
Tambahkan ini di dalam `<head>` file HTML:
```html
<script src="https://cdn.tailwindcss.com"></script>
````

### b. Via npm (proyek yang lebih serius)

```bash
npm install -D tailwindcss
npx tailwindcss init
```

Tambahkan konfigurasi di `tailwind.config.js`, lalu import di file CSS utama:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 3. Contoh Dasar

### Button sederhana dengan Tailwind:

```html
<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
  Klik Saya
</button>
```

### Card sederhana:

```html
<div class="max-w-sm rounded overflow-hidden shadow-lg p-4">
  <h1 class="text-xl font-bold">Judul Card</h1>
  <p class="text-gray-600">Ini adalah deskripsi card dengan Tailwind CSS.</p>
</div>
```

---

## 4. Responsive Design

Contoh layout responsive dengan Tailwind:

```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
  <div class="bg-red-200 p-4">Kolom 1</div>
  <div class="bg-green-200 p-4">Kolom 2</div>
  <div class="bg-blue-200 p-4">Kolom 3</div>
</div>
```

👉 Pada layar kecil: 1 kolom, pada layar medium (`md:`): 3 kolom.

---

## 5. Referensi Resmi

* 📖 Dokumentasi Tailwind CSS: [https://tailwindcss.com/docs](https://tailwindcss.com/docs)
* 📖 Playground Tailwind: [https://play.tailwindcss.com](https://play.tailwindcss.com)
