# Perancangan Antarmuka & Sistem (Aplikasi Kepegawaian / HRMS)

## 1. Hirarki Menu (Sidebar / Navigation)
- **Dashboard**
  - Ringkasan Statistik Pegawai (Total, Hadir, Cuti)
  - Grafik Presensi Bulanan
- **Data Pegawai (Data Master)**
  - Daftar Pegawai
  - Tambah / Edit / Hapus Pegawai
- **Kehadiran**
  - Rekap Presensi Harian
- **Penggajian**
  - Laporan Gaji Pegawai
- **Pengaturan**
  - Manajemen Pengguna & Sistem
  erDiagram
    PEGAWAI ||--o{ KEHADIRAN : memiliki
    PEGAWAI ||--o{ GAJI : menerima
    
    PEGAWAI {
        string nip PK
        string nama
        string jabatan
        string status
    }
    KEHADIRAN {
        int id PK
        string nip FK
        date tanggal
        string status_hadir
    }
    GAJI {
        int id PK
        string nip FK
        string bulan
        double total_gaji
    }
    
    https://www.figma.com/design/EEvdkd3EgnwbFYhiKwyyj8/Untitled?node-id=0-1&t=y9uZEG89EJK7QdUa-1
