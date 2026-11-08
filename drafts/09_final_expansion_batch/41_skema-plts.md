---
Focus Keyword: skema plts
SEO Title (≤50 char): Skema Rangkaian PLTS: Diagram On, Off & Hybrid
Meta Description (≤140 char): Pelajari skema rangkaian PLTS lengkap: diagram pengkabelan seri-paralel panel surya, inverter, solar charge controller, & MCB proteksi DC/AC.
URL Slug: skema-plts
Kategori: Sistem PLTS (ID 4)
Status: Draft
---

# Skema Rangkaian PLTS: Diagram Pengkabelan Kelistrikan, Dimensi Proteksi DC/AC, dan Standar SNI/IEC

Skema PLTS (*single line diagram and solar photovoltaic wiring schematic*) adalah cetak biru teknis ketenagalistrikan yang menggambarkan konfigurasi pengkabelan terintegrasi, kalkulasi interkoneksi seri-paralel modul surya, dimensi pemutus sirkuit (*circuit breaker*), koordinasi relai proteksi, sistem penangkal petir transien (*surge protection device* / SPD), dan tata letak pembumian (*grounding network*) yang memenuhi standar keteknikan nasional [Badan Standardisasi Nasional (BSN / SNI)](https://bsn.go.id/) IEC 62548 dan regulasi keselamatan [PT PLN (Persero)](https://web.pln.co.id/).

Memahami skema PLTS yang benar merupakan syarat mutlak untuk mencegah timbulnya bahaya kebakaran akibat busur api arus searah (*DC arc fault*), sengatan listrik bertegangan tinggi hingga 1.000V DC, serta memastikan efisiensi transfer energi maksimal tanpa terjadinya rugi-rugi jatuh tegangan (*voltage drop*) kabel yang melampaui toleransi rekayasa 1,5% hingga 2%. Rancang bangun kelistrikan yang keliru pada sisi DC tidak hanya membatalkan garansi pabrikan inverter, tetapi juga menggagalkan proses uji kelayakan penerbitan Sertifikat Laik Operasi (SLO) dari inspektur ketenagalistrikan.

---

## Anatomi Diagram Kelistrikan Tunggal (*Single Line Diagram* / SLD)

Diagram kelistrikan sistem fotovoltaik profesional terdiri atas dua zona kelistrikan utama yang dipisahkan oleh tahap konversi daya:

```
[ ZONA TEGANGAN TINGGI DC ]
Rangkaian Modul Surya (String Fotovoltaik)
       │ (Kabel Solar PV1-F 4mm² / 6mm² Bertanda UV Resistant)
       ▼
[DC Combiner & Protection Box]
├── DC Fuse Pelindung Arus Lebih (gPV 1000V 15A/20A)
├── DC Isolator Switch / Disconnector (Rotary Switch 1000V)
└── DC Surge Arrester Tipe 2 (SPD DC 1000V / 40kA)
       │
       ▼
[INVERTER SURYA (On-Grid / Hybrid / Off-Grid)]
       │
       ▼
[ ZONA TEGANGAN RENDAH AC ]
[AC Combiner & Distribution Box]
├── AC Surge Protection Device (SPD AC 275V / 40kA)
├── Residual Current Circuit Breaker with Overcurrent (RCBO 30mA Tipe A)
├── Molded Case Circuit Breaker / MCB AC
└── Smart Meter Bi-Directional & Sensor Arus CT
       │
       ▼
Panel Distribusi Beban Properti (DB) & Meteran PLN
```

### 1. Zona Sisi DC (*Direct Current Side*)
Arus DC yang mengalir dari modul fotovoltaik tidak memiliki titik nol alami (*zero-crossing point*) seperti arus AC. Oleh karena itu, percikan busur api DC jauh lebih sulit padam secara alami. Rangkaian proteksi DC wajib menggunakan komponen yang tersertifikasi khusus PV:
* **Sekring DC (*gPV Fuse*):** Memutus arus balik (*reverse current*) bila salah satu string mengalami hubungan pendek (*short circuit*).
* **Sakelar Isolasi DC (*DC Disconnector*):** Mampu memutus arus beban penuh secara manual saat teknisi melakukan perawatan berkala.
* **Arester DC (*DC SPD*):** Membuang lonjakan voltase transien akibat induksi petir langsung ke batang elektroda pembumian tanah.

### 2. Zona Sisi AC (*Alternating Current Side*)
Setelah arus dikonversi oleh inverter menjadi AC 220V/380V berfrekuensi 50 Hz, daya dialirkan melalui kotak distribusi AC yang dilengkapi:
* **RCBO (*Residual Current Circuit Breaker with Overcurrent*):** Mendeteksi kebocoran arus ke bumi di atas 30 mA untuk melindungi penghuni rumah dari sengatan listrik mematikan.
* **MCB AC:** Membatasi arus kerja agar tidak melebihi kapasitas kabel penghantar menuju busbar panel utama.

---

## Rangkaian Seri vs Paralel Panel Surya: Rekayasa Tegangan dan Arus

Konfigurasi string pada skema PLTS menentukan apakah tegangan atau arus yang dilipatgandakan untuk mencocokkan rentang kerja MPPT inverter (*MPPT Operating Voltage Range*):

```
Rangkaian SERI:    Tegangan BERTAMBAH (V_total = V1 + V2 + ... + Vn), Arus TETAP (I_total = I1)
Rangkaian PARALEL: Tegangan TETAP (V_total = V1), Arus BERTAMBAH (I_total = I1 + I2 + ... + In)
```

| Parameter Rangkaian | Skema Hubungan Seri | Skema Hubungan Paralel |
| :--- | :--- | :--- |
| **Karakteristik Tegangan** | Meningkat secara linier ($V_{total} = \Sigma V_{mp}$) | Sama dengan tegangan satu panel ($V_{total} = V_{mp}$) |
| **Karakteristik Arus** | Sama dengan arus satu panel ($I_{total} = I_{mp}$) | Meningkat secara linier ($I_{total} = \Sigma I_{mp}$) |
| **Ukuran Diameter Kabel** | Cukup kabel solar standar $4\,	ext{mm}^2$ | Membutuhkan kabel tebal ($16\,	ext{mm}^2 - 35\,	ext{mm}^2$) |
| **Dampak Rugi Daya Kabel ($I^2R$)** | Sangat Rendah (Arus kecil, voltase tinggi) | Sangat Tinggi bila jarak kabel panjang |
| **Toleransi Bayangan (*Shading*)** | 1 sel tertutup bayangan melemahkan 1 string | Hanya panel yang terkena bayangan yang turun |
| **Kompatibilitas Inverter** | Standar inverter modern (150V – 600V DC) | Hanya untuk MPPT voltase rendah (12V – 48V) |

### Contoh Rekayasa Konfigurasi String:
Misalkan Anda menggunakan 10 unit panel surya 550 Wp dengan parameter elektrik:
* Tegangan Daya Maksimal ($V_{mp}$): $42,0\,	ext{Volt}$
* Tegangan Sirkuit Terbuka ($V_{oc}$): $50,0\,	ext{Volt}$
* Arus Daya Maksimal ($I_{mp}$): $13,1\,	ext{Ampere}$

Bila dirangkai **10 modul Seri Penuh (1 String × 10 Modul)**:
* $V_{mp\_total} = 10 	imes 42,0\,	ext{V} = \mathbf{420\,	ext{Volt}}$ (Sangat ideal untuk inverter on-grid dengan rentang MPPT 120V–550V).
* $V_{oc\_max} = 10 	imes 50,0\,	ext{V} = 500\,	ext{Volt}$ (Aman di bawah tegangan maksimum inverter 600V DC).
* $I_{mp\_total} = \mathbf{13,1\,	ext{Ampere}}$ (Aman di bawah batas arus input inverter 16A).

---

## Standar Pembumian (*Earthing Network*) dan Manajemen Kabel

Berdasarkan regulasi teknis SNI 0225:2020 (PUIL 2020), sistem keselamatan skema PLTS wajib mematuhi kaidah pembumian berikut:

1. **Pemisahan Jalur Grounding:** Rangkaian penangkal petir eksternal gedung (*lightning rod* / konvensional / elektrostatis) **tidak boleh disatukan secara langsung** dengan pembumian frame panel surya dan pembumian kelistrikan inverter. Keduanya harus memiliki elektroda pentanahan terpisah dengan jarak antar elektroda minimal 5 meter untuk mencegah arus balik sambaran petir menghancurkan perangkat elektronik inverter.
2. **Nilai Tahanan Pembumian ($R_g \le 5\,\Omega$):** Seluruh rangka aluminium panel surya, rak *mounting*, kotak panel combinator logam, dan sasis inverter harus dibumikan ke tanah dengan nilai tahanan resistansi pembumian maksimal **di bawah 5 Ohm** (direkomendasikan < 2 Ohm pada instalasi komersial).
3. **Kabel Khusus Solar PV1-F / H1Z2Z2-K:** Kabel dari panel surya menuju panel proteksi wajib bertipe tembaga berlapis timah (*tinned copper*) dengan insulasi ganda (*double insulated*) tahan sinar ultraviolet dan tahan suhu tinggi hingga 120°C. Jangan pernah menggunakan kabel instalasi rumah biasa (seperti NYM atau NYA) di atap terbuka karena lapisan PVC akan getas dan pecah akibat cuaca tropis dalam waktu kurang dari 2 tahun.

---

## Tanya Jawab Seputar Skema Rangkaian PLTS (FAQ)

1. **Mengapa MCB AC biasa tidak boleh dipakai untuk memutus sirkuit DC panel surya?**
   Karena MCB AC dirancang untuk memadamkan busur api pada titik nol gelombang sinus bolak-balik ($50\,	ext{Hz}$). Pada sirkuit DC, arus mengalir konstan tanpa titik nol, sehingga celah kontak MCB AC tidak mampu memadamkan busur api listrik. Menggunakan MCB AC pada sirkuit DC panel surya berisiko tinggi menyebabkan kontak internal meleleh terbakar.

2. **Berapa batas maksimal penurunan tegangan (*voltage drop*) kabel yang diizinkan?**
   Sesuai standar teknik IEC 62548, penurunan tegangan antara modul terjauh hingga terminal input inverter tidak boleh melampaui **1,5% hingga 2%** dari tegangan nominal sirkuit. Kerugian jatuh tegangan di atas 3% akan menghasilkan panas berlebih pada kabel dan mengurangi efisiensi produksi energi tahunan secara signifikan.

3. **Kapan kita harus merangkai panel surya dalam konfigurasi kombinasi seri-paralel?**
   Kombinasi seri-paralel digunakan apabila jumlah total panel surya menghasilkan tegangan total sirkuit terbuka ($V_{oc}$) yang melampaui ambang batas maksimum inverter (misalnya > 600V atau > 1000V DC), atau ketika menggunakan kontroler pengisian daya baterai off-grid 48V yang memiliki batas voltase input menengah (misal: 150V DC).

4. **Bagaimana memastikan skema PLTS saya lolos uji Sertifikat Laik Operasi (SLO)?**
   Pastikan skema dirancang oleh insinyur ketenagalistrikan bersertifikat, memiliki kelengkapan gambar as-built, tata letak kabel tertata rapi di dalam konduit tahan api (*corrugated PVC / metal conduit*), nilai resistansi pembumian terukur di bawah 5 Ohm, serta dilengkapi label peringatan bahaya tegangan tinggi DC (*hazard labeling*) di setiap kotak junction. Tim instalatur [Solarium](https://solarium.id/wp/) yang memegang lisensi [legalitas dan sertifikasi BNSP](https://solarium.id/wp/legalitas-sertifikasi/) memastikan seluruh standar ini terpenuhi 100%.

---

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Skema Rangkaian PLTS: Diagram On, Off & Hybrid",
  "description": "Panduan teknis skema rangkaian PLTS: single line diagram (SLD), konfigurasi seri-paralel, dimensi proteksi DC/AC fuse, SPD, dan standar grounding SNI/IEC.",
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
  "mainEntityOfPage": "https://solarium.id/wp/skema-plts/"
}
```