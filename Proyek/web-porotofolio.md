# 📌 Project Brief: Personal Web Portfolio

## 🎯 Tujuan

Project ini bertujuan agar kalian dapat:

1. **Menguasai dasar Git & GitHub** dalam workflow pengembangan software.
2. **Memahami penggunaan Tailwind CSS** melalui implementasi di project nyata.
3. **Membangun portofolio pribadi** sebagai showcase skill dasar kalian.
4. **Menerapkan discipline workflow**: commit message yang baik, penggunaan branch, dan pull request.

---

## ⚙️ Tech Stack

* **Vite JS** → untuk development environment yang cepat.
* **Vanilla JS** → JavaScript dasar tanpa framework.
* **Tailwind CSS** → styling modern tanpa menulis CSS manual.
* **Git + GitHub** → version control & kolaborasi.

---

## 📂 Struktur Project (minimal)

```
portfolio/
├─ index.html
├─ src/
│  ├─ main.js
│  └─ style.css (opsional, jika butuh global style)
├─ public/
│  └─ images/ (foto profil, project showcase, dll.)
├─ README.md
└─ package.json
```

---

## 🖥️ Fitur Minimal yang Harus Ada

1. **Halaman Home**

   * Foto profil + nama lengkap.
   * Deskripsi singkat tentang diri kalian.

2. **Halaman About**

   * Penjelasan singkat background pendidikan/skill.

3. **Halaman Project/Portfolio**

   * Minimal 2 project yang pernah kalian buat (boleh dummy project).
   * Ditampilkan dalam card/grid.

4. **Contact Section**

   * Email, GitHub, LinkedIn (boleh pakai link dummy).

---

## 📋 Checkpoints & Aturan

### 🔹 Setup & Git

* [ ] Inisialisasi project dengan **Vite JS**.
* [ ] Setup **Tailwind CSS via NPM**.
* [ ] Buat repository di GitHub (nama repo: `portfolio-nama`).
* [ ] Push initial commit ke branch `main`.

### 🔹 Workflow Git

* [ ] Buat branch `feature/homepage` → kerjakan halaman Home.
* [ ] Commit dengan format yang jelas:

  ```
  feat: add homepage with profile section
  fix: adjust responsive layout on homepage
  docs: update README with setup instructions
  ```
* [ ] Push branch ke GitHub, lalu buat **Pull Request** → merge ke `main`.
* [ ] Lakukan hal yang sama untuk halaman About, Project, dan Contact.

### 🔹 Tailwind

* [ ] Gunakan minimal 5 utility classes Tailwind (contoh: `flex`, `grid`, `text-xl`, `bg-indigo-500`, `rounded-lg`).
* [ ] Gunakan **responsive utilities** (contoh: `md:flex`, `lg:grid-cols-3`).
* [ ] Tambahkan sedikit **hover effect** pada tombol/link.

### 🔹 Deployment

* [ ] Deploy project kalian di Vercel.
* [ ] Tambahkan link demo di `README.md`.

---

## 🎨 Cara Mencari Referensi UI di Dribbble

Sebagai developer, penting untuk bisa mencari inspirasi desain sebelum membuat project. Dribbble adalah salah satu platform populer untuk mencari referensi UI/UX modern.

---

### 🔹 1. Akses Dribbble

* Buka: [https://dribbble.com/](https://dribbble.com/)
* Bisa digunakan tanpa login, tapi kalau daftar akun akan lebih mudah untuk **save & like** desain.

---

### 🔹 2. Gunakan Keyword Pencarian

Gunakan kata kunci yang relevan dengan **project portfolio pribadi**. Beberapa contoh keyword:

* `"portfolio website"`
* `"personal portfolio"`
* `"developer portfolio"`
* `"designer portfolio"`
* `"minimal portfolio"`
* `"landing page portfolio"`

👉 Pro tip: coba kombinasikan keyword dengan style, misalnya:

* `"dark mode portfolio"`
* `"clean minimal portfolio"`
* `"modern web portfolio"`

---

### 🔹 3. Filter & Eksplorasi

* **Filter by Color** → pilih palet warna yang sesuai (misalnya biru/indigo untuk tech).
* **Filter by Animation** → cari inspirasi interaksi (untuk diimplementasi nanti dengan animasi dasar).
* **Save/Bookmark** → simpan desain yang menarik untuk jadi bahan referensi.

---

### 🔹 4. Analisis Desain

Saat melihat referensi di Dribbble, coba analisis:

* **Layout** → apakah pakai grid? sidebar? hero section besar?
* **Typography** → font besar untuk nama, font kecil untuk deskripsi.
* **Color Scheme** → warna dominan apa yang dipakai?
* **Section** → apakah ada "About", "Projects", "Contact"?

---

### 🔹 5. Implementasi ke Project

* Tidak perlu meniru 100%, cukup ambil **inspirasi konsep**.
* Gunakan **Tailwind CSS** untuk membuat layout serupa (misalnya `grid-cols-3`, `flex-col`, `text-2xl`).
* Sesuaikan dengan branding diri sendiri (foto, warna, nama, project asli).

---

### 🔹 6. Contoh Hasil Pencarian

* [Portfolio Website Examples](https://dribbble.com/search/portfolio%20website)
* [Personal Portfolio UI](https://dribbble.com/search/personal%20portfolio)
* [Minimal Portfolio](https://dribbble.com/search/minimal%20portfolio)

---

## 📝 Tugas Akhir

1. Repo GitHub lengkap dengan branch & pull request history.
2. Website portfolio yang bisa diakses online.
3. README.md yang berisi:

   * Cara setup project.
   * Deskripsi singkat project.
   * Link ke demo online.

---

## 📚 Referensi

* [Dokumentasi GitHub](https://docs.github.com/en)
* [Konvensi Commit Message (Conventional Commits)](https://www.conventionalcommits.org/)
* [Tailwind CSS Docs](https://tailwindcss.com/docs)
* [Vite Docs](https://vitejs.dev/guide/)
* [Deploy ke Vercel](https://vercel.com/docs/frameworks/vite)