# UTS Graf Sains Data — Analisis RetailRocket dengan Neo4j Naufal Muzaki (24031554061)

Repository ini berisi pengerjaan Ujian Tengah Semester (UTS) Naufal Muzaki NIM 24031554061 mata kuliah **Graf Sains Data** menggunakan dataset **RetailRocket**. Analisis dilakukan dengan Python/Jupyter Notebook dan Neo4j untuk mengolah aktivitas pengunjung terhadap barang, membentuk graf interaksi, serta mengeksplorasi kemiripan pengguna dan rekomendasi barang.

## Tujuan

- Memahami struktur dan karakteristik dataset RetailRocket.
- Mengolah data aktivitas untuk periode P1 dan P2 sesuai ketentuan tugas.
- Membentuk simpul pengunjung (*visitor*), simpul barang (*item*), dan relasi interaksi di Neo4j.
- Menjalankan query Cypher untuk memeriksa simpul dan relasi pada graf.
- Membentuk *User Vector Space Model* (User VSM) dan *Item Vector Space Model* (Item VSM).
- Mengeksplorasi kemiripan antar pengguna dan pendekatan rekomendasi barang.

## Dataset

Dataset utama yang digunakan adalah RetailRocket events.csv, yang berisi catatan aktivitas pengunjung terhadap barang di situs e-commerce. Jenis aktivitas pada dataset antara lain view, addtocart, dan transaction.

## Sumber Dataset
Dataset diperoleh dari Kaggle pada halaman Retailrocket recommender system dataset:
- Sumber: Roman Zykov, Retailrocket recommender system dataset.
- Tautan: https://www.kaggle.com/retailrocket/ecommerce-dataset
- File yang digunakan dalam proyek ini: events.csv.
- Keterangan: Dataset berisi catatan interaksi pengunjung dengan barang. Untuk pengerjaan ini, data aktivitas digunakan sebagai dasar pemfilteran periode P1 dan P2.
Harap merujuk ke halaman sumber Kaggle untuk informasi dataset, ketentuan penggunaan, dan lisensi yang menyertainya. Jika dataset tidak disertakan dalam repository, unduh dari sumber tersebut dan letakkan events.csv di folder data/.

| Kolom | Keterangan |
|---|---|
| `timestamp` | Waktu terjadinya aktivitas |
| `visitorid` | Identitas pengunjung |
| `event` | Jenis aktivitas, misalnya `view`, `addtocart`, atau `transaction` |
| `itemid` | Identitas barang |
| `transactionid` | Identitas transaksi, jika tersedia |

File dataset diletakkan pada folder `data/`. File dataset berukuran besar dapat tidak disertakan dalam repository apabila tidak diperlukan untuk pengumpulan atau jika ketentuan distribusinya membatasi pengunggahan. Jika file tidak tersedia di repository, siapkan dataset secara lokal dan sesuaikan lokasi file pada notebook.

## Struktur Repository

```text
UTS-Graf-Sains-Data-061/
├── README.md
├── UTS-GSD-061.ipynb        # notebook pengerjaan
├── data/
│   └── events.csv           # data aktivitas/event RetailRocket
├── output/
│   ├── P1                   # hasil pengolahan periode P1
│   └── P2                   # hasil pengolahan periode P2
└── Laporan_UTS_GSD_061.pdf 
```

**Keterangan folder dan file:**

- `README.md`: dokumentasi proyek dan petunjuk penggunaan repository.
- `UTS-GSD-061.ipynb`: notebook berisi kode Python, pengolahan data, analisis, serta proses yang terkait dengan Neo4j. Sesuaikan nama ini jika nama notebook yang diunggah berbeda.
- `data/`: menyimpan dataset aktivitas RetailRocket, yaitu `events.csv`.
- `output/P1`: hasil pengolahan data untuk periode P1.
- `output/P2`: hasil pengolahan data untuk periode P2. Keduanya bisa berupa file atau folder sesuai bentuk output yang dihasilkan notebook.
- `Laporan_UTS_GSD_061.pdf`: laporan tertulis

Pada struktur di atas, `P1` dan `P2` mewakili hasil pengolahan masing-masing periode. Pertahankan nama dan ekstensi file atau folder sesuai yang benar-benar ada di repository.

## Periode Pengamatan

Pengerjaan ini membagi data aktivitas ke dalam dua periode:

- **P1:** periode pengamatan 2–8 Juni 2015.
- **P2:** periode pengamatan 8–14 Agustus 2015.

Gunakan batas waktu dan hasil filter yang sama dengan yang diterapkan di notebook dan dijelaskan dalam laporan.

## Teknologi yang Digunakan

- **Python** untuk pengolahan dan analisis data.
- **Jupyter Notebook** untuk menjalankan serta mendokumentasikan kode.
- **Pandas dan NumPy** untuk pengolahan data.
- **Scikit-learn** untuk pembentukan matriks fitur dan pengukuran kemiripan.
- **NetworkX** untuk eksplorasi graf.
- **Neo4j dan Cypher** untuk pemodelan serta kueri graf.
- **Neo4j Python Driver** untuk menghubungkan Python dengan Neo4j.

## Alur Pengerjaan

1. Memuat dan memeriksa dataset RetailRocket.
2. Mengeksplorasi isi data, termasuk kolom serta jenis aktivitas (*event*).
3. Memfilter data ke dalam periode P1 dan P2, kemudian menyimpan hasilnya di folder `output/`.
4. Membentuk simpul pengunjung dan barang serta relasi interaksi pada Neo4j.
5. Menjalankan query Cypher untuk memeriksa struktur graf.
6. Membentuk User VSM dan Item VSM berdasarkan interaksi yang dianalisis.
7. Mengeksplorasi graf sampel dan menghitung kemiripan antar pengguna.
8. Menguji pendekatan rekomendasi serta mengevaluasi hasil yang diperoleh.

Hasil dan angka analisis yang menjadi acuan adalah hasil aktual dari notebook serta laporan UTS.

## Cara Menjalankan

1. Siapkan Python dan Jupyter Notebook/JupyterLab.
2. Letakkan dataset `events.csv` pada folder `data/`, lalu sesuaikan jalur file pada notebook apabila berbeda.
3. Instal library Python yang diperlukan berdasarkan impor pada notebook.
4. Jalankan Neo4j dan sesuaikan URI, nama database, serta konfigurasi koneksi pada notebook.
5. Jalankan sel notebook secara berurutan.
6. Periksa hasil pengolahan P1 dan P2 yang disimpan di folder `output/`.

## Keamanan

Jangan mengunggah kata sandi Neo4j, token, atau kredensial pribadi ke GitHub. Simpan kredensial di konfigurasi lokal atau variabel lingkungan yang tidak diunggah ke repository.

## Catatan

Repository ini digunakan untuk dokumentasi dan pengumpulan tugas UTS Graf Sains Data. Notebook, output P1 dan P2, serta laporan.