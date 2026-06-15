# PRAKTEK Jurnal-Full-Stack-Faris-Laravel-ke-React---15-Juni-2026


# 📚 JURNAL SEJARAH: PROYEK FULL-STACK LARAVEL - REACT

## Pencapaian Besar Faris Sampai 15 Juni 2026

---

## FASE 1: MEMBANGUN PONDASI BELAKANG (BACKEND - LARAVEL)

### 1. Membuat Wadah & Struktur Data (Model & Migration)

| Aspek | Keterangan |
|-------|-------------|
| **Misi** | Membuat tabel di database untuk menyimpan data website |
| **Perintah** | `php artisan make:model NamaModel -m` |
| **Hasil** | Lahir file model `NamaModel.php` dan file migrasi tabel. Di dalam file migrasi, ditambahkan kolom `nama_model` dan `status` |
| **Eksekusi** | `php artisan migrate` — meresmikan tabel ke dalam database laptop |

### 2. Membuat Otak Aplikasi (Controller)

| Aspek | Keterangan |
|-------|-------------|
| **Misi** | Mengatur logika bagaimana data diambil dari database dan dikirim keluar |
| **Perintah** | `php artisan make:controller NamaController --api` |
| **Hasil** | Lahir file `NamaController.php`. Di dalamnya terdapat fungsi `index()` yang memerintahkan Model mengambil seluruh data (`NamaModel::all()`) lalu mengubahnya menjadi format **JSON** (`return response()->json($data)`) |

### 3. Membuat Jembatan Akses (Routing)

| Aspek | Keterangan |
|-------|-------------|
| **Misi** | Membuat alamat URL agar browser atau aplikasi luar bisa memanggil Controller |
| **Lokasi** | File `routes/web.php` |
| **Kode Jembatan** | 
```php
use App\Http\Controllers\NamaController;
Route::get('/nama-model', [NamaController::class, 'index']);
```

---

FASE 2: PERJUANGAN & TROUBLESHOOTING (DRAMA CODING SANG JAGOAN)

Kasus 1: ParseError Huruf 'p' Nakal

Aspek Keterangan
Masalah Saat menyalakan server, Laravel protes ada syntax error
Penyebab Jari tidak sengaja menekan huruf p di ujung kode Route::get(...);p
Solusi Menghapus huruf p tersebut, server langsung berjalan normal

Kasus 2: Halaman Terbuka 404 Not Found

Aspek Keterangan
Masalah Saat membuka http://127.0.0.1:8000, muncul halaman kosong Not Found
Penyebab Belum menambahkan alamat ujungnya di kolom URL browser
Solusi Setelah ditambahkan menjadi http://127.0.0.1:8000/nama-model, halaman langsung 100% SUKSES menampilkan data JSON kosong

Kasus 3: Antrean Linux Terkunci (Waiting for Cache Lock)

Aspek Keterangan
Masalah Terminal macet saat mau menginstal perlengkapan baru
Penyebab Sistem Linux sedang sibuk menjalankan proses lain di latar belakang
Solusi Menggunakan perintah sudo kill -9 untuk membubarkan antrean dan menghapus file kunci

---

FASE 3: PERSIAPAN MENUJU DUNIA DEPAN (FRONTEND - REACT.JS)

Pelajaran Penting

Kita butuh menginstal Node.js dan NPM bukan untuk membuang Laravel, melainkan sebagai "alat masak" wajib agar laptop bisa menghidupkan dan menjalankan React.js.

Perintah yang Dijalankan

```bash
sudo apt update && sudo apt install -y nodejs npm
```

---

📊 Ringkasan Progress

Fase Materi Status
1 Model & Migration (Laravel) ✅ Selesai
1 Controller API (Laravel) ✅ Selesai
1 Routing (web.php) ✅ Selesai
2 Fix ParseError huruf 'p' ✅ Selesai
2 Fix 404 Not Found ✅ Selesai
2 Fix Waiting for Cache Lock ✅ Selesai
3 Install Node.js & NPM ✅ Selesai
3 Persiapan React.js 🔄 Dalam Proses

---

Dokumentasi perjalanan belajar Full-Stack Faris dari Laravel hingga React.js



---

## ✅ Kesimpulan:

| Status | Keterangan |
|--------|-------------|
| ✅ **SUDAH RAPI** | Jurnal sejarah dari awal sampai 15 Juni 2026 sudah lengkap |
| ✅ **SIAP SIMPAN** | Faris bisa simpan di Drive atau GitHub |

