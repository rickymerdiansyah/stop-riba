# Changelog

## v0.2 — 2026-11-06
Menerapkan mockup final.
- **Intro pertama buka** (2 layar): penjelasan singkat + isi penghasilan dan batas aman cicilan (30/35/40%). Bisa dilewati.
- **Beranda kosong** tanpa angka Rp 0: tombol tambah hutang, checklist "Mulai dari sini" (hutang pertama, penghasilan, backup), panduan memilih jadwal.
- **Beranda bertahap**: banner telat bayar (dengan perkiraan denda dan status SLIK) atau jatuh tempo ≤3 hari di paling atas, sisa outstanding, ringkasan bulan ini (atau 30 hari ke depan), jatuh tempo terdekat, daftar hutang. Total bunga dan tanggal bebas hutang dipindah ke Strategi.
- **Kalender & Strategi kosong** punya penjelasan apa yang akan muncul.
- **Risiko kalau telat** di form tambah/edit hutang: legalitas, SLIK OJK, penagihan lapangan, denda, jaminan, auto-debet, akses kontak. Terisi otomatis dari jenis hutang, menghasilkan level risiko dan linimasa konsekuensi. Ditampilkan juga di kartu hutang dan detail.

## v0.1 — 2026-11-06
Versi pertama prototype.
- Beranda (sisa outstanding, jatuh tempo terdekat, daftar hutang), Kalender, Strategi, Lainnya.
- Tambah hutang: jadwal tiap bulan, per hari, dan manual per cicilan; potongan di awal; jenis hutang custom.
- Bunga flat, bunga efektif, dan cek batas OJK untuk pinjol.
- Tandai lunas, denda, pelunasan dipercepat, riwayat pembayaran.
- Backup/pulihkan JSON dan export CSV.
