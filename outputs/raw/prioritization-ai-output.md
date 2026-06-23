# Prioritization Report: Student Task Management System

## 1. Tujuan Prioritisasi
- Tujuan prioritisasi: Menentukan urutan kebutuhan yang paling layak untuk implementasi awal berdasarkan nilai bisnis, dependency, risiko, dan constraint yang tersedia.
- Business goal: Memusatkan pengelolaan tugas perkuliahan, meningkatkan visibilitas status tugas, dan mendukung pelaporan akademik.
- Target rilis / periode keputusan: Rilis awal / MVP
- Stakeholder utama: Dosen, mahasiswa, administrator
- Constraint utama: Atribut kualitas sistem harus diperhatikan, tetapi metrik performa, usability, reliability, dan detail laporan belum didefinisikan secara kuantitatif.
- Kriteria keputusan: Business critical, dependency critical, user impact, operasional minimum, dan konsistensi dengan scope yang telah ditetapkan.

## 2. Konteks yang Ditinjau
| Source ID | Jenis Sumber | Ringkasan | Relevansi |
|---|---|---|---|
| SRC-001 | specification.md | SRS berisi business goal, user story, FR, NFR, business rule, AC, dan traceability | Sumber utama untuk item yang diprioritaskan |
| SRC-002 | elicitation.md | Memuat kebutuhan eksplisit, implisit, pertanyaan, dan temuan elicitation | Sumber untuk value, asumsi, dan gap |
| SRC-003 | inception-document.md | Menjelaskan masalah bisnis, scope, stakeholder, asumsi, constraint, dan open questions | Sumber untuk business goal dan constraint utama |
| SRC-004 | CASE.md | Menjelaskan konteks sistem kampus dan atribut kualitas sistem | Sumber legitimasi kebutuhan bisnis dan kualitas |
| SRC-005 | stakeholder-notes.md | Menjelaskan kebutuhan per stakeholder dan atribut kualitas | Sumber kebutuhan pengguna dan dampak stakeholder |

## 3. Item yang Diprioritaskan
| Item ID | Item | Jenis | Source | Business Value | Effort / Complexity | Status Validasi |
|---|---|---|---|---|---|---|
| US-001 | Sebagai dosen, saya ingin membuat tugas perkuliahan, sehingga saya dapat mendistribusikan tugas ke mahasiswa | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-002 | Sebagai dosen, saya ingin menetapkan deadline tugas, sehingga mahasiswa mengetahui batas waktu pengumpulan | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-003 | Sebagai dosen, saya ingin memberikan nilai dan umpan balik, sehingga hasil evaluasi tugas tercatat di sistem | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-004 | Sebagai mahasiswa, saya ingin melihat tugas, sehingga saya mengetahui tugas yang harus dikerjakan | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-005 | Sebagai mahasiswa, saya ingin mengumpulkan file tugas, sehingga pengumpulan saya tercatat di sistem | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-006 | Sebagai mahasiswa, saya ingin memantau status pengumpulan dan deadline, sehingga saya dapat mengelola tugas tepat waktu | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-007 | Sebagai administrator, saya ingin mengelola pengguna, sehingga akses sistem tetap terkontrol | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-008 | Sebagai administrator, saya ingin mengelola mata kuliah, sehingga struktur akademik tetap konsisten di sistem | User Story | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Pending Validation |
| US-009 | Sebagai administrator, saya ingin mengonfigurasi sistem, sehingga sistem sesuai dengan kebutuhan operasional kampus | User Story | SRC-001, SRC-002, SRC-003 | Sedang | Belum didefinisikan | Pending Validation |
| US-010 | Sebagai dosen dan administrator, saya ingin melihat laporan status pengumpulan tugas, sehingga saya dapat memantau progres akademik | User Story | SRC-001, SRC-002, SRC-003 | Sedang | Belum didefinisikan | Pending Validation |
| FR-001 | Sistem harus memungkinkan dosen membuat tugas perkuliahan | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-002 | Sistem harus memungkinkan dosen menetapkan deadline tugas | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-003 | Sistem harus memungkinkan dosen memberikan nilai dan umpan balik | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-004 | Sistem harus memungkinkan mahasiswa melihat tugas | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-005 | Sistem harus memungkinkan mahasiswa mengumpulkan file tugas | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang-Tinggi | Pending Validation |
| FR-006 | Sistem harus memungkinkan mahasiswa memantau status pengumpulan dan deadline | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-007 | Sistem harus memungkinkan administrator mengelola pengguna | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-008 | Sistem harus memungkinkan administrator mengelola mata kuliah | Requirement | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Pending Validation |
| FR-009 | Sistem harus memungkinkan administrator mengonfigurasi sistem | Requirement | SRC-001, SRC-002, SRC-003 | Sedang | Sedang | Pending Validation |
| FR-010 | Sistem harus menyediakan pelaporan status pengumpulan tugas | Requirement | SRC-001, SRC-002, SRC-003 | Sedang | Sedang | Pending Validation |
| NFR-002 | Sistem harus membatasi akses berdasarkan peran pengguna | NFR | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Assumption |
| NFR-005 | Data tugas, pengumpulan, nilai, dan umpan balik harus tersimpan akurat | NFR | SRC-001, SRC-002, SRC-003 | Tinggi | Sedang | Assumption |
| NFR-003 | Sistem harus tetap responsif saat diakses banyak pengguna secara bersamaan | NFR | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Assumption |
| NFR-004 | Sistem harus berfungsi konsisten saat proses pengelolaan tugas, pengumpulan, penilaian, dan pelaporan | NFR | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Assumption |
| NFR-001 | Antarmuka harus dapat digunakan oleh dosen, mahasiswa, dan administrator untuk menjalankan tugas utama tanpa bantuan teknis khusus | NFR | SRC-001, SRC-002, SRC-003 | Tinggi | Belum didefinisikan | Assumption |

## 4. Konflik Stakeholder
| Conflict ID | Stakeholder Terkait | Konflik | Dampak | Keputusan / Status | Klarifikasi Dibutuhkan |
|---|---|---|---|---|---|
| CON-001 | Dosen, mahasiswa, administrator | Tidak ada konflik eksplisit dalam sumber, tetapi prioritas detail laporan, notifikasi, dan validasi NFR belum disepakati | Berpotensi mengubah scope rilis awal | Status: belum ada konflik formal | Ya, untuk detail laporan dan metrik NFR |

## 5. Dependency Analysis
| Dependency ID | Item Terkait | Dependency | Jenis Dependency | Dampak Jika Tidak Terpenuhi | Status |
|---|---|---|---|---|---|
| DEP-001 | FR-005 | Tugas harus terhubung dengan mata kuliah dan akses mahasiswa dibatasi sesuai enrolment | Data / access dependency | Mahasiswa bisa mengumpulkan tugas yang tidak semestinya atau struktur data menjadi salah | Blocked until rules validated |
| DEP-002 | FR-002, FR-006 | Deadline harus memiliki definisi yang jelas mengenai tanggal/waktu | Rule dependency | Status deadline dan keterlambatan menjadi ambigu | Pending clarification |
| DEP-003 | FR-003 | Alur pengumpulan harus tersedia sebelum penilaian dan umpan balik | Functional predecessor | Penilaian tidak bisa dilakukan pada tugas yang belum dikumpulkan | Satisfied by FR-005 |
| DEP-004 | FR-007 | Model role-based access control harus disepakati | Security dependency | Pengelolaan pengguna bisa membuka akses yang tidak tepat | Pending validation |
| DEP-005 | FR-010 | Definisi format laporan dan pemilik akses laporan | Business rule / reporting dependency | Laporan mungkin tidak sesuai kebutuhan stakeholder | Pending clarification |
| DEP-006 | NFR-002 | Role-based access control | Security dependency | Security requirement tidak dapat diimplementasikan dengan benar | Pending validation |
| DEP-007 | NFR-003, NFR-004, NFR-001 | Metrik kualitas belum didefinisikan | Measurement dependency | NFR tidak dapat diuji secara final | Pending clarification |

## 6. MoSCoW Prioritization
| Item ID | Item | MoSCoW | Alasan Kategori | Dependency | Risiko | Status Validasi |
|---|---|---|---|---|---|---|
| US-001 | Sebagai dosen, saya ingin membuat tugas perkuliahan, sehingga saya dapat mendistribusikan tugas ke mahasiswa | Must Have | Business-critical untuk memulai alur utama sistem | DEP-001 | Jika tidak ada, sistem tidak memenuhi tujuan utama | Pending Validation |
| US-002 | Sebagai dosen, saya ingin menetapkan deadline tugas, sehingga mahasiswa mengetahui batas waktu pengumpulan | Must Have | Business-critical dan dependency-critical untuk pengumpulan tugas | DEP-002 | Tanpa deadline, kepatuhan waktu tidak terukur | Pending Validation |
| US-003 | Sebagai dosen, saya ingin memberikan nilai dan umpan balik, sehingga hasil evaluasi tugas tercatat di sistem | Must Have | Business-critical untuk proses akademik inti | DEP-003 | Penilaian tidak dapat selesai di sistem | Pending Validation |
| US-004 | Sebagai mahasiswa, saya ingin melihat tugas, sehingga saya mengetahui tugas yang harus dikerjakan | Must Have | Business-critical untuk penggunaan utama mahasiswa | DEP-001 | Mahasiswa tidak dapat memulai pengerjaan tugas | Pending Validation |
| US-005 | Sebagai mahasiswa, saya ingin mengumpulkan file tugas, sehingga pengumpulan saya tercatat di sistem | Must Have | Business-critical untuk tujuan sistem | DEP-001, DEP-002 | Alur inti tidak berjalan | Pending Validation |
| US-006 | Sebagai mahasiswa, saya ingin memantau status pengumpulan dan deadline, sehingga saya dapat mengelola tugas tepat waktu | Must Have | Business-critical untuk visibilitas dan kontrol tenggat | DEP-002 | Risiko keterlambatan meningkat | Pending Validation |
| US-007 | Sebagai administrator, saya ingin mengelola pengguna, sehingga akses sistem tetap terkontrol | Must Have | Security-critical dan operational-critical | DEP-004 | Akses pengguna menjadi tidak terkontrol | Pending Validation |
| US-008 | Sebagai administrator, saya ingin mengelola mata kuliah, sehingga struktur akademik tetap konsisten di sistem | Must Have | Dependency-critical untuk relasi tugas dan enrolment | DEP-001 | Struktur akademik tidak konsisten | Pending Validation |
| US-009 | Sebagai administrator, saya ingin mengonfigurasi sistem, sehingga sistem sesuai dengan kebutuhan operasional kampus | Should Have | Bernilai tinggi tetapi tidak menghalangi alur inti MVP | DEP-004 | Konfigurasi operasional tertunda | Pending Validation |
| US-010 | Sebagai dosen dan administrator, saya ingin melihat laporan status pengumpulan tugas, sehingga saya dapat memantau progres akademik | Should Have | Bernilai tinggi untuk monitoring, namun rilis awal masih bisa berjalan tanpa ini | DEP-005 | Transparansi progres berkurang | Pending Validation |
| FR-001 | Sistem harus memungkinkan dosen membuat tugas perkuliahan | Must Have | Mendukung business-critical workflow utama | DEP-001 | Alur inti tidak tersedia | Pending Validation |
| FR-002 | Sistem harus memungkinkan dosen menetapkan deadline tugas | Must Have | Wajib untuk operasi minimum pengumpulan tugas | DEP-002 | Deadline dan kepatuhan waktu tidak jelas | Pending Validation |
| FR-003 | Sistem harus memungkinkan dosen memberikan nilai dan umpan balik | Must Have | Wajib untuk proses akademik inti | DEP-003 | Penilaian tidak selesai | Pending Validation |
| FR-004 | Sistem harus memungkinkan mahasiswa melihat tugas | Must Have | Wajib untuk nilai pengguna utama | DEP-001 | Sistem tidak berguna bagi mahasiswa | Pending Validation |
| FR-005 | Sistem harus memungkinkan mahasiswa mengumpulkan file tugas | Must Have | Wajib untuk target utama sistem | DEP-001, DEP-002 | Proses pengumpulan gagal | Pending Validation |
| FR-006 | Sistem harus memungkinkan mahasiswa memantau status pengumpulan dan deadline | Must Have | Wajib untuk penggunaan operasional minimum | DEP-002 | Risiko keterlambatan dan salah status | Pending Validation |
| FR-007 | Sistem harus memungkinkan administrator mengelola pengguna | Must Have | Security-critical | DEP-004 | Otorisasi tidak terkontrol | Pending Validation |
| FR-008 | Sistem harus memungkinkan administrator mengelola mata kuliah | Must Have | Dependency-critical untuk relasi akademik | DEP-001 | Struktur akademik tidak konsisten | Pending Validation |
| FR-009 | Sistem harus memungkinkan administrator mengonfigurasi sistem | Should Have | Tidak menghalangi tujuan utama bila ditunda | DEP-004 | Operasional awal kurang fleksibel | Pending Validation |
| FR-010 | Sistem harus menyediakan pelaporan status pengumpulan tugas | Should Have | Memberi nilai tambahan untuk monitoring, namun bukan alur minimum | DEP-005 | Visibilitas laporan tertunda | Pending Validation |
| NFR-002 | Sistem harus membatasi akses berdasarkan peran pengguna | Must Have | Security-critical untuk semua peran | DEP-004, DEP-006 | Pelanggaran akses | Assumption |
| NFR-005 | Data tugas, pengumpulan, nilai, dan umpan balik harus tersimpan akurat | Must Have | Operational-critical dan data-critical | Tidak ada jika desain data benar | Risiko kehilangan data | Assumption |
| NFR-003 | Sistem harus tetap responsif saat diakses banyak pengguna secara bersamaan | Should Have | Penting untuk beban kampus, tetapi threshold belum ditetapkan | DEP-007 | Performa tidak terukur | Assumption |
| NFR-004 | Sistem harus berfungsi konsisten saat proses pengelolaan tugas, pengumpulan, penilaian, dan pelaporan | Should Have | Penting untuk reliabilitas, namun metrik belum ada | DEP-007 | Uji reliabilitas belum final | Assumption |
| NFR-001 | Antarmuka harus dapat digunakan oleh dosen, mahasiswa, dan administrator untuk menjalankan tugas utama tanpa bantuan teknis khusus | Should Have | Bernilai tinggi untuk adopsi, tetapi metrik usability belum tersedia | DEP-007 | Usability belum dapat diverifikasi final | Assumption |

## 7. Trade-Off Analysis
| Trade-Off ID | Keputusan | Opsi yang Dibandingkan | Yang Diperoleh | Yang Dikorbankan | Risiko | Alasan Keputusan |
|---|---|---|---|---|---|---|
| TRD-001 | Menempatkan alur inti tugas sebagai Must Have | Fokus pada tugas, deadline, pengumpulan, penilaian vs menambah laporan lanjutan dan konfigurasi detail sejak awal | MVP dapat mencapai tujuan bisnis utama | Fitur reporting lanjutan dan konfigurasi penuh ditunda | Stakeholder yang butuh pelaporan lengkap harus menunggu | Tujuan bisnis inti lebih kritis daripada fitur pendukung |
| TRD-002 | Menempatkan RBAC dan manajemen pengguna sebagai Must Have | Prioritaskan keamanan akses vs memperluas fitur non-kritis | Kontrol akses dan keamanan dasar terjaga | Waktu implementasi awal bertambah | Jika diabaikan, risiko akses salah sangat tinggi | Security-critical dan operational-critical |
| TRD-003 | Menunda metrik NFR yang belum jelas ke fase validasi | Pakai placeholder threshold vs memaksakan angka yang tidak ada bukti | Dokumen tetap jujur terhadap data yang tersedia | NFR belum final secara kuantitatif | NFR tidak bisa dianggap final | Tidak boleh mengarang ukuran tanpa bukti |

## 8. Decision Rationale
| Decision ID | Item / Konflik / Trade-Off | Keputusan | Alasan | Evidence / Source | Assumption | Owner Validasi |
|---|---|---|---|---|---|---|
| DEC-001 | US-001, FR-001 | Must Have | Merupakan pemicu utama alur pengelolaan tugas | SRC-001, SRC-002, SRC-003 | Tidak ada | Product / requirements owner |
| DEC-002 | US-002, FR-002 | Must Have | Tanpa deadline, pengumpulan tugas tidak dapat dikendalikan | SRC-001, SRC-002, SRC-003 | Deadline mencakup tanggal/waktu | Product / requirements owner |
| DEC-003 | US-005, FR-005 | Must Have | Pengumpulan file adalah inti sistem bagi mahasiswa | SRC-001, SRC-002, SRC-003 | Format upload belum final | Product / requirements owner |
| DEC-004 | US-007, FR-007, NFR-002 | Must Have | Pengelolaan akses pengguna dan RBAC bersifat security-critical | SRC-001, SRC-002, SRC-003, SRC-005 | RBAC benar-benar dibutuhkan | Security / product owner |
| DEC-005 | US-010, FR-010 | Should Have | Berguna untuk monitoring, tetapi bukan syarat minimum alur inti | SRC-001, SRC-002, SRC-003 | Format laporan belum final | Product owner |
| DEC-006 | TRD-001 | Pilih alur inti dulu | Fokus ke nilai bisnis utama | SRC-001, SRC-003, SRC-005 | Laporan lanjutan bisa ditunda | Product owner |
| DEC-007 | TRD-003 | Tunda angka NFR final | Tidak ada threshold kuantitatif di sumber | SRC-001, SRC-002, SRC-003 | Threshold perlu validasi | QA / stakeholder |

## 9. Rekomendasi Prioritas
### Must Have
- US-001 / FR-001
- US-002 / FR-002
- US-003 / FR-003
- US-004 / FR-004
- US-005 / FR-005
- US-006 / FR-006
- US-007 / FR-007
- US-008 / FR-008
- NFR-002
- NFR-005

### Should Have
- US-009 / FR-009
- US-010 / FR-010
- NFR-003
- NFR-004
- NFR-001

### Could Have
- Tidak ada item yang cukup bukti untuk dimasukkan ke kategori ini pada keputusan ini.

### Won't Have
- Fitur di luar scope pengelolaan tugas, pengumpulan, penilaian, deadline, administrasi dasar, dan pelaporan.

## 10. Gap dan Pertanyaan Terbuka
### Gap
- Effort atau complexity belum tersedia secara kuantitatif.
- Target release date belum tersedia.
- Metrik NFR untuk usability, performance, dan reliability belum didefinisikan.
- Format laporan dan notifikasi belum dipastikan.

### Pertanyaan Terbuka
- Apakah deadline tugas harus mencakup tanggal dan waktu secara wajib?
- Format file unggahan dan batas ukuran file apa yang akan digunakan?
- Apakah notifikasi merupakan syarat rilis awal atau bisa ditunda?
- Format laporan apa yang wajib tersedia pada rilis awal?
- Apakah ada threshold performa, usability, dan reliability yang harus dipatuhi?

## 11. Traceability Matrix
| Business Goal | Item ID | MoSCoW | Dependency ID | Conflict ID | Trade-Off ID | Decision ID |
|---|---|---|---|---|---|---|
| BG-001 | US-001 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | US-002 | Must Have | DEP-002 | CON-001 | TRD-001 | DEC-002 |
| BG-001 | US-003 | Must Have | DEP-003 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | US-005 | Must Have | DEP-001, DEP-002 | CON-001 | TRD-001 | DEC-003 |
| BG-002 | US-004 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-002 | US-006 | Must Have | DEP-002 | CON-001 | TRD-001 | DEC-002 |
| BG-001 | US-007 | Must Have | DEP-004 | CON-001 | TRD-002 | DEC-004 |
| BG-001 | US-008 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | US-009 | Should Have | DEP-004 | CON-001 | TRD-001 | DEC-005 |
| BG-003 | US-010 | Should Have | DEP-005 | CON-001 | TRD-001 | DEC-005 |
| BG-001 | FR-001 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | FR-002 | Must Have | DEP-002 | CON-001 | TRD-001 | DEC-002 |
| BG-001 | FR-003 | Must Have | DEP-003 | CON-001 | TRD-001 | DEC-001 |
| BG-002 | FR-004 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | FR-005 | Must Have | DEP-001, DEP-002 | CON-001 | TRD-001 | DEC-003 |
| BG-002 | FR-006 | Must Have | DEP-002 | CON-001 | TRD-001 | DEC-002 |
| BG-001 | FR-007 | Must Have | DEP-004 | CON-001 | TRD-002 | DEC-004 |
| BG-001 | FR-008 | Must Have | DEP-001 | CON-001 | TRD-001 | DEC-001 |
| BG-001 | FR-009 | Should Have | DEP-004 | CON-001 | TRD-001 | DEC-005 |
| BG-003 | FR-010 | Should Have | DEP-005 | CON-001 | TRD-001 | DEC-005 |

## 12. Quality Check Result
| Check | Result | Catatan |
|---|---|---|
| Lengkap | Lulus | Semua item utama, konflik, dependency, MoSCoW, trade-off, dan traceability dicatat |
| Konsisten | Lulus | Prioritas selaras dengan tujuan bisnis dan scope |
| Tidak ambigu | Sebagian lulus | Beberapa effort dan threshold masih belum tersedia |
| Traceable | Lulus | Setiap keputusan terhubung ke business goal, source, dependency, atau trade-off |
| Terjustifikasi | Lulus | Setiap prioritas memiliki alasan eksplisit |
| Feasible | Lulus | Item Must Have tidak dipilih tanpa mempertimbangkan dependency |
| Transparan | Lulus | Trade-off dan ketidakpastian dicatat terbuka |
| Bernilai bisnis | Lulus | Fokus pada alur inti yang paling mendukung tujuan sistem |
| Tervalidasi | Sebagian lulus | Beberapa item masih pending validation atau assumption |
