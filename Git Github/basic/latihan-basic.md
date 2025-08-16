## ​ **Latihan: Git & GitHub Basic**

## ​ Tujuan
Melatih kemampuan menggunakan Git dan GitHub untuk mengelola proyek sederhana, termasuk membuat commit, branch, merge, dan push ke GitHub.

---

## ​ Petunjuk
1. Pastikan sudah membaca dan memahami materi di README "Materi: Pengenalan Git & GitHub"  
2. Lakukan setiap langkah secara berurutan  
3. Tandai checklist jika sudah selesai  

---

## ​ Tugas

### **1. Membuat Repository Lokal**
- [ ] Buat folder baru bernama `latihan-git`  
- [ ] Masuk ke folder tersebut  
- [ ] Inisialisasi Git (`git init`)  

### **2. Menambahkan File & Commit Pertama**
- [ ] Buat file `README.md` di dalam folder  
- [ ] Isi dengan teks: `Latihan Git & GitHub Basic`  
- [ ] Tambahkan ke staging area (`git add README.md`)  
- [ ] Commit dengan pesan `"Commit pertama"`  

### **3. Membuat Repository di GitHub**
- [ ] Login ke GitHub  
- [ ] Buat repository baru bernama `latihan-git`  
- [ ] Jangan centang "Initialize this repository with a README"  

### **4. Menghubungkan & Mengirim ke GitHub**
- [ ] Hubungkan repo lokal dengan repo GitHub (`git remote add origin ...`)  
- [ ] Push commit ke branch `main` (`git push -u origin main`)  

### **5. Membuat Branch Baru**
- [ ] Buat branch bernama `fitur-tambah-file`  
- [ ] Checkout ke branch tersebut (`git checkout -b fitur-tambah-file`)  
- [ ] Buat file `hello.txt` berisi `Hello Git!`  
- [ ] Commit perubahan  

### **6. Menggabungkan Branch**
- [ ] Checkout kembali ke `main` (`git checkout main`)  
- [ ] Merge branch `fitur-tambah-file` ke `main` (`git merge fitur-tambah-file`)  
- [ ] Push ke GitHub (`git push`)  

### **7. Mengupdate Repository**
- [ ] Edit `README.md` untuk menambahkan nama kamu  
- [ ] Commit dan push  

---

## ​ Checkpoint Latihan
- [ ] Bisa membuat repository lokal  
- [ ] Bisa melakukan commit pertama  
- [ ] Bisa membuat repository di GitHub  
- [ ] Bisa menghubungkan repo lokal ke GitHub  
- [ ] Bisa membuat branch baru  
- [ ] Bisa melakukan merge branch  
- [ ] Bisa melakukan push update ke GitHub  

---

## ​ Bonus Challenge
1. Buat branch baru bernama `fitur-bonus`  
2. Tambahkan file baru `bonus.txt` berisi daftar hobi kamu  
3. Push branch tersebut ke GitHub tanpa merge (`git push -u origin fitur-bonus`)  
4. Cek dan lihat hasilnya di GitHub  

---

## ​ Referensi Dokumentasi
- Dokumentasi Git: https://git-scm.com/doc  
- Tutorial GitHub (Pull Request, Branch, dsb): https://docs.github.com/en/get-started/quickstart  
- Panduan interaktif di GitHub Guides: https://guides.github.com/
