# 📚 Minggu 1 – Pengenalan Laravel & Setup

## 🎯 Learning Objectives

Setelah sesi ini, peserta diharapkan mampu:

1. Memahami apa itu Laravel dan mengapa digunakan.
2. Meng-install Laravel menggunakan Composer.
3. Menjalankan aplikasi Laravel di local server.
4. Memahami struktur folder Laravel.
5. Membuat route sederhana di `routes/web.php`.
6. Membuat controller untuk meng-handle request.
7. Membuat view dengan Blade template.

---

## 📖 Materi Pembelajaran

### 1. Apa itu Laravel?

* Laravel adalah **framework PHP** untuk membangun aplikasi web dengan arsitektur MVC (**Model-View-Controller**).
* Keunggulan Laravel:

  * Struktur rapih → lebih mudah dibanding PHP native.
  * Built-in fitur: Routing, Authentication, ORM (Eloquent), Blade templating, Artisan CLI.
  * Komunitas besar & dokumentasi lengkap.

---

### 2. Instalasi Laravel

1. Pastikan **PHP ≥ 8.1**, Composer, dan MySQL sudah terinstall.
2. Buat project baru:

   ```bash
   composer create-project laravel/laravel portfolio-laravel
   cd portfolio-laravel
   ```
3. Jalankan server development:

   ```bash
   php artisan serve
   ```

   Default akan jalan di: [http://localhost:8000](http://localhost:8000).

---

### 3. Struktur Folder Laravel (High Level)

* **app/** → berisi logic aplikasi (Models, Http/Controllers).
* **routes/** → definisi route (`web.php`, `api.php`).
* **resources/views/** → file Blade template (`.blade.php`).
* **public/** → file publik (CSS, JS, gambar).
* **database/** → migration, seeder, factory.

---

### 4. Routing Dasar

Definisi routing ada di `routes/web.php`.
Contoh:

```php
Route::get('/', function () {
    return 'Hello Laravel!';
});
```

---

### 5. Controller

Buat controller dengan Artisan:

```bash
php artisan make:controller HomeController
```

Edit `app/Http/Controllers/HomeController.php`:

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class HomeController extends Controller
{
    public function index()
    {
        return view('home');
    }
}
```

Tambahkan route di `routes/web.php`:

```php
Route::get('/', [App\Http\Controllers\HomeController::class, 'index']);
```

---

### 6. Blade Template Dasar

Buat file `resources/views/home.blade.php`:

```blade
<!DOCTYPE html>
<html>
<head>
    <title>Laravel Intro</title>
</head>
<body>
    <h1>Halo, {{ $name ?? 'Laravel User' }}</h1>
    <p>Selamat datang di project pertama Laravel kamu 🚀</p>
</body>
</html>
```

Edit controller untuk mengirim data:

```php
public function index()
{
    return view('home', ['name' => 'Oka']);
}
```

---

## 📝 Latihan

### 🔹 Latihan 1: Setup & Run

* [ ] Install Laravel & jalankan di `localhost:8000`.
* [ ] Screenshot halaman default Laravel (logo Laravel).

### 🔹 Latihan 2: Routing Dasar

* [ ] Tambahkan 2 route baru di `web.php`:

  * `/about` → return text `"Ini halaman About"`.
  * `/contact` → return text `"Ini halaman Contact"`.

### 🔹 Latihan 3: Controller & Blade

* [ ] Buat controller `ProfileController`.
* [ ] Tambahkan method `index()` untuk menampilkan view `profile.blade.php`.
* [ ] View `profile.blade.php` harus berisi:

  ```html
  <h1>Halo, Nama Kamu</h1>
  <p>Ini adalah halaman profile sederhana.</p>
  ```
* [ ] Panggil controller via route `/profile`.

### 🔹 Latihan 4: Blade Templating

* [ ] Buat file `layout.blade.php` dengan struktur HTML dasar + `@yield('content')`.
* [ ] Extend layout di `home.blade.php` dan `profile.blade.php` dengan `@extends`.
* [ ] Tambahkan `@section('content')` untuk menampilkan konten halaman.

---

## ✅ Checkpoint Minggu 1

1. Bisa install Laravel dan menjalankan server.
2. Bisa menambahkan route sederhana.
3. Bisa membuat controller & view Blade.
4. Bisa menggunakan Blade layout untuk reusability.

---

## 📚 Referensi

* [Laravel Docs – Getting Started](https://laravel.com/docs/11.x)
* [Laravel Routing](https://laravel.com/docs/11.x/routing)
* [Laravel Controllers](https://laravel.com/docs/11.x/controllers)
* [Laravel Blade Templates](https://laravel.com/docs/11.x/blade)