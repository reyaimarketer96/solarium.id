---
Focus Keyword: plts on grid
SEO Title (≤50 char): PLTS On Grid: Cara Kerja, Skema PLN & Biaya 2026
Meta Description (≤140 char): Ulasan sistem PLTS on grid: cara kerja grid-tie inverter tanpa baterai, regulasi kuota PLN terbaru, dan penghematan tagihan 70%. Simak infonya!
URL Slug: plts-on-grid
Kategori: Sistem PLTS (ID 4)
Status: Draft
---

# PLTS On Grid: Prinsip Kerja Grid-Tie Inverter, Regulasi Kuota PLN 2026, dan Analisis ROI

PLTS on grid (*grid-tied photovoltaic power system*) adalah konfigurasi pembangkit listrik tenaga surya yang bekerja secara tersinkronisasi langsung dengan jaringan transmisi dan distribusi [PT PLN (Persero)](https://web.pln.co.id/) tanpa memerlukan komponen baterai kimia penampung daya, di mana listrik arus searah (DC) yang diproduksi oleh modul surya atap dikonversi secara seketika oleh *grid-tie inverter* menjadi arus bolak-balik (AC) 220V/380V untuk langsung memasok peralatan listrik yang sedang aktif menyala di dalam properti.

Sistem *on-grid* merupakan tipe instalasi PLTS atap yang paling populer dan paling ekonomis di perkotaan karena mengeliminasi 40% hingga 50% biaya modal investasi awal yang biasanya terserap untuk pembelian bank baterai lithium. Pada siang hari yang cerah, rumah atau gedung komersial akan memprioritaskan pemakaian listrik dari panel surya, dan apabila kebutuhan listrik melebihi produksi panel, kekurangan daya akan disuplai secara mulus dan otomatis oleh jaringan PLN tanpa adanya kedipan tegangan sedikit pun.

---

## Prinsip Kerja dan Mekanisme Anti-Islanding Protection

Kunci utama operasional PLTS on grid terletak pada sinkronisasi frekuensi dan fasa tegangan antara inverter *grid-tied* dengan jaringan utilitas PLN:

```
[Matahari Terbit] ──► [Panel Surya Fotovoltaik] ──(Arus DC)──► [Grid-Tie Inverter MPPT]
                                                                      │
                                                ┌─────────────────────┴─────────────────────┐
                                                ▼                                           ▼
                                 [Beban Listrik Rumah Aktif]                 [Jaringan Distribusi Listrik PLN]
                                 (Prioritas Konsumsi Sendiri)                (Sinkronisasi Frekuensi 50 Hz)
```

1. **Sinkronisasi Tegangan & Frekuensi:** Inverter *grid-tie* secara aktif membaca gelombang sinus jaringan PLN. Begitu mendeteksi voltase 220V dan frekuensi stabil 50 Hz, inverter mulai menyuntikkan daya listrik dengan menaikkan amplitudo tegangan fraksional sebesar beberapa milivolt di atas tegangan grid untuk mengalirkan arus listrik menuju beban rumah.
2. **Prioritas Aliran Daya (*Self-Consumption*):** Sesuai hukum kelistrikan Kirchoff, arus listrik mengalir mengikuti jalur hambatan terpendek. Karena panel surya berada di atap gedung yang sama dengan beban listrik, daya surya akan diserap habis terlebih dahulu oleh lampu, komputer, lemari es, dan AC.
3. **Fitur Proteksi Anti-Islanding (IEEE 1547 / IEC 62116):** Ini adalah standar keselamatan wajib internasional dan PLN. Jika jaringan transmisi PLN mengalami pemadaman atau gangguan teknis gardu, inverter *on-grid* wajib memutus aliran daya secara otomatis dalam waktu kurang dari 100 milidetik ($t < 0,1\,	ext{detik}$). Tindakan ini mencegah listrik dari panel surya mengalir ke tiang listrik jalan (*islanding effect*) yang dapat membahayakan nyawa petugas pemeliharaan PLN yang sedang memperbaiki trafo.

---

## Skema Regulasi PLN Berdasarkan Permen ESDM No 2/2024

Sejak diundangkannya Peraturan Menteri Energi dan Sumber Daya Mineral ([Permen ESDM](https://www.esdm.go.id/)) Nomor 2 Tahun 2024, regulasi PLTS on grid di Indonesia mengalami perubahan signifikan yang wajib dipahami oleh pemilik rumah dan industri:

| Aspek Regulasi | Regulasi Lama (Permen ESDM 26/2021) | Regulasi Baru (Permen ESDM 2/2024) |
| :--- | :--- | :--- |
| **Mekanisme Ekspor-Impor Listrik** | Net-metering 100% (Kelebihan listrik diekspor memotong tagihan kWh) | **Zero Net-Metering (Ekspor daya tidak lagi dihitung sebagai pengurang tagihan)** |
| **Kapasitas Maksimal Instalasi** | Dibatasi maksimal 100% dari daya tersambung PLN | **Berdasarkan Kuota Pengembangan PLTS Atap PLN per Wilayah Sistem** |
| **Biaya Kapasitas (*Capacity Charge*)** | Berlaku untuk konsumen industri tertentu | **Dihapuskan sepenuhnya untuk pelanggan residensial & bisnis** |
| **Sistem Pengontrol Ekspor Daya** | Menggunakan meteran Exim digital bidirectional | **Wajib memasang Smart Metering / Zero Export Device (Smart Meter / CT Sensor)** |
| **Persetujuan Izin Sambung** | Waktu tunggu verifikasi tidak pasti | **Persetujuan kuota terstruktur (pengajuan dibuka tiap Januari & Juli)** |

Konsekuensi rekayasa dari regulasi baru ini adalah: **PLTS on grid harus didesain dengan kapasitas yang presisi sesuai kurva beban dasar (*baseload*) siang hari**, bukan sekadar menutupi total tagihan bulanan. Tim perencana [Solarium](https://solarium.id/wp/) menggunakan perangkat perekam data beban (*power quality logger*) untuk memastikan efisiensi penyerapan daya *self-consumption* mencapai di atas **90% hingga 95%** tanpa membuang energi sia-sia.

---

## Rumus dan Analisis Penghematan Finansial (ROI) PLTS On Grid

Karena sistem *on-grid* tidak memiliki baterai, seluruh daya yang dipanen harus langsung dikonsumsi. Formula penghematan tagihan bulanan adalah:

$$	ext{Penghematan (Rp/Bulan)} = 	ext{Produksi Energi Bulanan (kWh)} 	imes 	ext{Tarif Dasar Listrik PLN (Rp/kWh)}$$

Mari kita simulasikan untuk rumah tangga golongan tarif R-2 (Daya 3.500 VA hingga 5.500 VA) dengan tarif Rp 1.699,53 per kWh:
* Kapasitas Terpasang: **5 kWp (5.000 Wp)**
* Rata-rata Radiasi Tropis Harian: 3,8 jam PSH
* Produksi Harian = $5\,	ext{kWp} 	imes 3,8\,	ext{PSH} 	imes 0,82\,(	ext{Performance Ratio}) = 15,58\,	ext{kWh/hari}$
* Produksi Bulanan = $15,58 	imes 30\,	ext{hari} = 467,4\,	ext{kWh/bulan}$
* **Nilai Penghematan Bulanan:** $467,4\,	ext{kWh} 	imes 	ext{Rp } 1.699,53 = 	extbf{Rp 794.360 per bulan}$ (atau sekitar **Rp 9,53 juta per tahun**).

```
Investasi Sistem 5 kWp: Rp 47.500.000
Penghematan Tahunan:    Rp 9.530.000
Payback Period (BEP):  Rp 47.500.000 / Rp 9.530.000 ≈ 4,9 Tahun
```
Dengan masa garansi performa modul surya mencapai **25 tahun**, maka setelah periode balik modal 5 tahun terlewati, pemilik rumah menikmati listrik tenaga surya gratis murni selama 20 tahun berikutnya.

---

## Tabel Spesifikasi Teknis Komponen Sistem On Grid

| Komponen Sistem | Spesifikasi Standar Industri Tier-1 | Fungsi Rekayasa |
| :--- | :--- | :--- |
| **Modul Surya Fotovoltaik** | Monocrystalline TOPCon / N-Type 550 – 600 Wp | Efisiensi sel > 22,5%, degradasi tahunan < 0,4%, sertifikasi IEC 61215 |
| **Grid-Tie Inverter** | String Inverter On-Grid Pure Sine Wave | Efisiensi MPPT > 99,5%, THD < 3%, IP65/IP66 outdoor rating |
| **Zero Export Controller** | Smart Energy Meter + Split-Core CT | Membatasi daya keluar ke trafo PLN agar tidak melanggar kuota |
| **DC Protection Box** | Surge Arrester DC 1000V + Fuse DC 15A + Isolator | Melindungi modul dan inverter dari sambaran petir induksi |
| **AC Protection Box** | RCBO 30mA + Surge Arrester AC 275V + MCB Chint/ABB | Memutus arus bocor dan lonjakan tegangan transien jaringan |
| **Sistem Braket Mounting** | Profil Aluminium Anodized AL6005-T5 + SUS304 | Tahan korosi air hujan asam dan beban angin hingga 130 km/jam |

Kunjungi artikel komprehensif kami mengenai [komponen PLTS](https://solarium.id/wp/komponen-plts/) dan [inverter PLTS](https://solarium.id/wp/inverter-plts/) untuk memperdalam detail pemilihan perangkat.

---

## Tanya Jawab Seputar PLTS On Grid (FAQ)

1. **Apakah listrik di rumah tetap menyala saat terjadi pemadaman PLN?**
   Tidak menyala. Pada sistem PLTS on grid standar, inverter akan mati secara otomatis (*anti-islanding*) saat aliran PLN padam demi alasan keselamatan ketenagalistrikan. Jika Anda membutuhkan listrik cadangan otomatis saat pemadaman PLN terjadi, solusinya adalah memasang sistem [PLTS hybrid](https://solarium.id/wp/plts-hybrid/) yang dilengkapi baterai *back-up*.

2. **Bagaimana jika cuaca hujan lebat atau mendung seharian?**
   Panel surya tetap memproduksi listrik dari radiasi difus matahari meskipun intensitasnya turun menjadi 15% hingga 25% dari kapasitas optimal. Seluruh sisa kekurangan daya yang dibutuhkan rumah akan ditarik secara otomatis dari jaringan PLN tanpa gangguan interupsi daya.

3. **Berapa lama proses pengurusan izin PLTS atap ke PLN?**
   Proses pengajuan persetujuan kuota dan izin paralel ke unit PLN Distribusi setempat biasanya memakan waktu antara **14 hingga 30 hari kerja**, mencakup verifikasi berkas teknis, uji komisioning bersama teknisi PLN, dan penerbitan Sertifikat Laik Operasi (SLO). Seluruh prosedur ini diurus tuntas oleh tim perizinan [Solarium](https://solarium.id/wp/).

4. **Apakah sistem on grid bisa dipasang di instalasi listrik 1-fase dan 3-fase?**
   Sangat bisa. Inverter on-grid tersedia untuk sistem listrik 1-fase (kapasitas 1 kW hingga 6 kW untuk rumah daya 1.300 VA hingga 6.600 VA) maupun sistem 3-fase (kapasitas 5 kW hingga 100 kW+ untuk rumah mewah daya di atas 10.600 VA, ruko, gedung perkantoran, dan pabrik).

---

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "PLTS On Grid: Cara Kerja, Skema PLN & Biaya 2026",
  "description": "Panduan komprehensif sistem PLTS on grid di Indonesia: cara kerja grid-tie inverter, regulasi kuota PLN Permen ESDM No 2/2024, zero-export, dan kalkulasi ROI.",
  "author": {
    "@type": "Organization",
    "name": "Solarium",
    "url": "https://solarium.id/wp/"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Solarium",
    "logo": {
      "@type": "ImageObject",
      "url": "https://solarium.id/wp/wp-content/uploads/logo.png"
    }
  },
  "mainEntityOfPage": "https://solarium.id/wp/plts-on-grid/"
}
```