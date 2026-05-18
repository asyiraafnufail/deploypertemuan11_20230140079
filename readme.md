# Tugas Praktikum - Pertemuan 11

## 👤 Identitas Mahasiswa
* **Nama:** ASYIRAAF NUFAIL DHIAURRAHMAN ARRAYYAN

---

## 📸 Dokumentasi & Screenshot Aplikasi

### 1. Halaman Registrasi Akun (`/register`)
Form pendaftaran user baru dengan inputan Username, Password, Nama Lengkap, dan Alamat tempat tinggal yang terhubung dengan objek `RegisterRequest` DTO.
![Halaman Register](/ss/register.png)

### 2. Halaman Login (`/login`)
Form masuk sistem yang telah diamankan oleh Spring Security, lengkap dengan validasi pesan kesalahan jika akun tidak cocok dan notifikasi jika berhasil *logout*.
![Halaman Login](/ss/login.png)

### 3. Halaman Utama / Dashboard (`/home`)
Halaman utama yang terproteksi penuh. Hanya dapat diakses oleh pengguna yang sudah memiliki token otoritas sesi aktif (`ROLE_USER`).
![Halaman Home](/ss/home.png)

### 4. Struktur & Isi Tabel `users` di TablePlus
Menampilkan data akun pengguna yang berhasil tersimpan di database dengan kondisi *password* yang telah terenkripsi secara aman menggunakan algoritma `BCryptPasswordEncoder`.
![Isi Tabel Users](/ss/users.png)

### 5. Struktur & Isi Tabel `profile` di TablePlus
Menampilkan data informasi profil lengkap pengguna yang secara otomatis terikat (*mapping*) dengan ID pengguna melalui relasi `@OneToOne`.
![Isi Tabel Profile](/ss/profile.png)

---

## 🚀 Cara Menjalankan Aplikasi Secara Lokal

## 🐳 Docker Hub Registry Link
Aplikasi ini telah di-push dan dapat di-pull langsung melalui Docker Hub:
👉 [Docker Hub: asyiraafnufail/pertemuan11](https://hub.docker.com/r/asyiraafnufail/pertemuan11)

---

### 1. Persiapan Database
1. Pastikan **DBngin** (PostgreSQL) Anda sudah menyala di port `5432`.
2. Buat database kosong baru bernama `webapp` melalui **TablePlus**.

### 2. Konfigurasi `application.properties`
Pastikan baris URL database mengarah ke host lokal Anda:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/webapp
spring.datasource.username=postgres
spring.datasource.password=