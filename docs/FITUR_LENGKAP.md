# 📋 Dokumentasi Fitur Lengkap - Ketua Tingkat App

## 1️⃣ Dashboard & Overview

### Ketua Tingkat
- 📊 Ringkasan aktivitas kelas (upcoming events, assignments, announcements)
- 📈 Statistik kehadiran anggota
- 🔔 Widget notifikasi real-time
- 📅 Calendar view mingguan/bulanan

### Anggota
- 📊 Jadwal kelas hari ini
- 🔔 Notifikasi assignment & deadline
- 📅 Calendar personal

---

## 2️⃣ Manajemen Jadwal Matakuliah

### Ketua Tingkat
- 📚 Buat daftar matakuliah (kode, nama, SKS, dosen, ruang, hari, jam)
- 🕐 Kelola jadwal kuliah
- 🔄 Edit/duplikasi jadwal
- ⚠️ Set alert untuk perubahan jadwal
- 📥 Import jadwal dari file Excel
- 📤 Export jadwal ke PDF/Excel
- 🔗 Sinkronisasi ke Google Calendar

### Anggota
- 📖 Lihat jadwal matakuliah
- 🔄 Filter by hari/jam
- 📌 Pin jadwal favorit
- 📥 Export ke kalender pribadi

---

## 3️⃣ Manajemen Kelas & Anggota

### Struktur Data Anggota
- 👤 Nama lengkap
- 🆔 NIM (Nomor Induk Mahasiswa)
- 📚 Angkatan (misal: 2021, 2022, 2023)
- 📋 Status keanggotaan (Aktif, Tidak Aktif, Graduated)
- 📞 Kontak (Nomor HP, Email)
- 🌐 Media sosial (Instagram, Line, WhatsApp)
- 📍 Alamat tinggal
- 📷 Foto profil

### Ketua Tingkat
- 👥 Lihat daftar anggota per angkatan
- ➕ Tambah anggota baru
- ✏️ Edit profil anggota
- 🗑️ Hapus/deactivate anggota
- 📊 Statistik anggota per angkatan
- 📥 Bulk import dari file Excel

### Anggota
- 👤 Lihat profil sendiri
- ✏️ Edit profil pribadi
- 👥 Lihat daftar anggota lain
- 🔍 Search anggota

---

## 4️⃣ Sistem Kehadiran & Absensi

### Database Absensi (Auto-Generated per NIM)
```
Kolom: NIM | Nama | Tanggal | Jam Masuk | Status | Catatan
```

### Ketua Tingkat
- 📋 Lihat laporan absensi lengkap
- 📊 Analisis pola kehadiran per anggota
- 🔍 Filter by tanggal, status, angkatan
- 📈 Statistik kehadiran (persentase, trend)
- 🏆 Leaderboard kehadiran terbaik
- 📥 Export laporan ke Excel/PDF
- ⚠️ Notifikasi untuk yang sering absen

### Anggota
- ✅ Submit absensi (input NIM, otomatis capture timestamp)
- 📋 Lihat riwayat absensi pribadi
- 🔔 Notifikasi konfirmasi absensi
- 📊 Statistik kehadiran pribadi

---

## 5️⃣ Pengumuman & Notifikasi

### Ketua Tingkat
- 📢 Buat pengumuman baru
- 🏷️ Kategori (Akademik, Sosial, Urgent, Event)
- ⏰ Scheduled posting (post otomatis)
- 📌 Pin pengumuman penting
- ✏️ Edit/hapus pengumuman
- 📊 Tracking read status
- 🔔 Send notifikasi via push/email/in-app

### Anggota
- 📖 Lihat pengumuman
- 🔔 Filter by kategori
- 👁️ Mark as read/unread
- 💬 Comment pada pengumuman
- ⭐ Favorite/bookmark

---

## 6️⃣ Manajemen Tugas & Deadline

### Ketua Tingkat
- 📝 Buat assignment dengan deskripsi detail
- ⏱️ Set deadline & reminder
- 📎 Upload file attachment
- ✍️ Track submission status
- 💬 Comment & feedback
- 🔔 Notifikasi reminder otomatis
- 📊 Submission analytics

### Anggota
- 📋 Lihat daftar assignment
- 📥 Download materi/attachment
- ✏️ Submit tugas
- 💬 Lihat feedback dari ketua
- ⏰ Countdown deadline

---

## 7️⃣ Forum Diskusi & Chat

### Fitur
- 💬 Channel-based discussion (per matakuliah, per topik)
- 🧵 Thread discussions
- 📎 Share file & links
- 😊 Emoji reactions
- 🔖 Bookmark/save posts
- 🔍 Search discussions
- 👤 Mention users (@mention)
- 🚫 Moderation tools (delete, pin, mute)

### Ketua Tingkat
- ➕ Buat channel baru
- 🎯 Manage channel members
- 📌 Pin important discussions
- 🗑️ Delete inappropriate posts
- 👁️ Moderate discussions

### Anggota
- 💬 Participate dalam channel
- 🧵 Create & reply threads
- 📎 Share resources
- 🔔 Get notified on mentions

---

## 8️⃣ Mading Digital

### Interface
- 📰 Tampilan seperti papan pengumuman tradisional
- 🎨 Berbentuk poster/card-based layout
- 📌 Pin multiple posts

### Ketua Tingkat
- ➕ Tambah post ke mading
- ✏️ Edit post yang sudah ada
- 🗑️ Hapus post
- 🖼️ Upload gambar/video
- 📐 Customize layout & background
- 📊 View analytics (views, reactions)
- 🔄 Drag & drop untuk arrange posts

### Anggota
- 👁️ Lihat mading kelas
- 💬 Like/react pada post
- 🔔 Get notified on new posts
- 📸 View post details

---

## 9️⃣ Direktori & Kontak

### Fitur
- 📖 Phonebook digital kelas
- 🔍 Search & filter cepat
- 📱 Kontak details (phone, email, IG, Line, WA)
- 🗺️ Location-based (alamat tinggal)
- 📥 Export kontak
- 🔐 Privacy controls (private/public)

---

## 🔟 Dokumentasi & File Sharing

### Ketua Tingkat
- ➕ Upload materi kelas
- 📁 Organize dalam folder
- ✏️ Edit metadata
- 🔐 Set permission (public/private)
- 🗑️ Hapus file
- 👁️ Track downloads

### Anggota
- 👁️ Browse & search file
- 📥 Download materi
- ⭐ Favorite documents

---

## 1️⃣1️⃣ KRS Selection (Checklist Matakuliah)

### Fitur
- ✅ Anggota bisa checklist matakuliah sesuai KRS
- 📋 Daftar matakuliah yang dibuat ketua tingkat
- 🔄 Update status KRS kapan saja
- 📊 Admin dapat melihat KRS per anggota
- 📥 Export KRS summary

### Ketua Tingkat
- 📊 Lihat KRS per anggota
- 📈 Analytics enrollment per matakuliah
- 🔍 Identify course conflicts
- 📥 Export report

### Anggota
- ✅ Checklist matakuliah saat pendaftaran
- 🔄 Update KRS kapan saja
- 📋 Lihat KRS pribadi
- 📥 Export sertifikat KRS

---

## 1️⃣2️⃣ Analytics & Reporting

### Dashboard Analytics (Ketua Tingkat)
- 📊 Class engagement metrics
- 📈 Attendance statistics
- 👥 Member activity tracking
- 🎯 Course enrollment analytics
- 💬 Discussion activity
- 📝 Assignment submission rate
- 🏆 Top performers

---

## 🎨 Design & UI/UX

- **Primary Color**: #2ec4b6 (Teal)
- **Secondary Color**: #1a1a2e (Dark Navy)
- **Font**: Sharp Sans
- **Typography**: Clear hierarchy
- **Icons**: Consistent iconography
- **Spacing**: Generous whitespace
- **Animations**: Smooth transitions
- **Accessibility**: WCAG compliant

---

**Last Updated**: 2026-06-11