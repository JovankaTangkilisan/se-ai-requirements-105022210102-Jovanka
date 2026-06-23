## Example Invocation

```
Saya ingin membuat inception document untuk proyek baru kami.

Nama proyek: SiPantau — Sistem Pemantauan Aset Daerah
Organisasi: Dinas PUPR Kota Manado
Masalah: Pencatatan aset infrastruktur masih manual menggunakan Excel, sering terjadi data ganda dan kehilangan data saat pergantian pegawai.
Tujuan: Digitalisasi pencatatan aset, audit trail, dan laporan otomatis ke BPK.
Stakeholder: Kepala Dinas, Staf Aset, Auditor Internal, BPK
Deadline: Go-live Q1 2026
Platform: Web-based, harus bisa diakses dari mobile browser
```

---

## Expected Output Example

```markdown
# Inception Document: SiPantau — Sistem Pemantauan Aset Daerah

**Versi:** 0.1  
**Tanggal:** 2025-06-23  
**Penulis:** [ASUMSI: Tim Analisis Dinas PUPR]  
**Status:** Draft

---

## 1. Masalah Bisnis

### 1.1 Latar Belakang
Dinas PUPR Kota Manado saat ini mengelola aset infrastruktur menggunakan spreadsheet Excel yang dikelola secara manual oleh staf. Sistem ini tidak memiliki mekanisme kontrol versi, audit trail, atau sinkronisasi antar pengguna.

### 1.2 Problem Statement
Saat ini, staf aset Dinas PUPR mengalami kesulitan menjaga akurasi data aset infrastruktur yang menyebabkan duplikasi data dan kehilangan riwayat aset saat terjadi pergantian pegawai. Hal ini terjadi karena tidak adanya sistem terpusat dengan kontrol akses dan pencatatan perubahan.

### 1.3 Dampak Bisnis
- Risiko temuan audit BPK akibat data aset yang tidak akurat
- Waktu rekonsiliasi data manual diperkirakan [BELUM DIDEFINISIKAN] jam per bulan [ASUMSI: signifikan berdasarkan deskripsi masalah]

---

## 2. Tujuan Proyek

| ID | Tujuan | Metrik Keberhasilan | Target |
|----|--------|---------------------|--------|
| BG-01 | Digitalisasi pencatatan aset | 100% aset terdaftar dalam sistem | Q1 2026 |
| BG-02 | Audit trail tersedia | Setiap perubahan data terekam dengan user dan timestamp | Go-live |
| BG-03 | Laporan otomatis ke BPK | Laporan dapat diekspor dalam format yang diterima BPK | Q1 2026 |

---

## 4. Scope

### 4.1 Dalam Scope
| ID | Fitur | Prioritas |
|----|-------|-----------|
| SC-IN-01 | Registrasi dan pencatatan aset infrastruktur | Must Have |
| SC-IN-02 | Audit trail setiap perubahan data | Must Have |
| SC-IN-03 | Ekspor laporan untuk BPK | Must Have |
| SC-IN-04 | Akses via mobile browser | Should Have |

### 4.2 Di Luar Scope
| ID | Yang Tidak Dikerjakan | Alasan |
|----|----------------------|--------|
| SC-OUT-01 | Aplikasi mobile native (iOS/Android) | [ASUMSI] Tidak disebutkan, mobile browser sudah cukup |
| SC-OUT-02 | Integrasi sistem keuangan BPKAD | [BELUM DIDEFINISIKAN — perlu konfirmasi] |

---

## 7. Open Questions

| ID | Pertanyaan | Pemilik | Deadline | Dampak |
|----|-----------|---------|----------|--------|
| OQ-01 | Format laporan BPK yang diterima (Excel/PDF/XML)? | Auditor Internal | 2025-07-15 | Tinggi |
| OQ-02 | Apakah perlu integrasi dengan sistem BPKAD? | Kepala Dinas | 2025-07-15 | Tinggi |
| OQ-03 | Berapa jumlah aset yang akan dimigrasi dari Excel? | Staf Aset | 2025-07-30 | Sedang |
```