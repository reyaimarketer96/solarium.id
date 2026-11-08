# DESIGN.md · Solarium (DRAF, belum disetujui pemilik)

Status: draf yang disusun dari diskusi 8 Nov 2026 ("tidak ada aura renewable", "kalah telak sama SolarSquare"). Ganti status jadi "disetujui" setelah pemilik setuju. Sampai saat itu, semua mockup yang memakai file ini berstatus draf.

## Identitas

- **Siapa:** kontraktor PLTS atap baru untuk rumah dan bisnis di Indonesia. Perusahaan pemula, jadi bukti dibangun dari proyek pertama, bukan diklaim besar.
- **Kepribadian:** jujur soal angka, tenang, praktis. Bicara seperti teknisi yang bisa dipercaya, bukan seperti brosur properti mewah.
- **Suasana:** pagi tropis. Cahaya siang, atap, daun. Bukan malam, bukan dashboard teknologi.

## Palet (2 inti + 1 aksen)

| Peran | Hex | Alasan |
|---|---|---|
| Inti 1: hijau daun | `#17533B` | Warna tumbuhan tropis yang matang, membaca sebagai energi bersih tanpa hijau neon |
| Inti 2: tinta | `#0F1F19` | Teks dan latar gelap. Kehijauan supaya serumpun dengan inti 1 |
| Aksen: amber matahari | `#F0A531` | Hanya untuk aksi utama (tombol "Cek Potensi Hemat") dan satu sorotan di hero |
| Netral | `#FFFFFF`, `#F6F3EC`, `#5A665F` | Latar putih, krem hangat untuk section jeda, abu teks sekunder (6:1 di putih) |

Tombol WhatsApp memakai `#12774A`: turunan inti 1 yang tetap terbaca sebagai WhatsApp, bukan warna baru.

Teks putih di atas amber dilarang (2,07:1). Teks di atas amber memakai `#2A1A02`.

## Tipografi

- **Plus Jakarta Sans** (400–800). Alasannya, huruf ini dirancang untuk identitas kota Jakarta. Bentuknya geometris tapi hangat, cocok untuk merek Indonesia yang ingin terlihat modern tanpa dingin.
- Judul 800, rapat (-0,025em). Badan 16–17 px, 400.
- Tanpa label huruf kapital ber-tracking lebar.

## Dial

`ENERGY 2 / RHYTHM 2 / MOTION 1`

- ENERGY 2: percaya diri, tapi produknya atap dan tagihan, bukan pameran.
- RHYTHM 2: konsisten, dengan sedikit selingan (section gelap, section foto penuh).
- MOTION 1: hanya hover dan transisi pendek. Tidak ada animasi berulang.

## Fotografi

- Rumah tropis Indonesia, cahaya pagi atau sore, panel hitam yang rapi.
- Foto AI boleh untuk suasana dan wajib berlabel "Ilustrasi". Foto AI tidak boleh dipakai sebagai proyek, pelanggan, atau tim.
- Close-up instalasi wajib foto asli (AI sering salah detail teknis).

## Bukti dan angka

- Angka, rating, dan testimoni hanya dari data asli. Sebelum ada, tampilkan slot `[data asli]`, bukan angka karangan.
- Kalkulator memakai rentang dan batas fisik sistem, tidak pernah persentase tagihan yang tetap.

## Belum diputuskan

- Logo final (sekarang dipakai wordmark teks).
- Motif identitas.
- Isi "Paket Tenang" (garansi, kunjungan perawatan).
