# 📚 Minggu 2 – Database & Model

## 🎯 Tujuan Pembelajaran

* Memahami cara konfigurasi database di Laravel.
* Mengenal konsep migration untuk membuat tabel.
* Mengenal seeder dan faker untuk mengisi data dummy.
* Memahami konsep Model di Laravel.
* Mengenal Eloquent ORM untuk interaksi database.
* Melakukan operasi dasar CRUD melalui Model.

---

## 📝 Materi Pembelajaran

### 1. Konfigurasi Database

* Laravel menggunakan file `.env` untuk menyimpan konfigurasi database.
* Contoh konfigurasi (gunakan MySQL):

  ```env
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=laravel_app
  DB_USERNAME=root
  DB_PASSWORD=
  ```
* Pastikan database sudah dibuat di MySQL sebelum menjalankan Laravel.

📖 Dokumentasi: [Laravel Database Configuration](https://laravel.com/docs/11.x/database#configuration)

---

### 2. Migration

* Migration adalah cara Laravel untuk membuat, mengubah, atau menghapus tabel database menggunakan kode.
* Membuat migration:

  ```bash
  php artisan make:migration create_posts_table
  ```
* Contoh migration `posts`:

  ```php
  public function up(): void
  {
      Schema::create('posts', function (Blueprint $table) {
          $table->id();
          $table->string('title');
          $table->text('content');
          $table->timestamps();
      });
  }
  ```
* Jalankan migration:

  ```bash
  php artisan migrate
  ```

📖 Dokumentasi: [Laravel Migrations](https://laravel.com/docs/11.x/migrations)

---

### 3. Seeder & Faker

* Seeder digunakan untuk mengisi data awal atau dummy ke database.
* Membuat seeder:

  ```bash
  php artisan make:seeder PostSeeder
  ```
* Contoh seeder:

  ```php
  public function run(): void
  {
      \App\Models\Post::factory(10)->create();
  }
  ```
* Jalankan:

  ```bash
  php artisan db:seed --class=PostSeeder
  ```

📖 Dokumentasi: [Laravel Seeding](https://laravel.com/docs/11.x/seeding)

---

### 4. Model

* Model adalah representasi tabel di database.
* Membuat model:

  ```bash
  php artisan make:model Post
  ```
* Contoh model `Post`:

  ```php
  class Post extends Model
  {
      protected $fillable = ['title', 'content'];
  }
  ```

📖 Dokumentasi: [Laravel Eloquent ORM](https://laravel.com/docs/11.x/eloquent)

---

### 5. CRUD Dasar dengan Eloquent

* **Create**

  ```php
  Post::create([
      'title' => 'First Post',
      'content' => 'This is the content',
  ]);
  ```

* **Read**

  ```php
  $posts = Post::all();
  ```

* **Update**

  ```php
  $post = Post::find(1);
  $post->update(['title' => 'Updated Title']);
  ```

* **Delete**

  ```php
  Post::destroy(1);
  ```

📖 Dokumentasi: [Eloquent Basic Usage](https://laravel.com/docs/11.x/eloquent#retrieving-models)

---

## 🎯 Latihan

### Latihan 1 – Setup Database

1. Konfigurasikan database di `.env`.
2. Buat database baru `portfolio_db` di MySQL.

✅ **Checkpoint:** `.env` sudah diset dan `php artisan migrate` berjalan tanpa error.

---

### Latihan 2 – Membuat Migration & Model

1. Buat migration dan model untuk entity `Project` dengan field:

   * `title` (string)
   * `description` (text)
   * `link` (string, nullable)
2. Jalankan migration.

✅ **Checkpoint:** Tabel `projects` terbentuk di database.

---

### Latihan 3 – Seeder dengan Faker

1. Buat seeder untuk entity `Project`.
2. Isi minimal 5 data dummy menggunakan faker.

✅ **Checkpoint:** Jalankan `php artisan db:seed` dan pastikan data masuk ke tabel `projects`.

---

### Latihan 4 – CRUD dengan Tinker

1. Gunakan `php artisan tinker`.
2. Buat data baru di tabel `projects`.
3. Baca semua data.
4. Update salah satu data.
5. Hapus salah satu data.

✅ **Checkpoint:** Semua operasi CRUD berhasil dijalankan dari Tinker.

---

### Latihan 5 – Mini Challenge

* Buat entity baru `Skill` dengan field:

  * `name` (string)
  * `level` (integer, range 1–100)
* Buat migration, model, dan seeder dengan minimal 5 data dummy.

✅ **Checkpoint:** Tabel `skills` terbentuk dengan data dummy.