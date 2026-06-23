## Example Invocation
Gunakan $validation-change untuk menilai perubahan fitur checkout berikut, lalu laporkan gap requirement, risiko implementasi, dan pertanyaan klarifikasi yang masih perlu dijawab.

## Expected Output Example
```text
Ringkasan
- Perubahan ini sebagian jelas, tetapi masih ada gap pada scope, kriteria sukses, dan dampak integrasi.

Asumsi
- A1: Semua referensi mengacu pada modul checkout yang sama.

Temuan Validasi
- V-01 | RQ-1 | clarity | Istilah "cepat" tidak terukur. Ganti dengan target waktu respons.
- V-02 | RQ-3 | testability | Acceptance criteria belum bisa diuji karena tidak ada kondisi lulus/gagal yang eksplisit.

Traceability
- RQ-1 -> UI checkout
- RQ-2 -> Payment service
- RQ-3 -> Test scenario belum tersedia

Impact Analysis
- Integrasi payment, test regression, dan dokumentasi release perlu diperbarui.

Pertanyaan Klarifikasi
- Apakah target respons yang dimaksud adalah p95 < 2 detik?

Rekomendasi
- Perjelas metrik, tambahkan acceptance criteria terukur, lalu validasi ulang.
```
