# Software Requirements Specification: Student Task Management System

## 1. Ringkasan
- Nama proyek/fitur: Student Task Management System
- Tujuan bisnis: Mendukung pengelolaan tugas perkuliahan, pengumpulan tugas, penilaian, tenggat waktu, dan pelaporan di lingkungan kampus.
- Stakeholder: Dosen, mahasiswa, administrator.
- Pengguna utama: Dosen, mahasiswa, administrator.
- Ruang lingkup: Pengelolaan tugas, deadline, pengumpulan file, penilaian, umpan balik, manajemen pengguna, manajemen mata kuliah, konfigurasi sistem, dan pelaporan.
- Di luar ruang lingkup: Integrasi eksternal dan fitur lain yang tidak disebutkan dalam kasus.

## 2. Konteks dan Asumsi
### 2.1 Konteks yang Ditinjau
| Source ID | Jenis Sumber | Ringkasan | Relevansi |
|---|---|---|---|
| SRC-001 | inception-document.md | Menjelaskan masalah bisnis, tujuan proyek, stakeholder, scope, asumsi, constraint, dan open questions | Sumber utama untuk business goal, stakeholder, scope, dan constraint |
| SRC-002 | elicitation.md | Menyajikan kebutuhan eksplisit, implisit, pertanyaan wawancara, FR, NFR, dan traceability | Sumber utama untuk requirement formal |
| SRC-003 | CASE.md | Menjelaskan sistem kampus, stakeholder, dan atribut kualitas yang harus diperhatikan | Menjadi sumber tujuan bisnis dan quality attribute |
| SRC-004 | assumptions.md | Daftar asumsi awal tentang login, RBAC, tugas, upload, penilaian, notifikasi, reporting, dan infrastruktur | Sumber asumsi eksplisit yang perlu ditandai |
| SRC-005 | stakeholder-notes.md | Catatan kebutuhan per stakeholder dan atribut kualitas sistem | Sumber kebutuhan stakeholder dan kualitas sistem |

### 2.2 Asumsi
| Assumption ID | Asumsi | Alasan | Validasi yang Dibutuhkan | Risiko Jika Salah |
|---|---|---|---|---|
| ASM-001 | `[ASUMSI]` Setiap pengguna memiliki akun unik dengan kredensial login | Untuk mendefinisikan identitas pengguna | Konfirmasi mekanisme akun | Pengguna tidak dapat dibedakan dengan benar |
| ASM-002 | `[ASUMSI]` Sistem memakai autentikasi berbasis sesi atau token | Untuk mendefinisikan alur login | Konfirmasi pola autentikasi | Desain security berubah |
| ASM-003 | `[ASUMSI]` Sistem menerapkan role-based access control | Untuk membatasi fitur sesuai peran | Konfirmasi matriks hak akses | Akses fitur menjadi terlalu luas |
| ASM-004 | `[ASUMSI]` Tugas terhubung dengan mata kuliah tertentu | Untuk menyusun model data tugas | Konfirmasi relasi tugas-mata kuliah | Struktur data salah |
| ASM-005 | `[ASUMSI]` Mahasiswa hanya dapat melihat dan mengumpulkan tugas pada mata kuliah yang diikuti | Untuk mengatur akses tugas | Konfirmasi aturan enrolment | Akses tugas menjadi tidak tepat |
| ASM-006 | `[ASUMSI]` Ada batas format dan ukuran file unggahan | Untuk mengatur validasi upload | Konfirmasi format dan ukuran file | Upload tidak terkontrol |
| ASM-007 | `[ASUMSI]` Deadline mencakup tanggal dan waktu | Untuk mengatur ketepatan waktu pengumpulan | Konfirmasi format deadline | Aturan keterlambatan ambigu |
| ASM-008 | `[ASUMSI]` Sistem mengirim pengingat deadline | Untuk mendukung notifikasi pengguna | Konfirmasi kebutuhan notifikasi | Mahasiswa kehilangan pengingat |
| ASM-009 | `[ASUMSI]` Laporan mencakup rekap status pengumpulan | Untuk mendefinisikan ruang lingkup reporting | Konfirmasi format laporan | Reporting tidak lengkap |
| ASM-010 | `[ASUMSI]` Sistem berbasis web dan multi-user | Untuk mendefinisikan konteks akses dan performa | Konfirmasi platform dan beban akses | Desain platform dan performa salah |

## 3. Business Goals
| Goal ID | Business Goal | Metrik Keberhasilan | Prioritas |
|---|---|---|---|
| BG-001 | Memusatkan pengelolaan tugas perkuliahan | Seluruh proses pembuatan, pengumpulan, dan penilaian tugas dilakukan melalui sistem | Tinggi |
| BG-002 | Meningkatkan visibilitas status tugas bagi mahasiswa dan dosen | Persentase tugas yang memiliki status dan deadline yang dapat dilihat di sistem | Tinggi |
| BG-003 | Mendukung pelaporan akademik yang lebih mudah | Laporan pengumpulan tugas dapat dihasilkan dari sistem | Sedang |

## 4. User Stories
| User Story ID | User Story | Business Goal | Prioritas | Status Validasi |
|---|---|---|---|---|
| US-001 | Sebagai dosen, saya ingin membuat tugas perkuliahan, sehingga saya dapat mendistribusikan tugas ke mahasiswa | BG-001 | Tinggi | Pending Validation |
| US-002 | Sebagai dosen, saya ingin menetapkan deadline tugas, sehingga mahasiswa mengetahui batas waktu pengumpulan | BG-001, BG-002 | Tinggi | Pending Validation |
| US-003 | Sebagai dosen, saya ingin memberikan nilai dan umpan balik, sehingga hasil evaluasi tugas tercatat di sistem | BG-001 | Tinggi | Pending Validation |
| US-004 | Sebagai mahasiswa, saya ingin melihat tugas, sehingga saya mengetahui tugas yang harus dikerjakan | BG-001, BG-002 | Tinggi | Pending Validation |
| US-005 | Sebagai mahasiswa, saya ingin mengumpulkan file tugas, sehingga pengumpulan saya tercatat di sistem | BG-001 | Tinggi | Pending Validation |
| US-006 | Sebagai mahasiswa, saya ingin memantau status pengumpulan dan deadline, sehingga saya dapat mengelola tugas tepat waktu | BG-002 | Tinggi | Pending Validation |
| US-007 | Sebagai administrator, saya ingin mengelola pengguna, sehingga akses sistem tetap terkontrol | BG-001 | Tinggi | Pending Validation |
| US-008 | Sebagai administrator, saya ingin mengelola mata kuliah, sehingga struktur akademik tetap konsisten di sistem | BG-001 | Tinggi | Pending Validation |
| US-009 | Sebagai administrator, saya ingin mengonfigurasi sistem, sehingga sistem sesuai dengan kebutuhan operasional kampus | BG-001 | Sedang | Pending Validation |
| US-010 | Sebagai dosen dan administrator, saya ingin melihat laporan status pengumpulan tugas, sehingga saya dapat memantau progres akademik | BG-003 | Sedang | Pending Validation |

## 5. Functional Requirements
| Requirement ID | Functional Requirement | User Story / Source | Prioritas | Acceptance Criteria | Status Validasi |
|---|---|---|---|---|---|
| FR-001 | Sistem harus memungkinkan dosen membuat tugas perkuliahan | US-001 / SRC-003 | Tinggi | AC-001 | Pending Validation |
| FR-002 | Sistem harus memungkinkan dosen menetapkan deadline tugas | US-002 / SRC-003 | Tinggi | AC-002 | Pending Validation |
| FR-003 | Sistem harus memungkinkan dosen memberikan nilai dan umpan balik | US-003 / SRC-003 | Tinggi | AC-003 | Pending Validation |
| FR-004 | Sistem harus memungkinkan mahasiswa melihat tugas | US-004 / SRC-003 | Tinggi | AC-004 | Pending Validation |
| FR-005 | Sistem harus memungkinkan mahasiswa mengumpulkan file tugas | US-005 / SRC-003 | Tinggi | AC-005 | Pending Validation |
| FR-006 | Sistem harus memungkinkan mahasiswa memantau status pengumpulan dan deadline | US-006 / SRC-003 | Tinggi | AC-006 | Pending Validation |
| FR-007 | Sistem harus memungkinkan administrator mengelola pengguna | US-007 / SRC-003 | Tinggi | AC-007 | Pending Validation |
| FR-008 | Sistem harus memungkinkan administrator mengelola mata kuliah | US-008 / SRC-003 | Tinggi | AC-008 | Pending Validation |
| FR-009 | Sistem harus memungkinkan administrator mengonfigurasi sistem | US-009 / SRC-003 | Sedang | AC-009 | Pending Validation |
| FR-010 | Sistem harus menyediakan pelaporan status pengumpulan tugas | US-010 / SRC-003 | Sedang | AC-010 | Pending Validation |

## 6. Non-Functional Requirements
| Requirement ID | Atribut Kualitas | Non-Functional Requirement | Ukuran / Threshold | Source | Status Validasi |
|---|---|---|---|---|---|
| NFR-001 | Usability | Antarmuka harus dapat digunakan oleh dosen, mahasiswa, dan administrator untuk menjalankan tugas utama tanpa bantuan teknis khusus | [BELUM DIDEFINISIKAN — diperlukan metrik usability] | SRC-003, SRC-005 | Assumption |
| NFR-002 | Security | Sistem harus membatasi akses berdasarkan peran pengguna | Akses hanya sesuai otorisasi peran | SRC-003, SRC-005 | Assumption |
| NFR-003 | Performance | Sistem harus tetap responsif saat diakses banyak pengguna secara bersamaan | [BELUM DIDEFINISIKAN — diperlukan threshold performa] | SRC-003, SRC-005 | Assumption |
| NFR-004 | Reliability | Sistem harus berfungsi konsisten saat proses pengelolaan tugas, pengumpulan, penilaian, dan pelaporan | [BELUM DIDEFINISIKAN — diperlukan threshold reliability] | SRC-003, SRC-005 | Assumption |
| NFR-005 | Data Integrity | Data tugas, pengumpulan, nilai, dan umpan balik harus tersimpan akurat | Tidak boleh ada kehilangan atau korupsi data pada alur utama | SRC-003, SRC-005 | Assumption |

## 7. Business Rules
| Rule ID | Business Rule | Kondisi | Pengecualian | Requirement Terkait | Status Validasi |
|---|---|---|---|---|---|
| BR-001 | Tugas terhubung dengan mata kuliah tertentu | Saat dosen membuat tugas | Jika struktur akademik berubah | FR-001, FR-008 | Assumption |
| BR-002 | Mahasiswa hanya dapat melihat dan mengumpulkan tugas pada mata kuliah yang diikuti | Saat mahasiswa membuka atau mengumpulkan tugas | Jika admin memberi akses khusus | FR-004, FR-005 | Assumption |
| BR-003 | Upload file dibatasi format dan ukuran tertentu | Saat mahasiswa mengunggah file | Jika kebijakan upload belum ditetapkan | FR-005 | Assumption |
| BR-004 | Deadline mencakup tanggal dan waktu | Saat dosen menetapkan deadline | Jika kebijakan kampus hanya memakai tanggal | FR-002, FR-006 | Assumption |
| BR-005 | Nilai dan umpan balik dipublikasikan setelah dosen menyelesaikan penilaian | Saat dosen menyimpan hasil penilaian | Jika kampus menerapkan mode draft | FR-003 | Assumption |
| BR-006 | Administrator memiliki hak untuk mengelola pengguna dan mata kuliah | Saat operasi administrasi dilakukan | Jika hak akses admin dibatasi lebih lanjut | FR-007, FR-008, FR-009 | Assumption |

## 8. Acceptance Criteria
| Acceptance Criteria ID | Requirement / User Story | Given | When | Then | Tipe Skenario |
|---|---|---|---|---|---|
| AC-001 | FR-001 / US-001 | Dosen telah login dan memiliki akses membuat tugas | Dosen menyimpan data tugas yang valid | Sistem menyimpan tugas baru dan menampilkannya pada daftar tugas | Berhasil |
| AC-002 | FR-002 / US-002 | Dosen telah login dan sedang membuat atau mengubah tugas | Dosen menetapkan deadline | Sistem menyimpan deadline untuk tugas tersebut | Berhasil |
| AC-003 | FR-003 / US-003 | Dosen telah login dan membuka tugas yang sudah dikumpulkan | Dosen menyimpan nilai dan umpan balik | Sistem menyimpan hasil penilaian dan umpan balik | Berhasil |
| AC-004 | FR-004 / US-004 | Mahasiswa telah login | Mahasiswa membuka daftar tugas | Sistem menampilkan tugas yang tersedia untuk mahasiswa tersebut | Berhasil |
| AC-005 | FR-005 / US-005 | Mahasiswa telah login dan tugas masih dapat dikumpulkan | Mahasiswa mengunggah file yang valid | Sistem menyimpan pengumpulan dan mencatat timestamp | Berhasil |
| AC-006 | FR-006 / US-006 | Mahasiswa telah login | Mahasiswa membuka detail tugas | Sistem menampilkan status pengumpulan dan deadline | Berhasil |
| AC-007 | FR-007 / US-007 | Administrator telah login | Administrator melakukan pengelolaan akun pengguna | Sistem menyimpan perubahan data pengguna sesuai hak akses | Berhasil |
| AC-008 | FR-008 / US-008 | Administrator telah login | Administrator mengelola data mata kuliah | Sistem menyimpan perubahan data mata kuliah | Berhasil |
| AC-009 | FR-009 / US-009 | Administrator telah login | Administrator mengubah konfigurasi sistem | Sistem menyimpan konfigurasi baru | Berhasil |
| AC-010 | FR-010 / US-010 | Dosen atau administrator memiliki akses laporan | Pengguna membuka laporan status pengumpulan | Sistem menampilkan data pengumpulan sesuai hak akses | Berhasil |

## 9. Traceability Matrix
| Business Goal | User Story ID | Requirement ID | Business Rule ID | Acceptance Criteria ID | Status |
|---|---|---|---|---|---|
| BG-001 | US-001 | FR-001 | BR-001 | AC-001 | Pending Validation |
| BG-001 | US-002 | FR-002 | BR-004 | AC-002 | Pending Validation |
| BG-001 | US-003 | FR-003 | BR-005 | AC-003 | Pending Validation |
| BG-001 | US-007 | FR-007 | BR-006 | AC-007 | Pending Validation |
| BG-001 | US-008 | FR-008 | BR-001, BR-006 | AC-008 | Pending Validation |
| BG-001 | US-009 | FR-009 | BR-006 | AC-009 | Pending Validation |
| BG-002 | US-004 | FR-004 | BR-002 | AC-004 | Pending Validation |
| BG-002 | US-005 | FR-005 | BR-002, BR-003 | AC-005 | Pending Validation |
| BG-002 | US-006 | FR-006 | BR-004 | AC-006 | Pending Validation |
| BG-003 | US-010 | FR-010 | [BELUM DIDEFINISIKAN] | AC-010 | Pending Validation |

## 10. Gap, Konflik, dan Pertanyaan Terbuka
### Gap
- Format deadline belum divalidasi secara eksplisit.
- Format dan batas ukuran file unggahan belum didefinisikan.
- Metrik usability, performance, dan reliability belum tersedia.
- Detail format laporan belum cukup spesifik.

### Konflik
- Tidak ditemukan konflik eksplisit pada sumber yang ditinjau.

### Pertanyaan Terbuka
- Apakah deadline harus mencakup tanggal dan waktu, atau cukup tanggal?
- Format file unggahan apa yang didukung dan berapa batas ukurannya?
- Notifikasi deadline apakah wajib, dan kanal apa yang digunakan?
- Format laporan apa yang dibutuhkan oleh dosen dan administrator?
- Apakah ada target terukur untuk usability, performance, dan reliability?

## 11. Quality Check Result
| Check | Result | Catatan |
|---|---|---|
| Kelengkapan | Lulus | Struktur utama SRS terisi |
| Konsistensi | Lulus | Requirement selaras dengan inception dan elicitation |
| Tidak Ambigu | Sebagian lulus | Beberapa NFR masih memerlukan threshold final |
| Dapat Diuji | Sebagian lulus | FR dan AC dapat diuji; beberapa NFR belum punya ukuran final |
| Traceability | Lulus | Business goal, user story, requirement, rule, dan AC saling terhubung |
| Business Value | Lulus | Semua item mendukung tujuan sistem kampus |
| Feasible | Lulus | Tidak ada requirement yang jelas bertentangan dengan konteks |
| Terprioritaskan | Lulus | Prioritas diberikan pada FR dan US |
| Tervalidasi | Sebagian lulus | Beberapa item masih berstatus assumption atau pending validation |
