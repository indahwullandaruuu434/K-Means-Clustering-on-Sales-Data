# Klasterisasi K-Means pada Data Penjualan

Proyek ini mendemonstrasikan penerapan **K-Means clustering** pada dataset penjualan (**sales.csv**) untuk menemukan pola dan mengelompokkan data yang serupa.

## **Ringkasan Dataset**
Dataset ini berisi data terkait penjualan dengan 811 baris dan 107 kolom. Rincian utama meliputi:

- **Product_Code**: Identifier untuk setiap produk.
- **W0, W1, ..., W8**: Atribut numerik terkait penjualan.
- **Fitur yang Dinormalisasi**: Data yang telah diproses untuk analisis.
- **Kolom Numerik**: Hanya kolom numerik yang digunakan untuk klasterisasi.

Nilai yang hilang atau tidak valid ditangani dengan menghapus baris yang mengandung data tersebut.

---

## **Langkah-Langkah Analisis**

### **1. Pra-pemrosesan Data**
- Memilih hanya kolom numerik untuk klasterisasi.
- Menangani nilai yang hilang atau tidak valid.
- Menormalisasi data menggunakan **StandardScaler** agar memiliki skala yang seragam.

### **2. Penentuan Jumlah Klaster Optimal**
Metode **Elbow** digunakan untuk menentukan jumlah klaster (‘k’) yang optimal. Metode ini melibatkan plotting inertia (jumlah kuadrat dalam klaster) untuk berbagai nilai ‘k’ dan memilih titik di mana penurunan inertia mulai melambat ("siku" grafik).

### **3. Klasterisasi dengan K-Means**
- Menerapkan algoritma **K-Means** dengan jumlah ‘k’ yang telah ditentukan.
- Menentukan setiap data ke klaster masing-masing.
- Menambahkan label klaster ke dataset untuk analisis lebih lanjut.

### **4. Visualisasi**
- Scatter plot digunakan untuk memvisualisasikan klaster berdasarkan dua fitur pertama dalam dataset.
- Setiap klaster direpresentasikan dengan warna yang berbeda.

---

## **Teknologi yang Digunakan**

- **Python**: Bahasa pemrograman untuk analisis data dan klasterisasi.
- **Pandas**: Manipulasi dan pembersihan data.
- **Scikit-learn**: Implementasi K-Means dan normalisasi.
- **Matplotlib/Seaborn**: Visualisasi hasil.

---

## **Cara Menjalankan Proyek**

1. Klon repositori:
   ```bash
   git clone <repository-url>
   ```
2. Masuk ke direktori proyek:
   ```bash
   cd kmeans-clustering-sales
   ```
3. Instal pustaka yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
4. Letakkan dataset **sales.csv** di direktori proyek.
5. Jalankan Jupyter Notebook atau skrip Python:
   ```bash
   jupyter notebook
   ```
   ATAU
   ```bash
   python kmeans_clustering.py
   ```

---

## **Hasil**
- Dataset berhasil dikelompokkan menjadi beberapa grup.
- Metode Elbow mengidentifikasi jumlah klaster optimal sebagai **k = 3** (atau sesuai hasil analisis).
- Visualisasi dengan jelas menunjukkan klaster yang berbeda, membantu memahami pola penjualan.
