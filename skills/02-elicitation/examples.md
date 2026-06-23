## Example Invocation
```text
Gunakan skill software-engineering-elicitation untuk menganalisis catatan stakeholder berikut tentang sistem booking janji temu rumah sakit. Identifikasi teknik elicitation, pertanyaan wawancara, kebutuhan eksplisit, kebutuhan implisit, functional requirements, non-functional requirements, temuan, dan pertanyaan terbuka. Gunakan requirement ID dan tandai asumsi dengan jelas.
```

## Expected Output Example
```markdown
# Laporan Elicitation: Booking Janji Temu Rumah Sakit

## 1. Tujuan Elicitation
- Tujuan: Mengidentifikasi requirement untuk membuat, mengubah, dan membatalkan janji temu pasien.
- Tujuan bisnis: Mengurangi panggilan manual untuk penjadwalan dan meningkatkan visibilitas jadwal.
- Stakeholder: Pasien, staf resepsionis, dokter, administrator klinik.
- Scope: Pencarian jadwal, booking, reschedule, cancellation, notifikasi, dan visibilitas kalender staf.

## 3. Teknik Elicitation
| Technique ID | Teknik | Tujuan | Stakeholder / Sumber | Alasan Pemilihan |
|---|---|---|---|---|
| TECH-001 | Wawancara stakeholder | Memahami pain point dan aturan booking | Pasien, staf resepsionis | Input langsung dibutuhkan untuk memahami workflow dan exception. |
| TECH-002 | Document analysis | Meninjau kebijakan penjadwalan yang ada | Dokumen kebijakan klinik | Business rules harus berdasarkan kebijakan yang berlaku. |

## 4. Pertanyaan Wawancara
| Question ID | Peran Stakeholder | Pertanyaan | Tujuan | Pemicu Follow-Up |
|---|---|---|---|---|
| Q-001 | Staf resepsionis | Perubahan janji temu seperti apa yang saat ini membutuhkan persetujuan manual? | Mengidentifikasi business rules dan exception. | Jika persetujuan bergantung pada dokter, spesialisasi, atau jenis janji temu. |
| Q-002 | Pasien | Informasi apa yang Anda butuhkan sebelum memilih slot janji temu? | Mengidentifikasi kebutuhan tampilan data. | Jika pasien menyebut biaya, dokter, lokasi, atau instruksi persiapan. |

## 5. Kebutuhan Eksplisit
| Need ID | Stakeholder / Sumber | Kebutuhan yang Dinyatakan | Evidence | Business Value |
|---|---|---|---|---|
| NEED-001 | Staf resepsionis | Staf perlu melihat ketersediaan dokter sebelum mengonfirmasi booking. | Catatan stakeholder | Mengurangi double booking dan koreksi manual. |

## 6. Kebutuhan Implisit dan Asumsi
| Assumption ID | Kebutuhan yang Diinferensi | Dasar Inferensi | Validasi yang Dibutuhkan | Risiko jika Salah |
|---|---|---|---|---|
| ASM-001 | Pasien mungkin membutuhkan pesan konfirmasi otomatis. | Workflow booking mencakup konfirmasi janji temu, tetapi channel belum disebutkan. | Konfirmasi channel notifikasi yang diinginkan dengan pasien dan staf klinik. | Pasien dapat melewatkan janji temu atau menerima pesan melalui channel yang tidak didukung. |

## 7. Functional Requirements
| Requirement ID | Requirement | Source Need | Priority | Acceptance Criteria | Validation Status |
|---|---|---|---|---|---|
| FR-001 | Sistem harus menampilkan slot janji temu yang tersedia berdasarkan dokter, tanggal, dan jenis janji temu. | NEED-001 | High | AC-001: Given staf memilih dokter dan tanggal, when staf mencari ketersediaan, then sistem hanya menampilkan slot yang belum terisi untuk dokter dan tanggal tersebut. | Menunggu Validasi |

## 8. Non-Functional Requirements
| Requirement ID | Quality Attribute | Requirement | Measurement / Threshold | Source Need | Validation Status |
|---|---|---|---|---|---|
| NFR-001 | Performance | Pencarian ketersediaan janji temu harus mengembalikan hasil dalam waktu maksimal 2 detik untuk 95% pencarian selama jam operasional klinik. | 95th percentile response time <= 2 detik | ASM-001 | Asumsi |

## 9. Temuan Elicitation
### Temuan Utama
- Visibilitas ketersediaan staf dan dokter penting untuk mencegah double booking.
- Requirement channel notifikasi belum tervalidasi.

### Gap dan Pertanyaan Terbuka
- Channel notifikasi apa yang diperbolehkan: SMS, email, WhatsApp, atau in-app notification?
- Siapa yang boleh melakukan override terhadap slot yang tidak tersedia?

## 11. Hasil Quality Check
| Check | Hasil | Catatan |
|---|---|---|
| Traceable | Lulus | FR-001 terhubung ke NEED-001. NFR-001 terhubung ke ASM-001. |
| Testable | Lulus | Requirement memiliki acceptance criteria atau threshold yang terukur. |
| Validated | Perlu Follow-Up | Perilaku notifikasi masih berupa asumsi. |
```
