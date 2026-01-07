# Klasifikasi Penyakit Pada Pohon Pisang Menggunakan Algoritma CNN

Proyek ini adalah implementasi *Deep Learning* menggunakan metode **Convolutional Neural Network (CNN)** untuk mendeteksi dan mengklasifikasikan jenis penyakit pada daun pohon pisang secara otomatis. [cite_start]Proyek ini bertujuan untuk meminimalkan kerugian ekonomi petani akibat kesalahan diagnosis manual[cite: 1, 46].

## 👥 Anggota Kelompok
[cite_start]Proyek ini disusun oleh mahasiswa Program Studi S1 Teknik Informatika, Universitas Telkom[cite: 4, 10]:
* [cite_start]**Arjun Ahmad Santoso** (2311102211) [cite: 6]
* [cite_start]**Buswiryawan Raditya Boenyamin** (2311102090) [cite: 7]
* [cite_start]**Willyan Hyuga Pratama** (2211102129) [cite: 8]

## 🎯 Tujuan
1.  [cite_start]**Ekstraksi Fitur Otomatis:** Menerapkan arsitektur CNN untuk mempelajari pola visual (tekstur, warna, bercak) pada daun pisang[cite: 49].
2.  [cite_start]**Klasifikasi Multi-Kelas:** Mengidentifikasi 7 kondisi daun berbeda, termasuk membedakan penyakit dengan gejala mirip seperti Black Sigatoka dan Yellow Sigatoka[cite: 50].
3.  [cite_start]**Evaluasi Kinerja:** Mengukur efektivitas model berdasarkan Akurasi, Presisi, Recall, dan F1-Score[cite: 51].

## 📂 Dataset
[cite_start]Data yang digunakan bersumber dari repositori publik (Kaggle) yang mencakup citra daun pisang dalam berbagai kondisi[cite: 80]. Dataset dibagi menjadi 7 kelas kategori:

1.  [cite_start]**Banana Black Sigatoka Disease** (Bercak garis gelap) [cite: 82, 120]
2.  [cite_start]**Banana Yellow Sigatoka Disease** (Bercak kuning meluas) [cite: 82, 126]
3.  [cite_start]**Banana Panama Disease** (Layu fusarium) [cite: 83, 125]
4.  [cite_start]**Banana Bract Mosaic Virus Disease** [cite: 121]
5.  [cite_start]**Banana Moko Disease** [cite: 124]
6.  [cite_start]**Banana Insect Pest Disease** (Serangan Hama) [cite: 123]
7.  [cite_start]**Banana Healthy Leaf** (Daun Sehat) [cite: 122]

## ⚙️ Metodologi & Arsitektur
* [cite_start]**Metode:** Convolutional Neural Network (CNN)[cite: 54].
* **Preprocessing:**
    * [cite_start]*Resizing:* Menyeragamkan dimensi gambar (misal: 128x128 atau 224x224 pixel)[cite: 89].
    * [cite_start]*Normalisasi:* Rescaling nilai piksel menjadi range 0-1[cite: 92].
    * [cite_start]*Augmentasi Data:* Rotasi, zoom, dan flip untuk mencegah overfitting[cite: 93].
* [cite_start]**Split Data:** Pembagian data latih (training) dan data uji (testing)[cite: 94].

## 📊 Hasil Evaluasi Model
[cite_start]Berdasarkan pengujian menggunakan data uji sebanyak 652 sampel, model mencapai performa berikut[cite: 127, 134]:

| Metrik | Nilai (Weighted Avg) | Keterangan |
| :--- | :--- | :--- |
| **Akurasi** | **77.91%** | Model memprediksi benar ~78 dari 100 citra |
| **Presisi** | 79.46% | Tingkat relevansi prediksi positif |
| **Recall** | 77.91% | Kemampuan menemukan kembali data relevan |
| **F1-Score** | 77.10% | Keseimbangan antara Presisi dan Recall |

**Catatan Analisis:**
* [cite_start]✅ **Performa Terbaik:** Kelas *Healthy Leaf* (F1-Score 0.94), model sangat handal membedakan tanaman sehat[cite: 154, 202].
* [cite_start]⚠️ **Kelemahan:** Kelas *Black Sigatoka* memiliki Recall terendah (48%), sering tertukar karena kemiripan visual yang tinggi[cite: 143, 206].
* [cite_start]⚠️ **Bias Hama:** Model cenderung agresif memprediksi *Insect Pest* (Recall tinggi, Presisi rendah)[cite: 207].

## 🚀 Pengembangan Selanjutnya (Future Work)
Untuk meningkatkan akurasi di atas 90% dan kegunaan sistem, rencana pengembangan meliputi:
1.  [cite_start]**Data Balancing:** Menambah sampel pada kelas minoritas (Yellow Sigatoka & Panama Disease)[cite: 291].
2.  [cite_start]**Transfer Learning:** Menggunakan *pre-trained models* seperti MobileNetV2, ResNet, atau VGG16[cite: 292].
3.  [cite_start]**Aplikasi Mobile:** Integrasi model ke Android/iOS menggunakan TensorFlow Lite untuk deteksi *real-time* di kebun[cite: 294].
4.  [cite_start]**Optimasi Hyperparameter:** Tuning learning rate, epoch, dan batch size[cite: 295].

## 💻 Tech Stack
* Python
* TensorFlow / Keras
* Jupyter Notebook
* Matplotlib / Seaborn (untuk visualisasi evaluasi)

---
[cite_start]*Dibuat berdasarkan Laporan Tugas Besar Mata Kuliah Kecerdasan Buatan, Universitas Telkom, 2025.* [cite: 2, 14]