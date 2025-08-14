# ​ Materi: Pengenalan Git & GitHub

## ​ Tujuan
Memberikan pemahaman dasar tentang apa itu Git dan GitHub, serta cara menggunakannya untuk mengelola versi kode secara kolaboratif.

---

## 1. Apa itu Git?
Git adalah sistem kontrol versi (Version Control System) yang memungkinkan kita melacak perubahan pada file atau proyek, bekerja secara kolaboratif, dan kembali ke versi sebelumnya jika diperlukan.

**Fungsi utama Git:**
- Melacak perubahan (versioning)
- Kolaborasi dalam tim
- Mengembalikan ke versi sebelumnya
- Membuat cabang (branch) untuk fitur atau percobaan

**📖 Bacaan Tambahan:**
- Dokumentasi resmi Git: https://git-scm.com/doc
- Tutorial Git interaktif: https://git-scm.com/docs/gittutorial

---

## 2. Apa itu GitHub?
GitHub adalah platform hosting untuk menyimpan repository Git di cloud.  
Dengan GitHub, kita bisa:
- Menyimpan kode secara online
- Bekerja sama dalam tim
- Menggunakan fitur Pull Request untuk review kode
- Mengelola issue dan dokumentasi

**📖 Bacaan Tambahan:**
- Dokumentasi GitHub: https://docs.github.com/en/get-started/quickstart
- GitHub Guides (Tutorial & video): https://guides.github.com/

---

## 3. Istilah Penting
| Istilah       | Penjelasan |
|--------------|------------|
| Repository   | Folder/project yang dikelola Git |
| Commit       | Catatan perubahan yang kita simpan |
| Branch       | Jalur pengembangan terpisah |
| Merge        | Menggabungkan branch |
| Clone        | Mengunduh repository |
| Push         | Mengirim perubahan ke server |
| Pull         | Mengambil update terbaru dari server |

---

## 4. Instalasi Git
1. Download Git di: https://git-scm.com/downloads  
2. Install sesuai OS yang digunakan  
3. Cek instalasi  
   ```bash
   git --version

---

## 5. Konfigurasi Awal

```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```

---

## 6. Alur Kerja Dasar Git

### 1). Buat folder proyek
```bash
mkdir proyek-belajar-git && cd ./proyek-belajar-git
```

### 2). Inisialisasi Git

```bash
git init
```

### 3). Tambah file ke staging

```bash
git add nama_file
```

### 4). Commit perubahan

```bash
git commit -m "Pesan commit"
```

### 5). Hubungkan ke GitHub

```bash
git remote add origin https://github.com/username/nama-repo.git
```

### 6). Kirim ke GitHub

```bash
git push -u origin main
```

---

## 7. Diagram Alur Dasar

```bash
File → git add → Staging Area → git commit → Local Repository → git push → Remote Repository (GitHub)
```

---

## 8. Checkpoint Materi

 - [ ] Memahami perbedaan Git dan GitHub

 - [ ] Mengerti istilah-istilah dasar Git

 - [ ] Menginstall Git di komputer

 - [ ] Mengatur konfigurasi Git (username & email)

 - [ ] Memahami alur kerja dasar Git