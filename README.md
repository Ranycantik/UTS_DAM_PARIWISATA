# UTS DATA ACQUISITION & MANAGEMENT
## Akuisisi Data Pariwisata dan Kondisi Cuaca di Indonesia

### 1. Identitas Mahasiswa
- **Nama:** Katarina Gita Candranurani
- **NIM:** 2501010369
- **Kelas:** E
- **Mata Kuliah:** Akuisisi dan Manajemen Data
- **Dosen:** Dr. I Gede Totok Suryawan, S.Kom., M.T.
- **Tanggal Ujian:** 19 November 2026

### 2. Deskripsi Proyek
Proyek ini merupakan tugas Ujian Tengah Semester (UTS) mata kuliah Akuisisi dan Manajemen Data. Proyek membahas proses pengumpulan, pemeriksaan, pengolahan, dan penggabungan data pariwisata dengan data kondisi cuaca di Indonesia.

Data utama yang digunakan adalah jumlah perjalanan wisatawan nusantara menurut provinsi tujuan yang diperoleh dari Badan Pusat Statistik (BPS). Data tersebut kemudian dikaitkan dengan data suhu dan curah hujan dari Open-Meteo Historical Weather API.

Periode data yang digunakan adalah tahun 2022–2025.

### 3. Tujuan Proyek
1. Memahami proses akuisisi data dari berbagai sumber.
2. Mengumpulkan data perjalanan wisatawan nusantara dari BPS.
3. Mengambil data cuaca melalui API Open-Meteo.
4. Melakukan web scraping tabel daftar ibu kota provinsi dari Wikipedia.
5. Melakukan pemeriksaan kualitas dan kelengkapan data.
6. Menggabungkan data perjalanan wisatawan dengan data cuaca.
7. Menerapkan prinsip etika dalam proses pengumpulan data.

### 4. Wilayah Penelitian
Penelitian menggunakan lima provinsi tujuan:
- Bali
- DI Yogyakarta
- Jawa Barat
- Sumatera Utara
- Sulawesi Selatan

Data cuaca diambil berdasarkan koordinat ibu kota masing-masing provinsi.

### 5. Sumber dan Metode Akuisisi Data

| Metode | Sumber Data | Jenis Data |
|---|---|---|
| Dataset | Badan Pusat Statistik (BPS) | XLSX |
| API | Open-Meteo Historical Weather API | JSON |
| Web Scraping | Wikipedia Indonesia | HTML dan tabel |

**Sumber data:**
- BPS: https://www.bps.go.id/
- Open-Meteo: https://open-meteo.com/
- Wikipedia: https://id.wikipedia.org/wiki/Daftar_ibu_kota_provinsi_di_Indonesia

### 6. Struktur Repository

```text
UTS_DAM_PARIWISATA/
│
├── data/
│   ├── raw/
│   │   └── Data mentah dari BPS, Open-Meteo,
│   │       dan Wikipedia
│   │
│   └── processed/
│       └── Data hasil pengolahan
│
├── docs/
│   ├── bukti/
│   │   └── Bukti lisensi dan robots.txt
│   │
│   ├── provenance.csv
│   └── data_ethics_checklist.md
│
├── notebook/
│   └── Uts_Akuisisi_(2)_(1)(1).ipynb
│
└── README.md
```

### 7. Tahapan Pengerjaan

**Soal 1 – Akuisisi Dataset BPS**
- Membaca berkas XLSX BPS tahun 2022–2025.
- Mengidentifikasi jenis, jumlah, dan struktur data.
- Memeriksa nilai kosong.
- Mengestimasi kebutuhan penyimpanan data.

**Soal 2 – Lisensi dan Data Ethics**
- Memeriksa ketentuan penggunaan sumber data.
- Memeriksa keberadaan PII dan quasi-identifier.
- Membuat Data Ethics Checklist.
- Mencatat provenance setiap sumber data.

**Soal 3 – Akuisisi melalui API**
- Menggunakan Open-Meteo Historical Weather API.
- Mengambil data suhu rata-rata dan curah hujan harian.
- Mengumpulkan data periode 2022–2025.
- Menyimpan respons API dalam format JSON.

**Soal 4 – Web Scraping**
- Memeriksa robots.txt Wikipedia.
- Mengambil tabel daftar ibu kota provinsi.
- Mengolah tabel menggunakan BeautifulSoup dan Pandas.
- Menyimpan hasil scraping dalam format CSV.

**Soal 5 – Penggabungan Data**
- Mengubah data BPS dari format lebar menjadi panjang.
- Mengagregasi data cuaca harian menjadi bulanan.
- Menggabungkan kedua dataset menggunakan kolom provinsi dan periode.
- Memeriksa duplikasi dan kesesuaian jumlah baris.
- Menyimpan hasil penggabungan dan metadata.

### 8. Tools dan Library
- Python
- Jupyter Notebook
- Pandas
- Requests
- BeautifulSoup
- Matplotlib (jika diperlukan untuk pengembangan analisis)
- GitHub
- Visual Studio Code / Google Colab

### 9. Hasil Akhir Proyek

Hasil pengolahan data yang dihasilkan dalam proyek ini meliputi:

- `data/processed/tabel_scrape_wikipedia.csv`
- `data/processed/data_gabungan.csv`
- `data/processed/data_gabungan_metadata.json`
- `docs/provenance.csv`
- `docs/data_ethics_checklist.md`

Data mentah disimpan dalam folder `data/raw`, sedangkan bukti lisensi dan pemeriksaan etika disimpan dalam folder `docs`.

