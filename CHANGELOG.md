# Changelog

## v0.8 — 2026-11-07
- **Model denda**: % per hari, % per bulan, atau nominal tetap, plus batas maksimal. Kartu kredit otomatis ikut aturan BI (maks 1% tagihan, maks Rp100.000). Perkiraan denda tampil di banner telat dan detail hutang.
- **Pelunasan dipercepat**: isian penalti %. Untuk bunga anuitas ada pelunasan sebagian dengan pilihan angsuran turun atau tenor lebih pendek, lengkap dengan perkiraan hemat bunga.
- **Paylater per akun**: banyak transaksi (30 hari / cicilan 3–12 bulan + biaya %/bulan) digabung jadi satu tagihan per bulan, dengan limit terpakai dan daftar transaksi.

## v0.7 — 2026-11-07
- **KPR / KKB**: maksimal 360 cicilan. Cara hitung bunga: isi total bunga, flat % per tahun, atau anuitas % per tahun dengan masa fixed lalu floating.
- **Bunga berubah (floating)**: hitung ulang angsuran dari sisa pokok mulai cicilan tertentu.
- Sisa pokok tampil di detail dan tiap cicilan. Jenis KPR & KKB ditambahkan ke daftar jenis bawaan.

## v0.6 — 2026-11-07
- **Kartu kredit dicatat per lembar tagihan**: form khusus kartu (nama, limit opsional, tanggal cetak & jatuh tempo tiap bulan, bunga per bulan default 1,75%, minimum 5%) plus lembar tagihan pertama.
- **Bayar tagihan**: pilih Bayar penuh, Bayar minimum, atau Nominal lain. Langsung terlihat sisa yang dibawa ke bulan depan, perkiraan bunga, dan perkiraan tagihan berikutnya. Bayar minimum = status "Dibayar sebagian", bukan lunas.
- **Tagihan berikutnya (perkiraan)** muncul otomatis setelah bayar sebagian; catat lembar tagihan baru dengan sisa & bunga terisi otomatis, tinggal isi belanja baru.
- Peringatan "bayar minimum terus": perkiraan lama lunas dan total bunga.
- Detail kartu: sisa tagihan, pemakaian limit, riwayat tagihan per bulan.
- Data kartu kredit lama (1 cicilan) otomatis dikonversi ke format lembar tagihan.

## v0.5 — 2026-11-06
- Fix: impor backup bisa langsung dari beranda kosong ("Sudah punya backup? Impor file .json") dan dari layar intro ("Sudah punya backup? Pulihkan data").
- Header di HP layar sempit: label status sinkron disembunyikan supaya ikon gear (Lainnya) tidak terdorong keluar layar.
- Logo STOP RIBA (bunga dicoret) sebagai ikon Add to Home Screen di iPhone & Android, favicon, dan manifest dengan nama "STOP RIBA".

## v0.4 — 2026-11-06
- **Beranda fokus 7 hari ke depan**: ringkasan sisa outstanding & tagihan bulan ini, banner telat, lalu tagihan 7 hari ke depan per tanggal (bisa dibuka-tutup, centang lunas langsung).
- **Tab baru "Hutang"**: semua hutang digabung per pemberi pinjaman, dengan pencarian, filter jenis & status (telat, 7 hari, perlu dilengkapi, sudah lunas), dan urutan jatuh tempo / sisa terbesar.
- Navigasi: Beranda · Hutang · + · Kalender · Strategi. Menu Lainnya pindah ke ikon gear di kanan atas.
- Penanda untuk data migrasi dari reminder Telegram: "Perlu dilengkapi" dan "Sebagian cicilan diperkirakan". Hilang otomatis setelah hutang diedit dan disimpan.
- Fix: tanggal bebas hutang di Strategi sekarang memakai tenor terakhir yang benar.

## v0.3 — 2026-11-06
- **Angsuran per cicilan bisa diedit** di jadwal Tiap bulan dan Per hari. Awalnya dibagi rata dari nominal pengembalian; begitu satu angsuran diubah, nominal pengembalian dan bunga mengikuti total angsuran. Tombol "Bagi rata ulang" untuk kembali ke pembagian rata.
- Mengubah jumlah cicilan atau tanggal tidak menghapus angsuran yang sudah diedit.
- **Jadwal Manual jadi satu kolom "Angsuran"** per cicilan (tanpa pecahan pokok dan bunga). Bunga dan nominal pengembalian dihitung otomatis dari total angsuran.
- Validasi baru: cicilan tidak boleh jatuh tempo sebelum tanggal dana cair atau lewat due date pengembalian.

## v0.2 — 2026-11-06
Menerapkan mockup final.
- **Intro pertama buka** (2 layar): penjelasan singkat + isi penghasilan dan batas aman cicilan (30/35/40%). Bisa dilewati.
- **Beranda kosong** tanpa angka Rp 0: tombol tambah hutang, checklist "Mulai dari sini" (hutang pertama, penghasilan, backup), panduan memilih jadwal.
- **Beranda bertahap**: banner telat bayar (dengan perkiraan denda dan status SLIK) atau jatuh tempo ≤3 hari di paling atas, sisa outstanding, ringkasan bulan ini (atau 30 hari ke depan), jatuh tempo terdekat, daftar hutang. Total bunga dan tanggal bebas hutang dipindah ke Strategi.
- **Kalender & Strategi kosong** punya penjelasan apa yang akan muncul.
- **Form nominal & tanggal (semua jenis hutang)**: Nominal pinjaman, Pinjaman diterima, Bunga, Nominal pengembalian. Potongan di awal = nominal pinjaman − pinjaman diterima; pengembalian = nominal pinjaman + bunga (bisa diisi dari dua arah). Tanggal dana cair + Due date pengembalian (max tenor) menentukan lama pinjaman dan jadwal cicilan.
- **Risiko kalau telat** di form tambah/edit hutang: legalitas, SLIK OJK, penagihan lapangan, denda, jaminan, auto-debet, akses kontak. Terisi otomatis dari jenis hutang, menghasilkan level risiko dan linimasa konsekuensi. Ditampilkan juga di kartu hutang dan detail.

## v0.1 — 2026-11-06
Versi pertama prototype.
- Beranda (sisa outstanding, jatuh tempo terdekat, daftar hutang), Kalender, Strategi, Lainnya.
- Tambah hutang: jadwal tiap bulan, per hari, dan manual per cicilan; potongan di awal; jenis hutang custom.
- Bunga flat, bunga efektif, dan cek batas OJK untuk pinjol.
- Tandai lunas, denda, pelunasan dipercepat, riwayat pembayaran.
- Backup/pulihkan JSON dan export CSV.
