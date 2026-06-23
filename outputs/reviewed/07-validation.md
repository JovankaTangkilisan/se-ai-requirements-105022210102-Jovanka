# Validation Change Report: Student Task Management System

## 1. Ringkasan
- Perubahan yang divalidasi: Paket dokumen requirements untuk Student Task Management System, mencakup inception, elicitation, specification, dan prioritization.
- Fokus validasi: clarity, completeness, consistency, feasibility, testability, traceability, dan impact analysis.
- Status umum: Sebagian besar alur inti sudah konsisten dan traceable, tetapi beberapa bagian masih belum cukup terukur untuk diputuskan final.
- Keputusan keseluruhan: Belum siap final tanpa klarifikasi untuk threshold NFR, detail laporan, notifikasi, dan beberapa dependency bisnis.

## 2. Asumsi
| Assumption ID | Asumsi | Alasan | Validasi yang Dibutuhkan | Risiko Jika Salah |
|---|---|---|---|---|
| ASM-001 | `[ASUMSI]` Semua referensi mengarah ke paket dokumen Student Task Management System yang sama | Agar validation dilakukan pada satu baseline | Konfirmasi bahwa seluruh dokumen memang satu rangkaian | Salah menilai dokumen yang tidak saling terkait |
| ASM-002 | `[ASUMSI]` Item dengan status `Pending Validation` dan `Assumption` belum final | Untuk membedakan temuan final dan temuan sementara | Konfirmasi status validasi yang diinginkan stakeholder | Keputusan bisa dianggap final padahal belum tervalidasi |
| ASM-003 | `[ASUMSI]` Target utama validasi adalah kesiapan requirement untuk desain dan implementasi awal, bukan desain teknis detail | Sesuai konteks dokumen yang diberikan | Konfirmasi fase proyek | Validasi bisa terlalu longgar atau terlalu ketat |

## 3. Temuan Validasi
| Finding ID | Referensi | Dimensi | Dampak Bisnis / Teknis | Saran Perbaikan |
|---|---|---|---|---|
| FV-001 | `specification.md` bagian 6, 7, 11 | testability, consistency | Beberapa NFR masih memakai placeholder seperti `[BELUM DIDEFINISIKAN — diperlukan metrik usability]`, sehingga belum dapat diuji final | Tetapkan threshold terukur untuk usability, performance, reliability, dan state jelas metode uji yang dipakai |
| FV-002 | `specification.md` bagian 6.3, 7, 10 | completeness, traceability | `CON-REG-01` belum didefinisikan, padahal sistem kampus bisa saja memiliki aturan privasi, akademik, atau kepatuhan internal | Tambahkan sumber regulasi atau tandai eksplisit bahwa tidak ada regulasi khusus yang berlaku |
| FV-003 | `specification.md` bagian 7-8 | clarity, testability | Beberapa business rule masih berstatus `Assumption`, misalnya deadline tanggal/waktu, batas upload, dan RBAC, sehingga requirement turunan belum final | Validasi asumsi yang mempengaruhi alur inti sebelum design gate |
| FV-004 | `elicitation.md` bagian 6-8 | feasibility, completeness | Kebutuhan implisit seperti notifikasi deadline dan format laporan belum punya spesifikasi final, namun dipakai dalam NFR dan user story | Putuskan mana yang wajib di MVP dan mana yang ditunda |
| FV-005 | `prioritization.md` bagian 3-6 | consistency, traceability | Item prioritas tinggi sudah cocok dengan alur inti, tetapi effort/complexity masih `Belum didefinisikan`, sehingga trade-off belum kuat | Tambahkan estimasi effort atau kompleksitas untuk item utama sebelum final release planning |
| FV-006 | `inception-document.md` bagian 2, 7 | completeness, feasibility | Business goals masih memakai target yang belum didefinisikan, dan open questions masih banyak, sehingga level kesiapan keputusan belum penuh | Isi target kuantitatif untuk business goal dan selesaikan open questions utama |
| FV-007 | `validation-change` keseluruhan paket | impact analysis | Dampak pada UI, API, schema, dan test plan belum dibahas secara rinci dalam dokumen yang ada | Tambahkan impact analysis teknis terpisah sebelum implementasi |

## 4. Traceability
| Source / Item | Status Traceability | Catatan |
|---|---|---|
| `CASE.md` -> `inception-document.md` -> `elicitation.md` -> `specification.md` | Baik | Alur kebutuhan sudah konsisten dari konteks ke requirement formal |
| `specification.md` -> `prioritization.md` | Baik | Prioritas didasarkan pada user story, FR, dan business goal |
| `prioritization.md` -> `validation-change.md` | Baik | Item Must Have selaras dengan alur inti sistem |
| NFR dan business rules yang masih asumsi | Perlu validasi | Belum ada threshold final atau bukti regulasi spesifik |

## 5. Impact Analysis
- Dampak positif:
  - Alur inti sistem sudah jelas: dosen membuat tugas, mahasiswa melihat dan mengumpulkan tugas, dosen menilai, administrator mengelola data.
  - Prioritas MVP sudah fokus pada nilai bisnis utama dan dependency kritis.
  - Traceability antar dokumen cukup baik untuk baseline requirements.
- Dampak negatif / risiko:
  - Beberapa requirement masih belum bisa diuji secara final karena threshold belum tersedia.
  - Validasi NFR dan business rules masih bergantung pada asumsi.
  - Jika detail laporan dan notifikasi dipaksakan masuk MVP tanpa bukti tambahan, scope bisa melebar.

## 6. Pertanyaan Klarifikasi
- Apakah threshold usability, performance, dan reliability harus ditetapkan sebelum implementasi?
- Apakah notifikasi deadline wajib ada pada rilis awal, atau boleh masuk fase berikutnya?
- Format laporan apa yang wajib tersedia pada MVP?
- Apakah ada aturan regulasi atau kebijakan kampus yang harus ditulis sebagai constraint formal?
- Apakah deadline tugas harus selalu mencakup tanggal dan waktu?

## 7. Rekomendasi
- Finalkan threshold NFR sebelum dokumen dipakai sebagai acuan implementasi.
- Validasi asumsi yang memengaruhi alur inti, terutama deadline, RBAC, upload file, dan notifikasi.
- Tambahkan impact analysis teknis untuk UI, API, database schema, dan test plan.
- Pertahankan prioritas MVP pada alur inti tugas, pengumpulan, penilaian, dan kontrol akses.
- Tunda fitur reporting lanjutan dan detail operasional yang belum terukur sampai ada keputusan stakeholder.
