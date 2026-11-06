# STOP RIBA — Jurnal Hutang

Web app satu halaman untuk mencatat hutang (kartu kredit, pinjol, paylater, KTA, dan jenis lain), memantau jatuh tempo, dan melunasinya dengan urutan paling hemat. Dibuka di HP lewat browser, bisa di-*Add to Home Screen*.

**Link:** https://rickymerdiansyah.github.io/stop-riba/

## Fitur
- Tambah hutang dengan 3 jenis jadwal: tiap bulan, per hari (total hari ÷ jumlah cicilan), atau manual per cicilan (pokok + bunga, sesuai aplikasi pinjol).
- Hitung bunga flat (cara OJK) dan bunga efektif (bunga riil dari dana yang diterima), plus cek batas manfaat ekonomi pinjol OJK.
- Tandai lunas per cicilan, catat denda, pelunasan dipercepat.
- Kalender jatuh tempo, strategi urutan pelunasan, rasio cicilan vs penghasilan.
- Jenis hutang bisa ditambah sendiri.
- Backup / pulihkan (JSON) dan export CSV.

## Penyimpanan data
- Dibuka dari GitHub Pages: data tersimpan di browser perangkat itu saja (localStorage). Rutin backup lewat **Lainnya → Backup (JSON)**.
- Dibuka dari link artifact Claude: data juga tersinkron ke akun Claude pemiliknya.
- Tidak ada data hutang yang disimpan di repo ini.

## Alur revisi & QA
1. Revisi dikerjakan di branch terpisah dan dibuka sebagai Pull Request berisi daftar yang perlu dites.
2. Setelah dites dan disetujui, PR di-merge ke `main`.
3. GitHub Actions otomatis deploy ke GitHub Pages (± 1–2 menit).
4. Kalau ada masalah, revert commit merge-nya.

Catatan perubahan per versi ada di [CHANGELOG.md](CHANGELOG.md).
