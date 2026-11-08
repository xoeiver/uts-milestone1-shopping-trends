# UTS Milestone 1 — Prediksi Subscription Status pada Customer Shopping Trends

| | |
|---|---|
| **Project ID** | A18 |
| **Nama Kelompok** | Perilaku Konsumen |
| **Mata Kuliah** | Pembelajaran Mesin |

## Anggota
| Nama | NIM | Kontribusi |
|---|---|---|
| Cindy Nathania (Ketua) | 231111567 | Data, EDA, preprocessing |
| Gloria Apriyanti Siagian | 231111304 | Feature engineering, model, evaluasi |
| Thresya Tupa Revalika Gultom | 231112901 | Hasil, dokumentasi, integrasi |

## Deskripsi Masalah
Memprediksi apakah seorang pelanggan berlangganan (`Subscription Status` = Yes/No) berdasarkan profil dan perilaku belanjanya. Pendekatan: klasifikasi biner dengan classical machine learning. Karena kelas tidak seimbang, metrik utama adalah PR-AUC (average precision), didukung ROC-AUC, F1, dan balanced accuracy. Pada Milestone 1 dibangun dua baseline (Dummy) dan empat model kandidat (Logistic Regression, Decision Tree, Random Forest, HistGradientBoosting).

## Dataset
Lihat [`DATASET.md`](DATASET.md). Sumber: https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset

## Struktur Repository
```
├── README.md
├── DATASET.md                              # dokumentasi sumber dataset
├── requirements.txt
├── UTS_Milestone1_Shopping_Trends.ipynb    # notebook eksperimen (sudah ber-output)
├── Laporan_UTS_Milestone1.pdf              # laporan
├── data/                                   # CSV (lihat DATASET.md)
├── results/                                # tabel hasil eksperimen
│   ├── cv_results.csv
│   ├── holdout_results.csv
│   └── eda_rate_per_kategori.csv
└── figures/                                # gambar EDA dan confusion matrix
```

## Petunjuk Penggunaan
1. Clone/unduh repo ini.
2. `pip install -r requirements.txt`
3. Letakkan CSV dataset di folder `data/` (cara memperolehnya di `DATASET.md`).
4. Jalankan `UTS_Milestone1_Shopping_Trends.ipynb` dengan **Run All** (seed = 42). Bisa juga di Google Colab: upload notebook, buat folder `data/`, upload CSV, lalu Runtime → Run all.
5. Tabel hasil akan muncul di `results/` dan gambar di `figures/`.

## Hasil Eksperimen Awal
Lihat `results/cv_results.csv` dan `results/holdout_results.csv`, serta bagian H pada laporan.
