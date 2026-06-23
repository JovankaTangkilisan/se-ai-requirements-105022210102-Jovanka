# Assumptions — Student Task Management System

Dokumen ini mencatat semua asumsi yang dibuat selama proses requirements engineering.  
Sesuai ketentuan kasus, **semua asumsi yang tidak berasal dari kasus wajib ditandai secara eksplisit** dengan label `[ASUMSI]`.

---

## 1. Asumsi Pengguna & Akses

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-01 | `[ASUMSI]` Setiap pengguna (dosen, mahasiswa, administrator) memiliki akun unik dengan kredensial login (username/email dan password). | Tidak dari kasus |
| A-02 | `[ASUMSI]` Sistem menggunakan mekanisme autentikasi berbasis sesi atau token (misal: JWT) untuk menjaga keamanan akses. | Tidak dari kasus |
| A-03 | `[ASUMSI]` Setiap pengguna hanya dapat mengakses fitur sesuai perannya masing-masing (role-based access control). | Tidak dari kasus |
| A-04 | `[ASUMSI]` Administrator dapat membuat, menonaktifkan, dan menghapus akun pengguna. | Tidak dari kasus |

---

## 2. Asumsi Tugas & Pengumpulan

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-05 | `[ASUMSI]` Tugas yang dibuat dosen terhubung dengan mata kuliah tertentu yang dikelola oleh administrator. | Tidak dari kasus |
| A-06 | `[ASUMSI]` Mahasiswa hanya dapat melihat dan mengumpulkan tugas pada mata kuliah yang mereka ikuti. | Tidak dari kasus |
| A-07 | `[ASUMSI]` Format file yang dapat dikumpulkan mahasiswa dibatasi pada tipe tertentu (misal: PDF, DOCX, ZIP). | Tidak dari kasus |
| A-08 | `[ASUMSI]` Terdapat batas ukuran file yang dapat diunggah oleh mahasiswa. | Tidak dari kasus |
| A-09 | `[ASUMSI]` Mahasiswa hanya dapat mengumpulkan tugas sebelum atau pada batas waktu deadline yang ditetapkan dosen. | Tidak dari kasus |
| A-10 | `[ASUMSI]` Sistem mencatat timestamp pengumpulan tugas untuk keperluan validasi ketepatan waktu. | Tidak dari kasus |

---

## 3. Asumsi Penilaian & Umpan Balik

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-11 | `[ASUMSI]` Penilaian dilakukan oleh dosen secara manual melalui antarmuka sistem. | Tidak dari kasus |
| A-12 | `[ASUMSI]` Nilai yang diberikan dosen berupa angka atau huruf sesuai skala yang berlaku di kampus. | Tidak dari kasus |
| A-13 | `[ASUMSI]` Umpan balik dosen dapat berupa teks dan/atau file yang dilampirkan. | Tidak dari kasus |
| A-14 | `[ASUMSI]` Mahasiswa dapat melihat nilai dan umpan balik setelah dosen mempublikasikannya. | Tidak dari kasus |

---

## 4. Asumsi Deadline & Notifikasi

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-15 | `[ASUMSI]` Deadline tugas mencakup tanggal dan waktu (bukan hanya tanggal). | Tidak dari kasus |
| A-16 | `[ASUMSI]` Sistem mengirimkan notifikasi pengingat kepada mahasiswa menjelang deadline tugas. | Tidak dari kasus |
| A-17 | `[ASUMSI]` Notifikasi dapat disampaikan melalui antarmuka sistem (in-app notification) dan/atau email. | Tidak dari kasus |

---

## 5. Asumsi Pelaporan

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-18 | `[ASUMSI]` Fitur pelaporan mencakup rekap status pengumpulan tugas per mata kuliah dan per mahasiswa. | Tidak dari kasus |
| A-19 | `[ASUMSI]` Laporan dapat diakses oleh dosen (untuk mata kuliah yang diampu) dan administrator (untuk seluruh data). | Tidak dari kasus |
| A-20 | `[ASUMSI]` Laporan dapat diekspor dalam format tertentu (misal: PDF atau Excel). | Tidak dari kasus |

---

## 6. Asumsi Teknis & Infrastruktur

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-21 | `[ASUMSI]` Sistem berbasis web dan dapat diakses melalui browser tanpa instalasi tambahan. | Tidak dari kasus |
| A-22 | `[ASUMSI]` Sistem menggunakan basis data relasional untuk menyimpan data pengguna, tugas, dan nilai. | Tidak dari kasus |
| A-23 | `[ASUMSI]` File yang diunggah mahasiswa disimpan di server atau layanan penyimpanan yang dikelola kampus. | Tidak dari kasus |
| A-24 | `[ASUMSI]` Sistem dapat diakses secara bersamaan oleh banyak pengguna (multi-user concurrent access). | Tidak dari kasus |
| A-25 | `[ASUMSI]` Sistem memiliki mekanisme backup data secara berkala untuk menjaga data integrity dan reliability. | Tidak dari kasus |

---

## 7. Asumsi Akademik & Organisasi

| ID   | Pernyataan                                                                                          | Sumber        |
|------|-----------------------------------------------------------------------------------------------------|---------------|
| A-26 | `[ASUMSI]` Satu mata kuliah dapat diasuh oleh satu atau lebih dosen. | Tidak dari kasus |
| A-27 | `[ASUMSI]` Satu mata kuliah dapat diikuti oleh banyak mahasiswa. | Tidak dari kasus |
| A-28 | `[ASUMSI]` Struktur akademik (semester, program studi) dikelola oleh administrator dalam konfigurasi sistem. | Tidak dari kasus |

---

## Catatan

- Semua asumsi di atas berstatus **tentatif** dan harus divalidasi dengan pemangku kepentingan nyata (dosen, mahasiswa, pihak kampus) sebelum dijadikan dasar perancangan sistem.
- Jika terdapat asumsi yang keliru atau bertentangan dengan kebijakan kampus, asumsi tersebut wajib direvisi dan dokumen ini diperbarui.
