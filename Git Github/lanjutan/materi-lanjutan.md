# 📚 Materi Lanjutan: Commit Message & Pull Request

## 🎯 Tujuan
Memberikan pemahaman tentang cara menulis pesan commit yang baik agar riwayat Git lebih rapi dan mudah dipahami, serta mengenalkan alur kerja menggunakan Pull Request (PR) di GitHub.

---

## 1. Pentingnya Commit Message
Commit message yang baik:
- Memudahkan kolaborasi (tim bisa cepat memahami perubahan)
- Memudahkan tracking bug
- Membantu otomatisasi (CI/CD, release note, changelog)

---

## 2. Struktur Commit Message
Format umum (mengikuti **Conventional Commits**):

<type>(optional scope): <short summary>
<BLANK LINE>
(optional body)
<BLANK LINE>
(optional footer)


### Contoh:


feat(auth): tambah fitur login dengan Google

Menambahkan integrasi OAuth2 untuk login menggunakan akun Google.
Perubahan ini melibatkan update pada controller AuthController.

Closes #12


### Tipe Commit yang Umum:
| Tipe     | Keterangan                                    |
|----------|-----------------------------------------------|
| feat     | Fitur baru                                   |
| fix      | Perbaikan bug                                |
| docs     | Perubahan dokumentasi                        |
| style    | Format kode (spasi, titik koma, dll)         |
| refactor | Refactor kode tanpa menambah fitur/bugfix    |
| test     | Menambah atau memperbaiki pengujian          |
| chore    | Perubahan kecil (build, tool, dependensi)    |

---

## 3. Pull Request (PR)
Pull Request adalah mekanisme di GitHub untuk menggabungkan perubahan dari satu branch ke branch lain (biasanya ke `main` atau `develop`), dengan kesempatan untuk review terlebih dahulu.

### Alur Dasar PR:
1. Buat branch baru untuk fitur/perbaikan
2. Commit perubahan dengan pesan yang baik
3. Push branch ke GitHub
4. Buat Pull Request di GitHub
5. Lakukan code review (oleh rekan tim)
6. Jika sudah disetujui, merge ke branch utama

---

## 4. Tips Membuat Pull Request yang Baik
- Gunakan judul PR yang jelas
- Tambahkan deskripsi singkat mengenai perubahan
- Jika menyelesaikan issue tertentu, hubungkan dengan `Closes #issue_number`
- Usahakan satu PR fokus pada satu perubahan besar (hindari campur aduk)

---

## 5. Referensi
- 📖 Conventional Commits: https://www.conventionalcommits.org/en/v1.0.0/
- 📖 Git Commit Guidelines (Angular): https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format
- 📖 GitHub Pull Requests: https://docs.github.com/en/pull-requests