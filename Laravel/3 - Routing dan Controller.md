# 📚 Minggu 3 – Routing & Controller

## 🎯 Tujuan Pembelajaran

* Memahami cara kerja routing di Laravel.
* Mengenal tipe route (GET, POST, PUT, DELETE).
* Menggunakan route parameter & named route.
* Membuat controller untuk memisahkan logic.
* Menghubungkan controller dengan model & view.
* Menampilkan data sederhana ke browser.

---

## 📝 Materi Pembelajaran

### 1. Routing Dasar

* Routing di Laravel didefinisikan di file `routes/web.php`.
* Contoh route sederhana:

  ```php
  Route::get('/hello', function () {
      return 'Hello, Laravel!';
  });
  ```
* Route dengan parameter:

  ```php
  Route::get('/hello/{name}', function ($name) {
      return "Hello, $name!";
  });
  ```
* Named route:

  ```php
  Route::get('/about', function () {
      return 'About Page';
  })->name('about.page');
  ```

📖 Dokumentasi: [Routing Laravel](https://laravel.com/docs/11.x/routing)

---

### 2. Controller

* Controller digunakan untuk memisahkan logic dari file route.

* Membuat controller:

  ```bash
  php artisan make:controller ProjectController
  ```

* Contoh controller:

  ```php
  namespace App\Http\Controllers;

  use App\Models\Project;

  class ProjectController extends Controller
  {
      public function index()
      {
          $projects = Project::all();
          return response()->json($projects);
      }
  }
  ```

* Menghubungkan route ke controller:

  ```php
  Route::get('/projects', [ProjectController::class, 'index']);
  ```

📖 Dokumentasi: [Laravel Controllers](https://laravel.com/docs/11.x/controllers)

---

### 3. Route Resource

* Laravel menyediakan cara cepat untuk membuat CRUD route.
* Contoh:

  ```php
  Route::resource('projects', ProjectController::class);
  ```
* Akan otomatis membuat route untuk `index`, `create`, `store`, `show`, `edit`, `update`, `destroy`.

📖 Dokumentasi: [Resource Controllers](https://laravel.com/docs/11.x/controllers#resource-controllers)

---

### 4. Controller + Model + View (MVT Pattern)

* Konsep alurnya:

  1. Request datang → route.
  2. Route memanggil method di controller.
  3. Controller mengambil data dari model.
  4. Controller me-return response (sementara bisa berupa JSON).
* Contoh:

  ```php
  Route::get('/projects', [ProjectController::class, 'index']);
  ```

  ```php
  public function index()
  {
      $projects = Project::all();
      return response()->json($projects);
  }
  ```

---

## 🎯 Latihan

### Latihan 1 – Route Dasar

1. Tambahkan route `/hello` yang mengembalikan tulisan "Hello, World!".
2. Tambahkan route `/hello/{name}` untuk menerima parameter nama.

✅ **Checkpoint:** Route bisa diakses di browser.

---

### Latihan 2 – Membuat Controller

1. Buat `ProjectController`.
2. Tambahkan method `index()` untuk menampilkan semua project (JSON).
3. Tambahkan route `/projects` yang memanggil `index()`.

✅ **Checkpoint:** Saat akses `/projects`, muncul list data project dari database.

---

### Latihan 3 – Route Resource

1. Ubah route `/projects` menjadi `Route::resource('projects', ProjectController::class)`.
2. Tambahkan method `show($id)` di `ProjectController` untuk menampilkan 1 project berdasarkan ID.

✅ **Checkpoint:** Akses `/projects/1` menampilkan data project dengan ID=1.

---

### Latihan 4 – Mini API Sederhana

1. Buat `SkillController`.
2. Tambahkan route resource `skills`.
3. Implementasikan:

   * `index()` → tampilkan semua skills.
   * `store()` → simpan skill baru dari request.
   * `update()` → update skill berdasarkan ID.
   * `destroy()` → hapus skill berdasarkan ID.

✅ **Checkpoint:** Bisa CRUD data skill lewat route (gunakan Postman atau browser + form sederhana nanti).

---

### Latihan 5 – Mini Challenge 🚀

* Buat route `/portfolio` yang menampilkan:

  * Semua project dari `ProjectController@index`.
  * Semua skill dari `SkillController@index`.
* Gabungkan hasil dalam satu response JSON seperti:

  ```json
  {
    "projects": [...],
    "skills": [...]
  }
  ```

✅ **Checkpoint:** Akses `/portfolio` menampilkan data gabungan project & skill.