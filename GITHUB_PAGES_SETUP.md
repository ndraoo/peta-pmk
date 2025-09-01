# Panduan Setup GitHub Pages

## Langkah-langkah untuk mengatasi error 404 pada GitHub Pages:

### 1. Buat Repository di GitHub
1. Buka [GitHub.com](https://github.com) dan login
2. Klik tombol "New" atau "+" untuk membuat repository baru
3. Beri nama repository: `peta-pmk` (atau nama yang Anda inginkan)
4. Pastikan repository adalah **Public** (GitHub Pages gratis hanya untuk repository public)
5. **JANGAN** centang "Add a README file" (karena sudah ada)
6. Klik "Create repository"

### 2. Hubungkan Repository Lokal dengan GitHub
Jalankan perintah berikut di terminal (ganti `username` dengan username GitHub Anda):

```bash
git remote add origin https://github.com/USERNAME/peta-pmk.git
git branch -M main
git push -u origin main
```

### 3. Setup GitHub Pages
1. Buka repository di GitHub
2. Klik tab **Settings**
3. Scroll ke bawah ke bagian **Pages** (di sidebar kiri)
4. Di bagian **Source**, pilih **Deploy from a branch**
5. Pilih branch **main** dan folder **/ (root)**
6. Klik **Save**

### 4. Tunggu Deployment
- GitHub akan memproses deployment (biasanya 1-5 menit)
- Anda akan melihat notifikasi hijau "Your site is published at https://USERNAME.github.io/peta-pmk"

### 5. Akses Website
Website Anda akan tersedia di: `https://USERNAME.github.io/peta-pmk`

## Troubleshooting Error 404:

### Jika masih error 404:
1. **Pastikan file `index.html` ada di root repository**
2. **Pastikan repository adalah Public**
3. **Tunggu beberapa menit** - deployment membutuhkan waktu
4. **Cek tab Actions** di GitHub untuk melihat status deployment
5. **Pastikan branch yang dipilih di Settings > Pages adalah `main`**

### Jika file tidak ter-upload:
```bash
git status
git add .
git commit -m "Update files"
git push origin main
```

## Catatan Penting:
- GitHub Pages hanya mendukung file statis (HTML, CSS, JS)
- File `index.html` harus ada di root directory
- Repository harus public untuk GitHub Pages gratis
- URL akan selalu: `https://USERNAME.github.io/REPOSITORY-NAME`
