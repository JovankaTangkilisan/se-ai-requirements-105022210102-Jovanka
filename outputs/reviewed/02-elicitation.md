# Laporan Elicitation: Student Task Management System

## 1. Tujuan Elicitation
- Tujuan: Menurunkan kebutuhan stakeholder menjadi kebutuhan eksplisit, implisit, requirement fungsional, dan non-fungsional yang traceable.
- Tujuan bisnis: Mendukung pengelolaan tugas perkuliahan, pengumpulan tugas, penilaian, tenggat waktu, dan pelaporan di lingkungan kampus.
- Stakeholder: Dosen, mahasiswa, administrator.
- Scope: Proses pengelolaan tugas, pengumpulan file, penilaian, deadline, pengelolaan pengguna, pengelolaan mata kuliah, konfigurasi sistem, dan pelaporan.

## 2. Konteks yang Ditinjau
| Source ID | Jenis Sumber | Ringkasan | Relevansi |
|---|---|---|---|
| SRC-001 | CASE.md | Menjelaskan Student Task Management System, peran dosen, mahasiswa, administrator, dan atribut kualitas sistem | Sumber utama tujuan sistem, stakeholder, dan constraint kualitas |
| SRC-002 | SKILL.md | Panduan elicitation, format output, rules, quality checks, dan failure conditions | Acuan struktur dan aturan output |
| SRC-003 | assumptions.md | Daftar asumsi awal tentang autentikasi, RBAC, tugas, upload, penilaian, notifikasi, reporting, dan infrastruktur | Sumber asumsi eksplisit yang perlu ditandai dan divalidasi |
| SRC-004 | stakeholder-notes.md | Catatan kebutuhan dan kepentingan per stakeholder serta atribut kualitas sistem | Sumber utama kebutuhan stakeholder dan quality attribute |

## 3. Teknik Elicitation
| Technique ID | Teknik | Tujuan | Stakeholder / Sumber | Alasan Pemilihan |
|---|---|---|---|---|
| TECH-001 | Interview terstruktur | Menggali tujuan, workflow, pain point, aturan, exception, dan prioritas | Dosen, mahasiswa, administrator | Paling sesuai untuk memahami kebutuhan per peran |
| TECH-002 | Document analysis | Mengekstrak kebutuhan dari CASE.md, assumptions.md, dan stakeholder-notes.md | SRC-001, SRC-003, SRC-004 | Bukti tertulis sudah tersedia dan cukup untuk menurunkan requirement awal |
| TECH-003 | Gap analysis | Mengidentifikasi hal yang belum jelas atau belum tervalidasi | Semua sumber | Diperlukan untuk menandai asumsi dan open question |

## 4. Pertanyaan Wawancara
### 4.1 Pertanyaan Umum
- Q1: Apa tujuan paling penting yang ingin dicapai sistem ini untuk kampus?
- Q2: Bagian mana dari proses tugas yang paling sering menimbulkan masalah saat ini?
- Q3: Informasi apa yang harus selalu tersedia untuk semua peran?

### 4.2 Pertanyaan Berdasarkan Peran
| Question ID | Peran Stakeholder | Pertanyaan | Tujuan | Pemicu Follow-Up |
|---|---|---|---|---|
| Q-001 | Dosen | Data apa saja yang wajib diisi saat membuat tugas? | Menentukan input requirement | Jika ada field wajib atau aturan validasi khusus |
| Q-002 | Dosen | Bagaimana deadline ditetapkan dan apakah perlu tanggal serta waktu? | Menetapkan rule deadline | Jika pengumpulan terlambat perlu aturan berbeda |
| Q-003 | Dosen | Nilai dan umpan balik perlu disimpan dalam format apa? | Menentukan model penilaian | Jika ada skala nilai atau template feedback tertentu |
| Q-004 | Mahasiswa | Informasi tugas apa yang harus terlihat sebelum mengumpulkan? | Menentukan tampilan tugas | Jika status tugas, deadline, dan detail lain harus muncul |
| Q-005 | Mahasiswa | Kapan pengumpulan dianggap berhasil atau gagal? | Menentukan acceptance criteria upload | Jika ada batas ukuran file atau format file |
| Q-006 | Administrator | Data pengguna dan mata kuliah apa yang harus dikelola? | Menentukan ruang lingkup administrasi | Jika ada operasi tambah, ubah, nonaktif, hapus |
| Q-007 | Administrator | Apakah konfigurasi sistem mencakup hak akses, akademik, atau parameter lain? | Menentukan scope konfigurasi | Jika ada pengaturan yang memengaruhi seluruh sistem |

## 5. Kebutuhan Eksplisit
| Need ID | Stakeholder / Sumber | Kebutuhan yang Dinyatakan | Evidence | Business Value |
|---|---|---|---|---|
| NEED-001 | CASE.md | Sistem dipakai untuk mengelola tugas perkuliahan | SRC-001 | Menyatukan proses akademik terkait tugas |
| NEED-002 | CASE.md | Dosen dapat membuat tugas | SRC-001 | Memudahkan distribusi tugas |
| NEED-003 | CASE.md | Dosen dapat menetapkan deadline | SRC-001 | Mendukung pengelolaan tenggat waktu |
| NEED-004 | CASE.md | Dosen dapat memberikan nilai dan umpan balik | SRC-001 | Mendukung proses evaluasi tugas |
| NEED-005 | CASE.md | Mahasiswa dapat melihat tugas | SRC-001 | Memudahkan akses informasi tugas |
| NEED-006 | CASE.md | Mahasiswa dapat mengumpulkan file | SRC-001 | Mendukung pengumpulan tugas terpusat |
| NEED-007 | CASE.md | Mahasiswa dapat memantau status dan deadline | SRC-001 | Meningkatkan visibilitas progres tugas |
| NEED-008 | CASE.md | Administrator dapat mengelola pengguna | SRC-001 | Mendukung kontrol akses dan manajemen akun |
| NEED-009 | CASE.md | Administrator dapat mengelola mata kuliah | SRC-001 | Mendukung struktur akademik |
| NEED-010 | CASE.md | Administrator dapat mengelola konfigurasi sistem | SRC-001 | Mendukung operasional sistem |
| NEED-011 | CASE.md | Sistem harus memperhatikan usability | SRC-001 | Menjaga kemudahan penggunaan |
| NEED-012 | CASE.md | Sistem harus memperhatikan security | SRC-001 | Melindungi data dan akses |
| NEED-013 | CASE.md | Sistem harus memperhatikan performance | SRC-001 | Menjaga respons sistem saat dipakai banyak pengguna |
| NEED-014 | CASE.md | Sistem harus memperhatikan reliability | SRC-001 | Menjaga konsistensi layanan |
| NEED-015 | CASE.md | Sistem harus memperhatikan data integrity | SRC-001 | Menjaga akurasi data tugas, nilai, dan pengumpulan |

## 6. Kebutuhan Implisit dan Asumsi
| Assumption ID | Kebutuhan yang Diinferensi | Dasar Inferensi | Validasi yang Dibutuhkan | Risiko jika Salah |
|---|---|---|---|---|
| ASM-001 | Setiap pengguna memiliki akun unik dan kredensial login | Asumsi A-01 di assumptions.md | Konfirmasi mekanisme akun | Akses pengguna tidak dapat dibedakan |
| ASM-002 | Sistem memakai autentikasi berbasis sesi atau token | Asumsi A-02 | Konfirmasi pola autentikasi | Implementasi security berubah |
| ASM-003 | Sistem menerapkan role-based access control | Asumsi A-03 dan stakeholder notes | Konfirmasi matriks hak akses | Pengguna bisa mengakses fitur yang tidak semestinya |
| ASM-004 | Tugas terkait dengan mata kuliah | Asumsi A-05 | Konfirmasi relasi data | Struktur data tugas salah |
| ASM-005 | Mahasiswa hanya dapat melihat dan mengumpulkan tugas pada mata kuliah yang diikuti | Asumsi A-06 | Konfirmasi aturan enrolment | Akses tugas menjadi terlalu luas |
| ASM-006 | Ada batas format dan ukuran file unggahan | Asumsi A-07 dan A-08 | Konfirmasi batas teknis upload | Upload tidak terkontrol |
| ASM-007 | Deadline mencakup tanggal dan waktu | Asumsi A-15 | Konfirmasi format deadline | Aturan keterlambatan ambigu |
| ASM-008 | Sistem mengirim pengingat deadline | Asumsi A-16 dan A-17 | Konfirmasi kebutuhan notifikasi | Mahasiswa kehilangan pengingat tugas |
| ASM-009 | Laporan mencakup rekap status pengumpulan | Asumsi A-18 | Konfirmasi bentuk laporan | Kebutuhan reporting tidak lengkap |
| ASM-010 | Sistem berbasis web dan multi-user | Asumsi A-21 dan A-24 | Konfirmasi platform dan beban akses | Desain platform dan performa salah |

## 7. Functional Requirements
| Requirement ID | Requirement | Source Need | Priority | Acceptance Criteria | Validation Status |
|---|---|---|---|---|---|
| FR-001 | Sistem harus memungkinkan dosen membuat tugas perkuliahan | NEED-002 | High | Dosen dapat menyimpan tugas baru dengan data valid | Menunggu Validasi |
| FR-002 | Sistem harus memungkinkan dosen menetapkan deadline tugas | NEED-003 | High | Deadline tersimpan untuk setiap tugas dan dapat dibaca mahasiswa | Menunggu Validasi |
| FR-003 | Sistem harus memungkinkan dosen memberikan nilai dan umpan balik | NEED-004 | High | Nilai dan umpan balik dapat disimpan pada tugas yang sudah dikumpulkan | Menunggu Validasi |
| FR-004 | Sistem harus memungkinkan mahasiswa melihat tugas | NEED-005 | High | Mahasiswa dapat melihat daftar tugas yang tersedia | Menunggu Validasi |
| FR-005 | Sistem harus memungkinkan mahasiswa mengumpulkan file tugas | NEED-006 | High | File yang valid dapat diunggah dan tercatat sebagai pengumpulan | Menunggu Validasi |
| FR-006 | Sistem harus memungkinkan mahasiswa memantau status pengumpulan dan deadline | NEED-007 | High | Status dan deadline tampil pada halaman tugas | Menunggu Validasi |
| FR-007 | Sistem harus memungkinkan administrator mengelola pengguna | NEED-008 | High | Administrator dapat menambah, mengubah, menonaktifkan, atau menghapus akun sesuai hak akses | Menunggu Validasi |
| FR-008 | Sistem harus memungkinkan administrator mengelola mata kuliah | NEED-009 | High | Administrator dapat menyimpan dan memperbarui data mata kuliah | Menunggu Validasi |
| FR-009 | Sistem harus memungkinkan administrator mengelola konfigurasi sistem | NEED-010 | Medium | Nilai konfigurasi dapat diperbarui oleh administrator yang berwenang | Menunggu Validasi |
| FR-010 | Sistem harus menyediakan pelaporan status pengumpulan tugas | NEED-015 | Medium | Laporan dapat menampilkan data tugas, pengumpulan, dan statusnya | Menunggu Validasi |

## 8. Non-Functional Requirements
| Requirement ID | Quality Attribute | Requirement | Measurement / Threshold | Source Need | Validation Status |
|---|---|---|---|---|---|
| NFR-001 | Usability | Antarmuka harus dapat digunakan oleh dosen, mahasiswa, dan administrator untuk menjalankan tugas utama tanpa bantuan teknis khusus | [BELUM DIDEFINISIKAN — diperlukan metrik usability] | NEED-011 | Asumsi |
| NFR-002 | Security | Sistem harus membatasi akses berdasarkan peran pengguna | Akses hanya sesuai otorisasi peran | NEED-012 | Asumsi |
| NFR-003 | Performance | Sistem harus tetap responsif saat diakses banyak pengguna secara bersamaan | [BELUM DIDEFINISIKAN — diperlukan threshold performa] | NEED-013 | Asumsi |
| NFR-004 | Reliability | Sistem harus berfungsi konsisten saat proses pengelolaan tugas, pengumpulan, penilaian, dan pelaporan | [BELUM DIDEFINISIKAN — diperlukan threshold reliability] | NEED-014 | Asumsi |
| NFR-005 | Data Integrity | Data tugas, pengumpulan, nilai, dan umpan balik harus tersimpan akurat | Tidak boleh ada kehilangan atau korupsi data pada alur utama | NEED-015 | Asumsi |

## 9. Temuan Elicitation
### Temuan Utama
- Sistem berfokus pada tiga peran utama: dosen, mahasiswa, dan administrator.
- Kebutuhan eksplisit sudah cukup jelas untuk alur tugas, pengumpulan, penilaian, dan administrasi dasar.
- Atribut kualitas sistem sudah disebutkan, tetapi belum memiliki metrik terukur.

### Konflik atau Kontradiksi
- Tidak ditemukan kontradiksi eksplisit pada sumber yang ditinjau.

### Gap dan Pertanyaan Terbuka
- Format deadline belum divalidasi secara eksplisit pada sumber utama.
- Format file unggahan dan batas ukuran file belum didefinisikan.
- Notifikasi deadline belum dipastikan sebagai requirement final.
- Metrik usability, performance, dan reliability belum tersedia.
- Detail pelaporan belum cukup spesifik untuk membuat threshold yang terukur.

### Risiko
- Jika asumsi autentikasi dan RBAC salah, desain akses sistem dapat berubah signifikan.
- Jika format upload tidak ditentukan, requirement pengumpulan file belum bisa diuji secara penuh.
- Jika kebutuhan laporan tidak diperjelas, scope reporting bisa melebar.

## 10. Traceability Matrix
| Need ID | Requirement ID | Source ID | Acceptance Criteria ID | Status |
|---|---|---|---|---|
| NEED-002 | FR-001 | SRC-001 | AC-001 | Menunggu Validasi |
| NEED-003 | FR-002 | SRC-001 | AC-002 | Menunggu Validasi |
| NEED-004 | FR-003 | SRC-001 | AC-003 | Menunggu Validasi |
| NEED-005 | FR-004 | SRC-001 | AC-004 | Menunggu Validasi |
| NEED-006 | FR-005 | SRC-001 | AC-005 | Menunggu Validasi |
| NEED-007 | FR-006 | SRC-001 | AC-006 | Menunggu Validasi |
| NEED-008 | FR-007 | SRC-001 | AC-007 | Menunggu Validasi |
| NEED-009 | FR-008 | SRC-001 | AC-008 | Menunggu Validasi |
| NEED-010 | FR-009 | SRC-001 | AC-009 | Menunggu Validasi |
| NEED-015 | FR-010 | SRC-001 | AC-010 | Menunggu Validasi |

## 11. Hasil Quality Check
| Check | Hasil | Catatan |
|---|---|---|
| Kelengkapan | Lulus | Semua bagian utama format terisi |
| Konsistensi | Lulus | Requirement selaras dengan stakeholder notes dan case |
| Tidak Ambigu | Sebagian lulus | Beberapa NFR masih memakai placeholder karena threshold belum tersedia |
| Dapat Diuji | Sebagian lulus | FR dapat diuji, beberapa NFR masih butuh metrik |
| Traceable | Lulus | Setiap requirement memiliki source need dan source ID |
| Bernilai Bisnis | Lulus | Semua requirement terkait tujuan sistem kampus |
| Tervalidasi | Sebagian lulus | Beberapa item masih berstatus asumsi atau menunggu validasi stakeholder |
