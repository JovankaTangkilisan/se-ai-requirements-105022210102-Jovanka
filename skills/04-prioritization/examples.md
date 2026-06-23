## Example Invocation
```text
Gunakan skill software-engineering-prioritization untuk memprioritaskan backlog fitur aplikasi pemesanan klinik. Sertakan konflik stakeholder, dependency, MoSCoW, trade-off, alasan keputusan, dan traceability matrix. Gunakan bahasa Indonesia dan tandai asumsi secara eksplisit.
```

## Expected Output Example
```markdown
# Prioritization Report: Aplikasi Pemesanan Klinik

## 1. Tujuan Prioritisasi
- Tujuan prioritisasi: Menentukan scope MVP untuk rilis pertama.
- Business goal: Mengurangi proses pemesanan manual melalui telepon.
- Target rilis / periode keputusan: MVP rilis pertama.
- Stakeholder utama: Pasien, resepsionis, dokter, manajemen klinik.
- Constraint utama: Jadwal dokter harus tersedia sebelum pasien dapat memilih slot.
- Kriteria keputusan: Business value, dependency, risiko operasional, dan kesiapan MVP.

## 3. Item yang Diprioritaskan
| Item ID | Item | Jenis | Source | Business Value | Effort / Complexity | Status Validasi |
|---|---|---|---|---|---|---|
| FEAT-001 | Pasien memilih slot janji temu yang tersedia | Fitur | SRC-001 | Mengurangi panggilan manual untuk pemesanan | Medium | Pending Validation |
| FEAT-002 | Pembayaran online sebelum janji temu | Fitur | SRC-002 | Mengurangi risiko no-show | High | Assumption |

## 4. Konflik Stakeholder
| Conflict ID | Stakeholder Terkait | Konflik | Dampak | Keputusan / Status | Klarifikasi Dibutuhkan |
|---|---|---|---|---|---|
| CON-001 | Manajemen klinik, pasien | Manajemen ingin pembayaran wajib sebelum booking, sedangkan kebutuhan pasien tentang metode pembayaran belum divalidasi. | Dapat menurunkan conversion jika metode pembayaran tidak sesuai. | Pending Decision | Validasi preferensi pembayaran pasien dan kebijakan klinik. |

## 5. Dependency Analysis
| Dependency ID | Item Terkait | Dependency | Jenis Dependency | Dampak Jika Tidak Terpenuhi | Status |
|---|---|---|---|---|---|
| DEP-001 | FEAT-001 | Data jadwal dokter harus tersedia dan sinkron. | Data / sistem | Pasien dapat memilih slot yang tidak valid. | Critical |

## 6. MoSCoW Prioritization
| Item ID | Item | MoSCoW | Alasan Kategori | Dependency | Risiko | Status Validasi |
|---|---|---|---|---|---|---|
| FEAT-001 | Pasien memilih slot janji temu yang tersedia | Must Have | Tanpa fitur ini MVP tidak memenuhi tujuan utama pemesanan online. | DEP-001 | Risiko double booking jika data jadwal tidak valid. | Pending Validation |
| FEAT-002 | Pembayaran online sebelum janji temu | Should Have | Bernilai untuk mengurangi no-show, tetapi MVP masih dapat berjalan dengan pembayaran di klinik. | Belum ada dependency pembayaran yang tervalidasi | Risiko integrasi dan conversion belum diketahui. | Assumption |

## 7. Trade-Off Analysis
| Trade-Off ID | Keputusan | Opsi yang Dibandingkan | Yang Diperoleh | Yang Dikorbankan | Risiko | Alasan Keputusan |
|---|---|---|---|---|---|---|
| TRD-001 | Menunda pembayaran online dari Must Have menjadi Should Have | Pembayaran online di MVP vs pembayaran di klinik | MVP lebih cepat fokus pada booking inti | Risiko no-show belum ditangani penuh | No-show tetap perlu mitigasi manual | Dependency dan preferensi pembayaran belum tervalidasi. |

## 8. Decision Rationale
| Decision ID | Item / Konflik / Trade-Off | Keputusan | Alasan | Evidence / Source | Assumption | Owner Validasi |
|---|---|---|---|---|---|---|
| DEC-001 | FEAT-001 | Prioritas Must Have | Fitur langsung mendukung business goal mengurangi booking manual. | SRC-001 | Tidak | Product Owner |
| DEC-002 | FEAT-002 | Prioritas Should Have | Business value ada, tetapi dependency pembayaran dan preferensi pasien belum tervalidasi. | SRC-002 | Ya, ASM-001 | Product Owner |

## 9. Rekomendasi Prioritas
### Must Have
- FEAT-001: Pasien memilih slot janji temu yang tersedia.

### Should Have
- FEAT-002: Pembayaran online sebelum janji temu.

### Could Have
- Belum ada item yang didukung konteks.

### Won't Have
- Belum ada item yang didukung konteks.

## 11. Traceability Matrix
| Business Goal | Item ID | MoSCoW | Dependency ID | Conflict ID | Trade-Off ID | Decision ID |
|---|---|---|---|---|---|---|
| Mengurangi proses pemesanan manual melalui telepon | FEAT-001 | Must Have | DEP-001 | Tidak ada | Tidak ada | DEC-001 |
| Mengurangi risiko no-show | FEAT-002 | Should Have | Pending | CON-001 | TRD-001 | DEC-002 |

## 12. Quality Check Result
| Check | Result | Catatan |
|---|---|---|
| Lengkap | Pass | Konflik, dependency, MoSCoW, trade-off, dan alasan keputusan tersedia. |
| Traceable | Pass | Keputusan DEC-001 dan DEC-002 terhubung ke item dan business goal. |
| Validasi | Needs Follow-Up | Pembayaran online masih asumsi dan membutuhkan validasi stakeholder. |
```

