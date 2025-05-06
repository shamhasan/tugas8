
# Aplikasi To-Do List Sederhana

Aplikasi web sederhana untuk mencatat daftar tugas (to-do list) yang dibuat menggunakan **Laravel** dan tampilan antarmuka menggunakan **Bootstrap**. Proyek ini dibuat sebagai bagian dari tugas kuliah untuk mendemonstrasikan operasi CRUD dan pengembangan aplikasi berbasis web.

## Fitur

- ✅ Menambah tugas  
- ✏️ Mengedit tugas  
- ❌ Menghapus tugas  
- 📋 Menampilkan daftar tugas  
- 🔍 Mencari tugas  
- 🕓 Dukungan timestamp (`created_at`, `updated_at`)  

## Teknologi yang Digunakan

- **Backend**: Laravel (PHP)
- **Frontend**: Bootstrap
- **Database**: MySQL (menggunakan phpMyAdmin)

## Kebutuhan Sistem

- PHP >= 8.x
- Composer
- Laravel (versi terbaru)
- MySQL server (contoh: XAMPP atau Laragon)
- phpMyAdmin untuk mengelola database

## Cara Instalasi

1. **Clone repository ini**
   ```bash
   git clone https://github.com/username-anda/simple-todo-laravel.git
   cd simple-todo-laravel
   ```

2. **Install dependensi**
   ```bash
   composer install
   ```

3. **Konfigurasi file `.env`**
   - Salin `.env.example` menjadi `.env`
   - Ubah konfigurasi database:
     ```env
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=nama_database_anda
     DB_USERNAME=root
     DB_PASSWORD=
     ```

4. **Membuat tabel database**
   Anda bisa menggunakan migrasi Laravel (jika tersedia), atau membuat tabel manual di phpMyAdmin dengan struktur berikut:

### Struktur Tabel Database

Aplikasi ini menggunakan database lokal MySQL dan dikelola menggunakan phpMyAdmin. Berikut struktur tabel `tasks` yang digunakan:

| Kolom         | Tipe         | Atribut                 | Deskripsi                      |
|---------------|--------------|--------------------------|-------------------------------|
| `id`          | bigint(20)   | PRIMARY, AUTO_INCREMENT  | ID unik untuk setiap tugas     |
| `task`        | varchar(255) | NOT NULL                 | Deskripsi tugas                |
| `is_done`     | tinyint(1)   | Default: 0               | Status tugas (0 = belum selesai) |
| `created_at`  | timestamp    | Bisa bernilai NULL       | Waktu saat tugas dibuat        |
| `updated_at`  | timestamp    | Bisa bernilai NULL       | Waktu saat tugas terakhir diubah |

> 💡 Struktur ini bisa Anda buat melalui phpMyAdmin atau melalui file migrasi Laravel jika sudah disediakan.

## Menjalankan Aplikasi

```bash
php artisan serve
```

Lalu buka di browser:
```
http://127.0.0.1:8000
```

## Lisensi

Proyek ini dibuat hanya untuk keperluan akademik. Tidak ada lisensi resmi yang diterapkan.
