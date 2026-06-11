# 🗄️ Database Schema - Ketua Tingkat App

## 📋 Tabel Utama

### 1. Users
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  nama_lengkap VARCHAR(255) NOT NULL,
  nim VARCHAR(20),
  role ENUM('ketua_tingkat', 'wakil_ketua', 'anggota'),
  angkatan INT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 2. Anggota Kelas
```sql
CREATE TABLE anggota_kelas (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  nim VARCHAR(20) UNIQUE NOT NULL,
  nama_lengkap VARCHAR(255) NOT NULL,
  angkatan INT NOT NULL,
  status ENUM('aktif', 'tidak_aktif', 'graduated') DEFAULT 'aktif',
  no_hp VARCHAR(15),
  email VARCHAR(255),
  instagram VARCHAR(100),
  line_id VARCHAR(100),
  whatsapp VARCHAR(15),
  alamat TEXT,
  foto_profil VARCHAR(255),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 3. Matakuliah
```sql
CREATE TABLE matakuliah (
  id UUID PRIMARY KEY,
  kode_mk VARCHAR(20) UNIQUE NOT NULL,
  nama_mk VARCHAR(255) NOT NULL,
  sks INT NOT NULL,
  dosen_pengampu VARCHAR(255),
  ruang_kelas VARCHAR(50),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 4. Jadwal Kuliah
```sql
CREATE TABLE jadwal_kuliah (
  id UUID PRIMARY KEY,
  matakuliah_id UUID REFERENCES matakuliah(id),
  hari ENUM('Senin', 'Selasa', 'Rabu', 'Kamis', 'Jumat', 'Sabtu', 'Minggu'),
  jam_mulai TIME NOT NULL,
  jam_selesai TIME NOT NULL,
  ruang VARCHAR(50),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 5. Absensi
```sql
CREATE TABLE absensi (
  id UUID PRIMARY KEY,
  anggota_id UUID REFERENCES anggota_kelas(id),
  nim VARCHAR(20) NOT NULL,
  nama VARCHAR(255) NOT NULL,
  tanggal DATE NOT NULL,
  jam_masuk TIME NOT NULL,
  status ENUM('hadir', 'terlambat', 'izin', 'sakit', 'alpa') DEFAULT 'hadir',
  catatan TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  UNIQUE(nim, tanggal)
);
```

### 6. Pengumuman
```sql
CREATE TABLE pengumuman (
  id UUID PRIMARY KEY,
  ketua_id UUID REFERENCES users(id),
  judul VARCHAR(255) NOT NULL,
  isi TEXT NOT NULL,
  kategori ENUM('akademik', 'sosial', 'urgent', 'event') DEFAULT 'akademik',
  is_pinned BOOLEAN DEFAULT FALSE,
  scheduled_at TIMESTAMP,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 7. Assignment
```sql
CREATE TABLE assignment (
  id UUID PRIMARY KEY,
  ketua_id UUID REFERENCES users(id),
  judul VARCHAR(255) NOT NULL,
  deskripsi TEXT,
  deadline TIMESTAMP NOT NULL,
  file_attachment VARCHAR(255),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 8. Assignment Submission
```sql
CREATE TABLE assignment_submission (
  id UUID PRIMARY KEY,
  assignment_id UUID REFERENCES assignment(id),
  anggota_id UUID REFERENCES anggota_kelas(id),
  file_submission VARCHAR(255),
  submitted_at TIMESTAMP,
  status ENUM('pending', 'submitted', 'graded') DEFAULT 'pending',
  grade INT,
  feedback TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 9. Forum Diskusi
```sql
CREATE TABLE forum_channel (
  id UUID PRIMARY KEY,
  nama_channel VARCHAR(255) NOT NULL,
  deskripsi TEXT,
  tipe ENUM('umum', 'matakuliah', 'topik') DEFAULT 'umum',
  created_by UUID REFERENCES users(id),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 10. Mading Posts
```sql
CREATE TABLE mading_posts (
  id UUID PRIMARY KEY,
  ketua_id UUID REFERENCES users(id),
  judul VARCHAR(255) NOT NULL,
  isi TEXT,
  gambar VARCHAR(255),
  video VARCHAR(255),
  position INT,
  is_active BOOLEAN DEFAULT TRUE,
  views INT DEFAULT 0,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 11. KRS Selection
```sql
CREATE TABLE krs_selection (
  id UUID PRIMARY KEY,
  anggota_id UUID REFERENCES anggota_kelas(id),
  matakuliah_id UUID REFERENCES matakuliah(id),
  selected BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  UNIQUE(anggota_id, matakuliah_id)
);
```

### 12. File Sharing
```sql
CREATE TABLE file_sharing (
  id UUID PRIMARY KEY,
  ketua_id UUID REFERENCES users(id),
  nama_file VARCHAR(255) NOT NULL,
  deskripsi TEXT,
  file_path VARCHAR(255) NOT NULL,
  kategori VARCHAR(100),
  permission ENUM('public', 'private') DEFAULT 'public',
  download_count INT DEFAULT 0,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

**Last Updated**: 2026-06-11