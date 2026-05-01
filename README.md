# SIAKAD Gallery — Sistem Informasi KRS Mahasiswa


## Akun Demo

| Role | Username / NIM / NIDN | Password |
|------|-----------------------|----------|
| **Admin** | `admin` | `password123` |
| **Mahasiswa** | `21010023` | `password123` |
| **Dosen** | `198504122010` | `password123` |

---

## Daftar Route

| URL | Nama View | Role | Akses |
|-----|-----------|------|-------|
| `/login` | `auth/login` | Semua | Ya |
| `/mahasiswa/dashboard` | `mahasiswa/dashboard` | Mahasiswa | Ya |
| `/mahasiswa/profil` | `mahasiswa/profil` | Mahasiswa | Ya |
| `/mahasiswa/krs` | `mahasiswa/krs` | Mahasiswa | Ya |
| `/mahasiswa/khs` | `mahasiswa/khs` | Mahasiswa | Ya |
| `/mahasiswa/jadwal` | `mahasiswa/jadwal` | Mahasiswa | Ya |
| `/dosen/dashboard` | `dosen/dashboard` | Dosen | Ya |
| `/dosen/daftar-mahasiswa` | `dosen/daftar_mahasiswa` | Dosen | Ya |
| `/dosen/input-nilai` | `dosen/input_nilai` | Dosen | Ya |
| `/dosen/jadwal` | `dosen/jadwal` | Dosen | Ya |
| `/admin/dashboard` | `admin/dashboard` | Admin | Ya |
| `/admin/mahasiswa` | `admin/mahasiswa/index` | Admin | Ya |
| `/admin/dosen` | `admin/dosen/index` | Admin | Ya |
| `/admin/matkul` | `admin/matkul/index` | Admin | Ya |
| `/admin/semester` | `admin/semester/index` | Admin | Ya |
| `/admin/jadwal` | `admin/jadwal/index` | Admin | Ya |

---

## Struktur View

```
resources/views/
├── layouts/          ← Layout utama (app, header, sidebar, footer)
├── components/       ← Blade Components (<x-stat-card>, <x-badge>, <x-alert>)
├── auth/             ← Halaman login
├── mahasiswa/        ← Dashboard, Profil, KRS, KHS, Jadwal
├── dosen/            ← Dashboard, Input Nilai, Daftar Mahasiswa, Jadwal
└── admin/            ← Dashboard + CRUD (Mahasiswa, Dosen, Matkul, Semester, Jadwal)
```

---

## Blade Components

| Komponen | Penggunaan |
|----------|-----------|
| `<x-stat-card>` | Kartu statistik di dashboard |
| `<x-badge>` | Badge status (aktif, cuti, lulus, wajib, pilihan, nilai huruf) |
| `<x-alert>` | Flash message (success, error, warning, info) |
