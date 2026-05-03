# Analisis Customer Churn dengan Random Forest, XGBoost, dan KNN

Proyek ini adalah studi kasus Machine Learning untuk memprediksi probabilitas pelanggan berhenti berlangganan (Churn) menggunakan tiga algoritma klasifikasi: **Random Forest**, **XGBoost**, dan **K-Nearest Neighbors (KNN)**.

Proyek ini dibuat menggunakan **Jupyter Notebook**, yang memungkinkan kode, dokumentasi, dan hasil visualisasi (grafik) ditampilkan dalam satu tempat yang interaktif.

---

## Cara Menjalankan Proyek (Langkah demi Langkah)

Ikuti panduan di bawah ini untuk menjalankan proyek dengan aman di komputer Anda tanpa mengacaukan konfigurasi sistem (menggunakan Virtual Environment).

### 1. Persiapan Awal
Pastikan Anda sudah menginstal **Python 3** di komputer Anda. Buka terminal (atau Command Prompt) dan arahkan ke folder proyek ini:
```bash
cd path/ke/folder/tugas_random_forest_XGBoost
```

### 2. Buat dan Aktifkan Virtual Environment
Virtual Environment berfungsi sebagai "ruang isolasi" agar instalasi library proyek ini tidak bertabrakan dengan proyek Anda yang lain.

*   **Pengguna Linux / macOS:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
*   **Pengguna Windows:**
    ```cmd
    python -m venv venv
    venv\Scripts\activate
    ```
*(Jika berhasil, Anda akan melihat tulisan `(venv)` di awal baris terminal Anda).*

### 3. Instalasi Library yang Dibutuhkan
Instal semua library (seperti Pandas, Scikit-Learn, XGBoost, dan Jupyter) secara otomatis melalui file `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 4. Buka Jupyter Notebook
Setelah proses instalasi selesai, jalankan perintah berikut di terminal:
```bash
jupyter notebook
```
Perintah ini akan menyalakan *local server* dan otomatis membuka tab baru di web browser Anda (seperti Chrome, Firefox, atau Edge).

---

## Cara Membaca dan Mengeksekusi Kode

1. Di halaman browser yang terbuka, klik file bernama **`main.ipynb`**.
2. Anda tidak perlu melakukan konfigurasi apa pun lagi. Untuk menjalankan seluruh program dari awal hingga akhir dan melihat hasilnya, klik menu di bagian atas:
   **`Run` -> `Run All Cells`** .
### Apa yang Harus Diperhatikan?
Berbeda dengan script `.py` biasa yang outputnya hanya muncul di akhir terminal, output Jupyter Notebook akan muncul tepat di bawah blok kode yang dijalankan. Perhatikan 3 output utama berikut:
*   **Bagian 1:** Menampilkan cuplikan tabel dataset asli.
*   **Bagian 5:** Menampilkan teks evaluasi model (Skor Akurasi, Presisi, Recall).
*   **Bagian 6:** Menampilkan visualisasi grafik (Confusion Matrix) untuk membandingkan kinerja ketiga algoritma secara visual.
