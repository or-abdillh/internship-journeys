# 🎨 Materi: Tailwind CSS dengan NPM & Vite JS

## 🎯 Tujuan
Memberikan pemahaman cara menggunakan Tailwind CSS dalam proyek modern menggunakan NPM dan Vite JS, bukan melalui CDN.

---

## 1. Mengapa Menggunakan NPM & Vite?
- **Lebih fleksibel**: mudah dikustomisasi sesuai kebutuhan
- **Lebih efisien**: build CSS otomatis hanya memuat class yang digunakan
- **Integrasi modern**: cocok untuk framework seperti Vue, React, Svelte

---

## 2. Membuat Project Baru dengan Vite
Jalankan perintah berikut:
```bash
npm create vite@latest my-tailwind-app
cd my-tailwind-app
npm install
```

Pilih framework sesuai kebutuhan (misalnya Vanilla, Vue, atau React). Untuk intro ini kita pakai Vanilla.

## 3. Instalasi Tailwind CSS

Tambahkan Tailwind ke proyek:

```bash
npm install tailwindcss @tailwindcss/vite
```

## 4. Konfigurasi Vite dengan Tailwind

Buat file `vite.config.js` di root proyek dan masukkan konfigurasi berikut ini:

```javascript
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})
```

## 5. Import Tailwind CSS

Modifikasi file `/src/main.js` dan `/src/style.css` dengan memasukkan code import tailwind berikut didalan masing - masing file tersebut:

```javascript
import './style.css'
```

```css
@import "tailwindcss";
```

## 6. Gunakan Tailwind di HTML

Edit index.html atau file App.jsx/main.js (tergantung framework). Contoh di index.html:

```html
<h1 class="text-3xl font-bold underline text-blue-600">
  Hello, Tailwind + Vite!
</h1>
```

## 7. Jalankan Proyek
```bash
npm run dev
```

Lalu buka URL yang diberikan (biasanya http://localhost:5173).