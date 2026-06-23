# Inception Document: Student Task Management System

**Versi:** 1.0  
**Tanggal:** [BELUM DIDEFINISIKAN — diperlukan klarifikasi]  
**Penulis:** Codex  
**Status:** Draft

---

## 1. Masalah Bisnis

### 1.1 Latar Belakang
Student Task Management System adalah aplikasi kampus untuk mendukung dosen, mahasiswa, dan administrator dalam mengelola tugas perkuliahan, pengumpulan tugas, penilaian, tenggat waktu, dan pelaporan.

### 1.2 Problem Statement
Saat ini, dosen, mahasiswa, dan administrator mengalami proses pengelolaan tugas perkuliahan yang belum terpusat yang menyebabkan pengelolaan tugas, pengumpulan file, penilaian, dan pelaporan menjadi kurang efisien serta berisiko menurunkan akurasi data dan kepatuhan terhadap deadline. Hal ini terjadi karena sistem belum didefinisikan secara formal untuk menangani seluruh alur tersebut dalam satu platform terintegrasi.

### 1.3 Dampak Bisnis
- Proses pemberian dan pengumpulan tugas menjadi lebih lambat.
- Risiko keterlambatan pengumpulan dan penilaian meningkat.
- Informasi status tugas, nilai, dan deadline berpotensi tidak konsisten.
- Administrator lebih sulit mengelola pengguna, mata kuliah, dan konfigurasi sistem secara terpusat.

---

## 2. Tujuan Proyek

### 2.1 Business Goals
| ID | Tujuan | Metrik Keberhasilan | Target |
|----|--------|---------------------|--------|
| BG-01 | Memusatkan pengelolaan tugas perkuliahan | Seluruh proses pembuatan, pengumpulan, dan penilaian tugas dilakukan melalui sistem | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| BG-02 | Meningkatkan visibilitas status tugas bagi mahasiswa dan dosen | Persentase tugas yang memiliki status dan deadline yang dapat dilihat di sistem | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| BG-03 | Mendukung pelaporan akademik yang lebih mudah | Laporan pengumpulan tugas dapat dihasilkan dari sistem | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |

### 2.2 Project Objectives
| ID | Objektif | Terukur? | Deadline |
|----|----------|----------|----------|
| OBJ-01 | Mendefinisikan alur pengelolaan tugas untuk dosen, mahasiswa, dan administrator | Ya | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| OBJ-02 | Mendefinisikan kebutuhan akses pengguna berdasarkan peran | Ya | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| OBJ-03 | Mendefinisikan kebutuhan pelaporan status pengumpulan dan penilaian | Ya | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |

---

## 3. Stakeholder

| ID | Nama / Peran | Jenis | Kepentingan | Tingkat Keterlibatan |
|----|-------------|-------|-------------|----------------------|
| STK-01 | Dosen | Internal | Membuat tugas, menetapkan deadline, memberi nilai, memberi umpan balik | Tinggi |
| STK-02 | Mahasiswa | Internal | Melihat tugas, mengumpulkan file, memantau status dan deadline | Tinggi |
| STK-03 | Administrator | Internal | Mengelola pengguna, mata kuliah, dan konfigurasi sistem | Tinggi |

**Keterangan Tingkat Keterlibatan:**
- Tinggi: Terlibat dalam keputusan dan review rutin
- Sedang: Dikonsultasikan pada milestone tertentu
- Rendah: Diinformasikan pada akhir fase

---

## 4. Scope

### 4.1 Dalam Scope (In Scope)
| ID | Fitur / Kapabilitas | Prioritas |
|----|---------------------|-----------|
| SC-IN-01 | Dosen dapat membuat tugas perkuliahan | Must Have |
| SC-IN-02 | Dosen dapat menetapkan deadline tugas | Must Have |
| SC-IN-03 | Mahasiswa dapat melihat tugas | Must Have |
| SC-IN-04 | Mahasiswa dapat mengumpulkan file tugas | Must Have |
| SC-IN-05 | Mahasiswa dapat memantau status pengumpulan dan deadline | Must Have |
| SC-IN-06 | Dosen dapat memberikan nilai dan umpan balik | Must Have |
| SC-IN-07 | Administrator dapat mengelola pengguna | Must Have |
| SC-IN-08 | Administrator dapat mengelola mata kuliah | Must Have |
| SC-IN-09 | Administrator dapat mengonfigurasi sistem | Must Have |
| SC-IN-10 | Sistem menyediakan pelaporan tugas | Should Have |

### 4.2 Di Luar Scope (Out of Scope)
| ID | Yang Tidak Dikerjakan | Alasan |
|----|----------------------|--------|
| SC-OUT-01 | Fitur yang tidak terkait dengan pengelolaan tugas, pengumpulan, penilaian, deadline, atau pelaporan | Belum didefinisikan dalam kasus |
| SC-OUT-02 | Integrasi eksternal yang tidak disebutkan dalam kasus | Tidak ada dasar informasi pada input yang diberikan |

### 4.3 Batasan Scope
Sistem ini menangani proses pengelolaan tugas perkuliahan, pengumpulan tugas, penilaian, tenggat waktu, dan pelaporan di lingkungan kampus. Sistem berinteraksi dengan tiga peran utama: dosen, mahasiswa, dan administrator. Detail integrasi dengan sistem lain, format dokumen resmi, serta aturan operasional kampus belum didefinisikan dalam input yang tersedia.

---

## 5. Asumsi

| ID | Asumsi | Dampak jika Salah | Pemilik Validasi |
|----|--------|-------------------|-----------------|
| ASM-01 | `[ASUMSI]` Setiap pengguna memiliki akun unik dengan kredensial login. | Akses dan identitas pengguna perlu didesain ulang. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-02 | `[ASUMSI]` Sistem memakai autentikasi berbasis sesi atau token. | Mekanisme keamanan dan implementasi login berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-03 | `[ASUMSI]` Setiap pengguna hanya dapat mengakses fitur sesuai perannya. | Model otorisasi perlu disesuaikan. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-04 | `[ASUMSI]` Administrator dapat membuat, menonaktifkan, dan menghapus akun pengguna. | Ruang lingkup manajemen akun berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-05 | `[ASUMSI]` Tugas terhubung dengan mata kuliah tertentu. | Struktur data tugas dan relasinya berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-06 | `[ASUMSI]` Mahasiswa hanya dapat melihat dan mengumpulkan tugas pada mata kuliah yang diikuti. | Aturan akses tugas perlu diubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-07 | `[ASUMSI]` Sistem membatasi format file unggahan pada tipe tertentu. | Validasi upload dan penyimpanan file perlu ditentukan ulang. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-08 | `[ASUMSI]` Ada batas ukuran file unggahan. | Desain penyimpanan dan validasi upload terdampak. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-09 | `[ASUMSI]` Mahasiswa hanya dapat mengumpulkan tugas sebelum atau pada deadline. | Logika pengumpulan terlambat perlu didefinisikan ulang. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-10 | `[ASUMSI]` Sistem mencatat timestamp pengumpulan tugas. | Mekanisme audit dan validasi ketepatan waktu wajib ada. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-11 | `[ASUMSI]` Penilaian dilakukan manual oleh dosen melalui sistem. | Alur penilaian perlu diubah jika ada otomasi. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-12 | `[ASUMSI]` Nilai berupa angka atau huruf sesuai skala kampus. | Format data nilai perlu disesuaikan. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-13 | `[ASUMSI]` Umpan balik dosen dapat berupa teks dan/atau file. | Model penyimpanan feedback berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-14 | `[ASUMSI]` Mahasiswa dapat melihat nilai dan umpan balik setelah dipublikasikan. | Aturan visibilitas hasil penilaian berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-15 | `[ASUMSI]` Deadline tugas mencakup tanggal dan waktu. | Ketepatan waktu pengumpulan harus ditetapkan lebih presisi. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-16 | `[ASUMSI]` Sistem mengirim pengingat menjelang deadline. | Notifikasi menjadi kebutuhan formal. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-17 | `[ASUMSI]` Notifikasi tersedia di sistem dan/atau email. | Kanal komunikasi perlu dipastikan. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-18 | `[ASUMSI]` Pelaporan mencakup rekap status pengumpulan per mata kuliah dan per mahasiswa. | Ruang lingkup laporan bisa lebih luas atau lebih sempit. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-19 | `[ASUMSI]` Laporan dapat diakses oleh dosen dan administrator. | Hak akses laporan perlu direvisi. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-20 | `[ASUMSI]` Laporan dapat diekspor ke format tertentu. | Kebutuhan export harus ditentukan. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-21 | `[ASUMSI]` Sistem berbasis web. | Platform implementasi berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-22 | `[ASUMSI]` Sistem menggunakan basis data relasional. | Desain data dan query berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-23 | `[ASUMSI]` File unggahan disimpan di server atau layanan kampus. | Arsitektur penyimpanan berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-24 | `[ASUMSI]` Sistem mendukung akses bersamaan dari banyak pengguna. | Kebutuhan performa dan kapasitas berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-25 | `[ASUMSI]` Sistem memiliki backup data berkala. | Strategi reliability dan recovery berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-26 | `[ASUMSI]` Satu mata kuliah dapat diasuh oleh satu atau lebih dosen. | Model relasi pengajar-mata kuliah berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-27 | `[ASUMSI]` Satu mata kuliah dapat diikuti oleh banyak mahasiswa. | Struktur enrolment berubah. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |
| ASM-28 | `[ASUMSI]` Struktur akademik dikelola administrator. | Data organisasi akademik perlu dipastikan. | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] |

> ⚠️ Semua asumsi harus divalidasi sebelum fase requirement dimulai.

---

## 6. Constraint

### 6.1 Constraint Bisnis
| ID | Constraint | Sumber | Fleksibilitas |
|----|------------|--------|---------------|
| CON-BIZ-01 | Sistem harus mendukung kebutuhan dosen, mahasiswa, dan administrator dalam proses akademik kampus | CASE.md | Terbatas |
| CON-BIZ-02 | Sistem harus memperhatikan usability | CASE.md | Tidak |

### 6.2 Constraint Teknis
| ID | Constraint | Sumber | Fleksibilitas |
|----|------------|--------|---------------|
| CON-TEC-01 | Sistem harus memperhatikan security | CASE.md | Tidak |
| CON-TEC-02 | Sistem harus memperhatikan performance | CASE.md | Tidak |
| CON-TEC-03 | Sistem harus memperhatikan reliability | CASE.md | Tidak |
| CON-TEC-04 | Sistem harus menjaga data integrity | CASE.md | Tidak |

### 6.3 Constraint Regulasi / Kepatuhan
| ID | Regulasi / Standar | Berlaku untuk | Catatan |
|----|-------------------|--------------|---------|
| CON-REG-01 | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Seluruh sistem | Tidak ada regulasi spesifik yang disebutkan pada input |

---

## 7. Open Questions

| ID | Pertanyaan | Pemilik | Deadline Jawaban | Dampak jika Tidak Dijawab |
|----|-----------|---------|-----------------|--------------------------|
| OQ-01 | Kapan tanggal versi awal dokumen ini disahkan? | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Rendah |
| OQ-02 | Apakah ada deadline proyek atau target rilis? | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Tinggi |
| OQ-03 | Format dan batas ukuran file unggahan apa yang akan didukung? | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Sedang |
| OQ-04 | Apakah sistem perlu notifikasi, dan jika ya, kanal apa yang wajib digunakan? | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Sedang |
| OQ-05 | Format laporan apa yang dibutuhkan oleh dosen dan administrator? | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | [BELUM DIDEFINISIKAN — diperlukan klarifikasi] | Sedang |

---

## 8. Ringkasan Risiko Awal (Opsional)

| ID | Risiko | Kemungkinan | Dampak | Mitigasi Awal |
|----|--------|-------------|--------|--------------|
| RSK-01 | Ketentuan upload file belum lengkap | Tinggi | Sedang | Tetapkan format dan batas ukuran file sejak awal |
| RSK-02 | Hak akses peran belum dipastikan sepenuhnya | Sedang | Tinggi | Validasi model role-based access control sebelum desain rinci |
| RSK-03 | Kebutuhan laporan belum spesifik | Tinggi | Sedang | Definisikan format laporan dan pemilik penggunaannya |

---

## 9. Referensi

- CASE.md
- assumptions.md
- stakeholder-notes.md

---

*Dokumen ini adalah living document. Perubahan harus melalui persetujuan [BELUM DIDEFINISIKAN — diperlukan klarifikasi].*
