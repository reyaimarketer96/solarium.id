# DNA Solarium

Diperbarui 8 November 2026. Pegangan bisnis, konten, halaman lokal, dan pengembangan kalkulator berdasarkan arahan pemilik. Dokumen ini menetapkan perilaku yang dituju; tidak menyatakan semua fitur sudah tersedia di situs.

## Janji utama

Solarium membantu pemilik rumah dan bisnis memahami tagihan listriknya, menentukan kebutuhan sistem surya, dan melihat peluang penghematan dengan investasi yang efisien. Pelanggan harus dapat mengikuti hubungan antara tagihan, energi, jumlah panel, investasi, dan penghematan tanpa memahami teknik kelistrikan terlebih dahulu.

Keunggulan harga adalah bagian inti positioning. Pemilik menegaskan paket Solarium paling murah: target penghematan sekitar Rp2 juta/bulan dapat ditawarkan dengan investasi sekitar Rp100 jutaan, sementara penawaran pembanding sekitar Rp200 juta. Ini adalah arahan positioning pemilik, bukan hasil audit seluruh pasar. Untuk perbandingan publik, simpan penawaran bertanggal yang sebanding dalam kapasitas, baterai, lingkup pemasangan, garansi, pajak, dan lokasi. Gunakan klaim terbatas pada pembanding yang benar-benar diperiksa.

Bahasa publik profesional, tenang, spesifik, dan mudah dipahami. Nilai ekonominya harus terasa kuat melalui angka dan penjelasan. Hindari janji penghematan seragam untuk semua rumah, kepastian bebas tagihan, atau perbandingan harga tanpa lingkup yang jelas.

## Story loop wajib

1. **Tagihan:** mulai dari masalah yang dikenali pelanggan: berapa biaya listrik yang keluar setiap bulan?
2. **Pertanyaan:** berapa kebutuhan energi hariannya dan bagian mana yang bisa dipasok oleh matahari?
3. **Penjelasan:** kalkulator mengubah tagihan menjadi perkiraan kWh/hari, lalu kebutuhan produksi, panel, dan luas atap.
4. **Solusi:** jelaskan pilihan sistem sesuai pemakaian siang/malam dan kebutuhan backup, disertai investasi dari sumber harga yang sesuai.
5. **Bukti:** tampilkan asumsi, sumber harga, reviewer teknis, serta hasil survei atau proyek sesuai status sebenarnya.
6. **Penutup loop:** kembali ke tagihan awal: berapa energi PLN yang berpotensi tergantikan, nilai penghematannya, dan estimasi sisa tagihan?
7. **Tindakan:** ajak pelanggan membawa hasil tersebut ke konsultasi atau survei. Hasil dasar tetap dapat dibaca sebelum memberikan kontak.

Contoh arah copy: “Seberapa jauh atap Anda bisa membantu mengurangi tagihan listrik? Mulai dari tagihan bulanan. Kami bantu menerjemahkannya menjadi kebutuhan energi, perkiraan panel, dan pilihan investasi yang sesuai.”

Untuk penawaran Rp100 jutaan, tampilkan harga serta potensi hemat secara berdekatan dengan konfigurasi acuan, tanggal sumber, dan asumsi pemakaian. Teks headline tidak boleh melebihi kemampuan sistem yang dihitung.

## Kalkulator sebagai helpful content

Urutan yang terlihat oleh pengguna: **tagihan → energi per hari → target energi surya → perkiraan panel dan atap → investasi → penghematan dan sisa tagihan**. Gunakan label seperti “Rumah Anda memakai sekitar … kWh listrik per hari”, lalu terangkan kWh sebagai jumlah energi yang dipakai perangkat.

Masukan bertahap:

- Awal: tagihan bulanan atau kWh aktual pada rekening, serta golongan tarif. Utamakan kWh aktual jika tersedia.
- Penyempurnaan: kota, jumlah hari rekening, pemakaian siang/malam, kebutuhan backup, dan kondisi atap.
- Harga: referensi paket bertanggal, cakupan lokasi, pekerjaan tambahan, serta status validitas penawaran.

Kontrak hitung:

| Tahap | Perhitungan dan batas |
|---|---|
| Energi bulanan | kWh aktual rekening; jika tidak ada, komponen biaya energi ÷ tarif Rp/kWh. Total tagihan yang masih memuat pajak/admin hanya menghasilkan perkiraan |
| Energi harian | kWh bulanan ÷ jumlah hari rekening |
| Target energi surya | Bagian konsumsi yang hendak digantikan. Periksa waktu penggunaan dan rugi sistem; seluruh konsumsi harian tidak otomatis dapat tergantikan |
| Kapasitas panel | Target produksi kWh/hari ÷ hasil energi bersih setempat dalam kWh/kWp/hari |
| Jumlah panel | Pembulatan ke atas: kapasitas kWp × 1.000 ÷ Wp modul aktual; hitung ulang kapasitas dan produksi setelah pembulatan |
| Hasil energi bersih | Gunakan data lokasi dan asumsi rugi sistem. Bila memakai PSH × performance ratio, jangan menghitung rugi yang sama dua kali |
| Inverter | Pertimbangkan beban bersamaan, fase, lonjakan awal, dan batas teknis; tidak ditentukan hanya oleh energi harian |
| Baterai | Ditentukan oleh energi yang perlu digeser/di-backup, kapasitas terpakai, efisiensi, dan batas daya. Baterai tidak menambah produksi energi |
| Atap | Dimensi modul aktual + ruang akses/jarak teknis, orientasi, bayangan, serta kelayakan struktur |
| Penghematan | Energi surya yang benar-benar menggantikan pembelian PLN × tarif energi yang dapat dihindari; batasi oleh produksi, beban terlayani, dan rugi penyimpanan |
| Investasi | Cocokkan konfigurasi dengan penawaran valid; sertakan pekerjaan di luar paket. Jangan mengekstrapolasi seluruh paket secara linear dari harga per panel |
| Balik modal | Investasi ÷ penghematan tahunan hanya sebagai simple payback; jelaskan biaya yang belum dihitung. Tampilkan hanya jika sumber harga cukup |

Nilai produksi yang melebihi kebutuhan pada waktu tertentu tidak otomatis menjadi penghematan. Jangan mengasumsikan kredit ekspor. Tarif dan ketentuan aktual harus diverifikasi saat implementasi/pembaruan.

Contoh pendidikan, **bukan tarif atau penawaran berlaku**: biaya energi Rp2 juta/bulan, tarif asumsi Rp1.700/kWh, 30 hari → sekitar 1.176 kWh/bulan atau 39,2 kWh/hari. Untuk menyamai energi itu pada hasil bersih asumsi 3,6 kWh/kWp/hari, kebutuhan awal sekitar 10,9 kWp. Dengan modul asumsi 600 Wp, pembulatan menghasilkan 19 panel atau 11,4 kWp. Ini menyamai energi rata-rata; penggantian seluruh energi PLN masih bergantung pada waktu pemakaian, baterai, cuaca, atap, dan batas sistem.

Kriteria hasil: pengguna dapat melihat angka sebelum/sesudah, memahami asal perkiraan panel, membedakan energi harian dari daya alat, serta memahami alasan survei dapat mengubah desain. Jangan memakai persentase hemat tetap atau payback yang ditanam sebagai hasil hitung.

## Acuan harga publik dan verifikasi

Positioning investasi sekitar Rp100 jutaan merupakan arahan pemilik. Dokumen penawaran, identitas pelanggan, rincian pemasok dan data internal disimpan di luar repo publik. Validasi konfigurasi, tanggal berlaku, biaya lokasi dan potensi penghematan sebelum publikasi. Klaim pembanding Rp200 juta memerlukan penawaran setara dan bertanggal. Jangan mengarang data yang tidak tersedia.

## Penerapan lokal dan E-E-A-T

Setiap halaman daerah menjalankan story loop yang sama dengan data berbeda: profil pemakaian, produksi lokasi, kondisi atap, biaya mobilisasi, jangkauan survei/perawatan, dan bukti setempat. Kota bisa mengisi kalkulator secara otomatis; pengguna tetap dapat mengubah asumsi. Penawaran dibuat berdasarkan daerah yang benar-benar dapat dilayani.

Bedakan simulasi, hasil survei, penawaran, proyek selesai, dan produksi terukur. Gunakan proyek mitra dengan atribusi yang jelas. Kredensial milik pihak lain tidak otomatis menjadi kredensial Solarium. Foto AI berlabel ilustrasi tidak menjadi bukti pengalaman.

Utamakan wilayah dengan permintaan, kemampuan operasional, dan bukti yang memadai. Jika pergantian nama kota tidak mengubah analisis, harga layanan, atau bukti, perkaya atau gabungkan halamannya. Ukur klik nonbrand lokal, konsultasi berkualitas, survei, dan penjualan; terbitnya halaman bukan bukti menang.

## Pemakaian dan pemeliharaan

- Baca DNA ini sebelum mengubah homepage, kalkulator, penawaran, artikel biaya, atau halaman daerah.
- [DESIGN.md](DESIGN.md) tetap mengatur arah visual dan masih berstatus draf; persetujuan DNA bisnis tidak menyetujui desain secara otomatis.
- [Konteks SEO](00_konteks_geodipo/KONTEKS_SOLARIUM.md) dan peta keyword tetap menjadi acuan arsitektur.
- [Blueprint kalkulator lama](BLUEPRINT_KALKULATOR_FARMING_DATA.md) bersifat historis bila bertentangan dengan kontrak hitung ini.
- Update sumber harga saat ada revisi Pak Yudi; update bukti pembanding saat membuat perbandingan publik. Verifikasi tarif, yield, spesifikasi, dan lingkup pekerjaan sebelum implementasi.
- Status pekerjaan ini: DNA dan kontrak produk tersimpan; perubahan kode kalkulator dan publikasi situs belum dilakukan.

