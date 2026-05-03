# Struktur Presentasi PPT: Analisis Komparatif Machine Learning

## Slide 1: Judul & Anggota Tim
* **Judul:** Analisis Komparatif Supervised Learning (Random Forest, XGBoost, & KNN) untuk Prediksi *Customer Churn*.
* **Anggota Kelompok:** 
  * 1. [Nama Anda] - [NIM]
  * 2. [Nama Teman Anda] - [NIM]
  * 3. [Nama Teman Anda] - [NIM]

## Slide 2: Tujuan Program
* **Tujuan:** Membangun dan mengevaluasi model *machine learning* untuk mengidentifikasi probabilitas pelanggan berhenti berlangganan (*churn*).
* **Alur Kerja:**
  * **Prapemrosesan Data:** Penghapusan ID, penanganan nilai kosong (*missing values*), *One-Hot Encoding* untuk data kategorikal, dan *Standard Scaling* (khusus untuk KNN).
  * **Pelatihan Model:** Menggunakan Random Forest, XGBoost, dan KNN.
  * **Evaluasi:** Membandingkan akurasi dan metrik presisi antar algoritma.

## Slide 3: Landasan Teori Singkat
* **Random Forest:** Algoritma berbasis pohon (*tree-based*) yang bekerja dengan prinsip *bagging* (menggabungkan banyak pohon keputusan). Sangat stabil dalam menangani berbagai jenis data dan mencegah *overfitting*.
* **XGBoost:** Algoritma *tree-based* yang menggunakan prinsip *boosting*. Setiap pohon baru dibangun untuk mengoreksi kesalahan dari pohon sebelumnya. Sangat kuat dalam menemukan pola data yang kompleks.
* **K-Nearest Neighbors (KNN):** Algoritma berbasis jarak (*distance-based*). Mengklasifikasi data baru berdasarkan kedekatannya dengan sejumlah (K) titik data pada himpunan pelatihan. Sangat bergantung pada proses *scaling* data.

## Slide 4: Data yang Digunakan
* **Dataset:** Telco Customer Churn.
* **Dimensi Data Awal:** 7.043 baris dan 21 kolom (fitur).
* **Target Klasifikasi:** 
  * Kelas 0: Pelanggan yang tetap berlangganan.
  * Kelas 1: Pelanggan yang *churn* (berhenti).
* **Tautan Sumber Data (Kaggle/GitHub):**
  * `https://github.com/IBM/telco-customer-churn-on-icp4d/blob/master/data/Telco-Customer-Churn.csv`

## Slide 5: Hasil Prediksi Model
* **Random Forest:** Meraih tingkat **Akurasi: 77.75%**. Menunjukkan kinerja terbaik secara keseluruhan dalam menyeimbangkan presisi antara pelanggan yang bertahan dan *churn*.
* **XGBoost:** Meraih tingkat **Akurasi: 77.04%**. Kinerjanya sangat kompetitif, hanya terpaut sedikit di bawah Random Forest pada dataset spesifik ini.
* **K-Nearest Neighbors (KNN):** Meraih tingkat **Akurasi: 74.63%**. Kinerja terendah, membuktikan bahwa algoritma berbasis jarak kesulitan bersaing dengan model *tree-based* pada dataset klasifikasi tabular dengan banyak fitur kategorikal (meskipun sudah di-*scale*).

## Slide 6: Visualisasi Kinerja (*Confusion Matrix*)
* **[TEMPATKAN SCREENSHOT KETIGA GAMBAR CONFUSION MATRIX DARI JUPYTER NOTEBOOK DI SINI]**
* **Analisis Visual:**
  * **Diagonal Utama (Prediksi Benar):** Kotak hijau gelap menunjukkan prediksi yang akurat (model menebak benar pelanggan yang bertahan maupun *churn*).
  * **Sisa Area (Error):** Kotak terang (hijau muda/putih) menunjukkan tingkat kegagalan (*False Positives* dan *False Negatives*).
  * *Contoh:* Random Forest berhasil menebak 920 pelanggan yang bertahan secara presisi (tertinggi di antara ketiga model).