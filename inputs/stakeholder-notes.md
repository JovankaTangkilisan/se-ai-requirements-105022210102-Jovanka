# Stakeholder Notes — Student Task Management System

## 1. Identifikasi Stakeholder

Berdasarkan deskripsi kasus, terdapat tiga stakeholder utama yang berinteraksi langsung dengan sistem:

| No | Stakeholder     | Peran dalam Sistem                                                                 |
|----|-----------------|------------------------------------------------------------------------------------|
| 1  | Dosen           | Membuat tugas, menetapkan deadline, memberikan nilai dan umpan balik               |
| 2  | Mahasiswa       | Melihat tugas, mengumpulkan file, memantau status dan deadline                     |
| 3  | Administrator   | Mengelola pengguna, mata kuliah, dan konfigurasi sistem                            |

---

## 2. Catatan per Stakeholder

### 2.1 Dosen

**Kebutuhan utama (dari kasus):**
- Membuat tugas perkuliahan
- Menetapkan deadline tugas
- Memberikan nilai kepada mahasiswa
- Memberikan umpan balik atas pengumpulan tugas

**Kepentingan sistem:**
- Kemudahan dalam mengelola dan mendistribusikan tugas ke mahasiswa
- Efisiensi proses penilaian dan pemberian umpan balik
- Visibilitas terhadap status pengumpulan tugas mahasiswa

---

### 2.2 Mahasiswa

**Kebutuhan utama (dari kasus):**
- Melihat tugas yang diberikan dosen
- Mengumpulkan file tugas melalui sistem
- Memantau status pengumpulan dan deadline tugas

**Kepentingan sistem:**
- Kemudahan akses informasi tugas dan tenggat waktu
- Transparansi status pengumpulan dan penilaian
- Notifikasi atau pengingat terkait deadline

---

### 2.3 Administrator

**Kebutuhan utama (dari kasus):**
- Mengelola data pengguna (dosen dan mahasiswa)
- Mengelola data mata kuliah
- Mengonfigurasi sistem

**Kepentingan sistem:**
- Kontrol penuh terhadap manajemen akun dan hak akses
- Kemampuan mengatur struktur akademik (mata kuliah, kelas)
- Stabilitas dan keamanan sistem secara keseluruhan

---

## 3. Atribut Kualitas Sistem (dari kasus)

Sistem harus memperhatikan aspek-aspek berikut yang berdampak pada semua stakeholder:

| Atribut        | Relevansi                                                                 |
|----------------|---------------------------------------------------------------------------|
| Usability      | Antarmuka mudah digunakan oleh dosen, mahasiswa, dan administrator        |
| Security       | Perlindungan data pengguna, tugas, nilai, dan akses sistem                |
| Performance    | Sistem responsif saat diakses banyak pengguna secara bersamaan            |
| Reliability    | Sistem tersedia dan berfungsi konsisten, terutama menjelang deadline      |
| Data Integrity | Data tugas, pengumpulan, dan nilai harus akurat dan tidak rusak/hilang    |

---

## 4. Konteks Penggunaan

- Sistem digunakan dalam lingkungan **kampus** (akademik)
- Mencakup proses: pengelolaan tugas, pengumpulan tugas, penilaian, tenggat waktu, dan pelaporan
- Peran Requirements Engineer dijalankan oleh mahasiswa dengan bantuan AI
