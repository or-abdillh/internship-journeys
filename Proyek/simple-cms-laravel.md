# 🧩 Project Magang – **Portfolio CMS with Laravel**

## 🎯 Tujuan Utama

Membangun **CMS (Content Management System)** sederhana menggunakan **Laravel**, yang berfungsi untuk mengelola konten dari website portofolio pribadi.
Project ini merupakan lanjutan dari project sebelumnya (Portfolio Website menggunakan HTML + Tailwind CSS).

---

## 🌟 Goals

### **Goal 1:**

**Memindahkan web portofolio yang sudah dibangun sebelumnya menggunakan HTML dan Tailwind ke dalam Laravel page.**

#### 🎯 Sub-goals:

* Mengintegrasikan template HTML lama ke struktur Laravel Blade.
* Mengatur layout global (header, footer, dan section utama).
* Menggunakan komponen Blade (`@include`, `@yield`, `@section`) untuk membuat tampilan modular.
* Memastikan asset seperti Tailwind dan image berfungsi dengan baik.

#### 🧭 Teknik:

* Pindahkan semua file `.html` ke folder `resources/views`.
* Gunakan layout utama `resources/views/layouts/app.blade.php`.
* Buat route publik untuk setiap halaman portofolio (`/`, `/projects`, `/skills`, `/contact`).
* Pastikan Tailwind di-setup menggunakan **Vite**.

#### 💡 Tips & Trick:

* Dokumentasi Blade: [https://laravel.com/docs/11.x/blade](https://laravel.com/docs/11.x/blade)
* Panduan setup Tailwind + Laravel: [https://tailwindcss.com/docs/guides/laravel](https://tailwindcss.com/docs/guides/laravel)
* Gunakan direktif `@vite` untuk memanggil file CSS/JS.

  ```blade
  @vite('resources/css/app.css')
  ```

---

### **Goal 2:**

**Melakukan analisa dan perancangan Database menggunakan tool DrawSQL**

#### 🎯 Sub-goals:

* Mendesain database dengan entitas utama:

  * `projects` → data project portofolio
  * `skills` → daftar keahlian
  * `contacts` → pesan dari form kontak
  * `profile` → data profil pengguna
* Menentukan relasi antar tabel (jika ada).
* Menghasilkan *ERD (Entity Relationship Diagram)* final.

#### 🧭 Teknik:

1. Buat akun di [https://drawsql.app/](https://drawsql.app/).
2. Desain struktur tabel sesuai kebutuhan CMS.
3. Export hasil desain menjadi `.png` dan `.sql`.
4. Implementasikan hasil desain ke migration file di Laravel.

#### 💡 Tips & Trick:

* Gunakan *naming convention* Laravel (`snake_case`, singular model, plural table).
* Dokumentasi ERD Laravel (unofficial): [https://laravel.com/docs/11.x/migrations](https://laravel.com/docs/11.x/migrations)

---

### **Goal 3:**

**Membuat admin panel sederhana untuk melakukan CRUD content yang ditampilkan di website portofolio.**

#### 🎯 Sub-goals:

* Membuat halaman login admin (gunakan Laravel Breeze).
* Mengimplementasikan CRUD untuk:

  * Projects
  * Skills
  * Profile
* Menampilkan data ke halaman publik (frontend).
* Menambahkan validasi input.

#### 🧭 Teknik:

1. Install Laravel Breeze untuk Auth:

   ```bash
   composer require laravel/breeze --dev
   php artisan breeze:install
   npm install && npm run dev
   php artisan migrate
   ```
2. Buat route dengan middleware `auth` untuk admin:

   ```php
   Route::middleware(['auth'])->group(function () {
       Route::resource('projects', Admin\ProjectController::class);
   });
   ```
3. Buat controller, model, dan view untuk setiap entity.
4. Gunakan Blade component (`<x-input>`, `<x-button>`) untuk UI form admin.

#### 💡 Tips & Trick:

* Gunakan resource controller agar CRUD rapi:
  [https://laravel.com/docs/11.x/controllers#resource-controllers](https://laravel.com/docs/11.x/controllers#resource-controllers)
* Dokumentasi Validasi:
  [https://laravel.com/docs/11.x/validation](https://laravel.com/docs/11.x/validation)
* Gunakan [Flowbite](https://flowbite.com/docs/getting-started/laravel/) atau [Tailwind UI](https://tailwindui.com/) sebagai referensi UI form.

---

### **Goal 4:**

**Menyimpan inputan dari contact form web portofolio ke dalam admin panel**

#### 🎯 Sub-goals:

* Membuat form kontak di halaman publik (`/contact`).
* Menyimpan input form ke database (`contacts` table).
* Menampilkan data kontak di halaman admin.

#### 🧭 Teknik:

1. Buat route `POST /contact` dan arahkan ke `ContactController@store`.
2. Gunakan validasi form sebelum menyimpan:

   ```php
   $validated = $request->validate([
       'name' => 'required',
       'email' => 'required|email',
       'message' => 'required|min:10'
   ]);
   ```
3. Simpan data ke model `Contact` dan arahkan user ke halaman sukses.

#### 💡 Tips & Trick:

* Gunakan `@csrf` di Blade form untuk keamanan.
* Dokumentasi Request Validation:
  [https://laravel.com/docs/11.x/validation#form-request-validation](https://laravel.com/docs/11.x/validation#form-request-validation)
* Tambahkan notifikasi kecil setelah submit (bisa pakai session flash).

---

## 📅 Timeline (4 Minggu)

| Minggu       | Fokus                                            | Target Output                                        |
| ------------ | ------------------------------------------------ | ---------------------------------------------------- |
| **Minggu 1** | Setup Laravel + Migrasi Portofolio ke Blade      | Struktur Laravel rapi, Tailwind terintegrasi         |
| **Minggu 2** | Desain Database + Implementasi Migration & Model | ERD di DrawSQL selesai, tabel Laravel terbentuk      |
| **Minggu 3** | CRUD Admin Panel                                 | Admin login + CRUD Project, Skill, Profile berfungsi |
| **Minggu 4** | Contact Form + Review Final + Deploy             | Data form tersimpan, sistem siap presentasi          |

📆 **Deadline:** Maksimal **H-7** sebelum masa magang berakhir.
💾 Deployment opsional ke **Vercel** atau **Laravel Forge**.

---

## 🧠 Tips Tambahan untuk Sukses Project Ini

### 🪶 Git Workflow

* Gunakan branch per fitur:
  `feature/migrate-blade`, `feature/admin-crud`, `feature/contact-form`
* Gunakan commit message konvensional:

  * `feat: add contact form submission`
  * `fix: update project model migration`
* Buat Pull Request ke branch `main` untuk setiap milestone.

📖 Referensi:
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

### 🎨 Inspirasi UI Admin

Cari referensi UI di [Dribbble](https://dribbble.com/tags/admin_dashboard) dengan keyword:

* `minimal admin dashboard`
* `portfolio admin`
* `cms interface`

Gunakan elemen yang simple dan ringan agar fokus ke fungsi, bukan estetika berlebihan.

---

### ⚙️ Struktur Folder Disarankan

```
app/
 ├── Http/
 │   ├── Controllers/
 │   │   ├── Admin/
 │   │   └── Public/
 │
resources/
 ├── views/
 │   ├── admin/
 │   ├── public/
 │   └── layouts/
```

---

### 📑 Deliverables Akhir

* Source code di GitHub (public repository)
* ERD (.png atau link DrawSQL)
* File `.env.example` (tanpa credential sensitif)
* README.md berisi:

  * Deskripsi singkat project
  * Panduan setup lokal
  * Screenshot admin & public page

---