## Example Invocation
```text
Gunakan skill software-engineering-specification untuk membuat spesifikasi fitur checkout e-commerce dari catatan stakeholder berikut. Sertakan functional requirements, non-functional requirements, business rules, user stories, acceptance criteria, dan traceability matrix. Gunakan bahasa Indonesia dan tandai asumsi secara eksplisit.
```

## Expected Output Example
```markdown
# Software Requirements Specification: Checkout E-Commerce

## 1. Ringkasan
- Nama proyek/fitur: Checkout E-Commerce
- Tujuan bisnis: Mengurangi kegagalan transaksi dan mempercepat proses pembelian.
- Stakeholder: Pembeli, admin toko, tim operasional, tim pembayaran.
- Pengguna utama: Pembeli.
- Ruang lingkup: Keranjang, alamat pengiriman, metode pembayaran, ringkasan pesanan, dan konfirmasi pesanan.
- Di luar ruang lingkup: Retur barang dan refund.

## 3. Business Goals
| Goal ID | Business Goal | Metrik Keberhasilan | Prioritas |
|---|---|---|---|
| BG-001 | Mengurangi kegagalan checkout | Persentase checkout gagal turun dari baseline yang disepakati | High |

## 4. User Stories
| User Story ID | User Story | Business Goal | Prioritas | Status Validasi |
|---|---|---|---|---|
| US-001 | Sebagai pembeli, saya ingin melihat ringkasan pesanan sebelum membayar, sehingga saya dapat memverifikasi item, harga, dan alamat pengiriman. | BG-001 | High | Pending Validation |

## 5. Functional Requirements
| Requirement ID | Functional Requirement | User Story / Source | Prioritas | Acceptance Criteria | Status Validasi |
|---|---|---|---|---|---|
| FR-001 | Sistem harus menampilkan ringkasan pesanan yang berisi daftar item, jumlah item, subtotal, biaya pengiriman, total pembayaran, dan alamat pengiriman sebelum pembeli melakukan pembayaran. | US-001 | High | AC-001 | Pending Validation |

## 6. Non-Functional Requirements
| Requirement ID | Atribut Kualitas | Non-Functional Requirement | Ukuran / Threshold | Source | Status Validasi |
|---|---|---|---|---|---|
| NFR-001 | Performance | Halaman ringkasan checkout harus tampil dalam waktu maksimal 2 detik untuk 95% request pada kondisi beban normal yang disepakati. | P95 load time <= 2 detik | ASM-001 | Assumption |

## 7. Business Rules
| Rule ID | Business Rule | Kondisi | Pengecualian | Requirement Terkait | Status Validasi |
|---|---|---|---|---|---|
| BR-001 | Pembeli tidak dapat melanjutkan pembayaran jika alamat pengiriman belum dipilih. | Saat pembeli menekan tombol bayar | Tidak ada pengecualian yang diberikan | FR-001 | Pending Validation |

## 8. Acceptance Criteria
| Acceptance Criteria ID | Requirement / User Story | Given | When | Then | Tipe Skenario |
|---|---|---|---|---|---|
| AC-001 | FR-001 | Pembeli memiliki item di keranjang dan alamat pengiriman telah dipilih | Pembeli membuka halaman checkout | Sistem menampilkan item, jumlah, subtotal, biaya pengiriman, total pembayaran, dan alamat pengiriman | Positive |

## 9. Traceability Matrix
| Business Goal | User Story ID | Requirement ID | Business Rule ID | Acceptance Criteria ID | Status |
|---|---|---|---|---|---|
| BG-001 | US-001 | FR-001 | BR-001 | AC-001 | Pending Validation |

## 11. Quality Check Result
| Check | Result | Catatan |
|---|---|---|
| Lengkap | Pass | FR, NFR, BR, US, dan AC tersedia. |
| Dapat diuji | Pass | FR-001 memiliki AC-001. NFR-001 memiliki threshold. |
| Traceable | Pass | BG-001 terhubung ke US-001, FR-001, BR-001, dan AC-001. |
| Validasi | Needs Follow-Up | NFR-001 masih asumsi karena baseline beban normal belum diberikan. |
```