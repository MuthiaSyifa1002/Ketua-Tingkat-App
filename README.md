# 📚 Ketua Tingkat App

Aplikasi manajemen kelas digital untuk ketua tingkat dan anggota kelas dengan fitur lengkap untuk mengelola jadwal, absensi, mading, dan komunikasi.

## 🎨 Design System

- **Primary Color**: `#2ec4b6` (Teal)
- **Secondary Color**: `#1a1a2e` (Dark Navy)
- **Font**: Sharp Sans

## ✨ Fitur Utama

### 👑 Untuk Ketua Tingkat
- ✅ Kelola jadwal matakuliah
- ✅ Kelola data anggota kelas (per angkatan)
- ✅ Monitor absensi anggota
- ✅ Kelola mading digital
- ✅ Post pengumuman & notifikasi
- ✅ Buat & kelola assignment
- ✅ Lihat analytics & reporting

### 👥 Untuk Anggota Kelas
- ✅ Lihat jadwal matakuliah
- ✅ Submit absensi dengan NIM (auto-timestamp)
- ✅ Pilih/checklist matakuliah sesuai KRS
- ✅ Lihat mading kelas
- ✅ Akses forum diskusi
- ✅ Lihat pengumuman & deadline
- ✅ Download materi & file kelas

## 📋 Daftar Fitur

1. **Dashboard & Overview** - Ringkasan aktivitas kelas
2. **Jadwal Matakuliah** - Kelola & lihat jadwal kuliah
3. **Manajemen Anggota** - Data per angkatan dengan profil
4. **Sistem Absensi** - Auto-generated per NIM dengan jam absen
5. **Pengumuman & Notifikasi** - Update info real-time
6. **Assignment & Deadline** - Tugas dan tracking
7. **Forum Diskusi & Chat** - Komunikasi kelas
8. **Mading Digital** - Papan pengumuman interaktif
9. **Direktori Kontak** - Phonebook digital
10. **File Sharing** - Dokumentasi & materi kelas
11. **KRS Selection** - Checklist matakuliah per anggota
12. **Analytics & Reporting** - Laporan aktivitas
13. **Role-Based Access** - Permission berbeda per role

## 📁 Struktur Project

```
Ketua-Tingkat-App/
├── frontend/              # React/Vue frontend
├── backend/               # Node.js/Express backend
├── database/              # Database schema & migrations
├── docs/                  # Dokumentasi
└── README.md
```

## 🚀 Teknologi Stack

- **Frontend**: React.js + Tailwind CSS
- **Backend**: Node.js + Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT
- **Real-time**: Socket.io
- **Notification**: Firebase/Node-mailer

## 📦 Instalasi

```bash
# Clone repository
git clone https://github.com/MuthiaSyifa1002/Ketua-Tingkat-App.git

# Install dependencies
cd Ketua-Tingkat-App
npm install

# Setup environment variables
cp .env.example .env

# Run development server
npm run dev
```

## 📄 Lisensi

MIT License

---

**Created with ❤️ by Muthia Syifa**