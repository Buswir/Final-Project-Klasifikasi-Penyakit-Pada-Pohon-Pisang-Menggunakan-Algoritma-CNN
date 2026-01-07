# Klasifikasi Penyakit Pada Pohon Pisang Menggunakan Algoritma CNN 🍌

Proyek ini adalah implementasi *Deep Learning* untuk mendeteksi dan mengklasifikasikan jenis penyakit pada daun pohon pisang secara otomatis. Dibangun menggunakan metode **Convolutional Neural Network (CNN)**, sistem ini bertujuan membantu petani melakukan diagnosis dini secara cepat dan akurat.

## 👥 Anggota Kelompok
Mahasiswa Program Studi S1 Teknik Informatika, Universitas Telkom Purwokerto:
* **Arjun Ahmad Santoso** (2311102211)
* **Buswiryawan Raditya Boenyamin** (2311102090)
* **Willyan Hyuga Pratama** (2211102129)

## 📖 Latar Belakang
Produktivitas pisang sering terganggu oleh penyakit daun seperti *Black Sigatoka* dan *Panama Disease*. Identifikasi manual sering kali subjektif dan rentan kesalahan karena gejala visual yang mirip. Proyek ini memanfaatkan pengolahan citra digital untuk mengenali pola visual penyakit (tekstur, warna, bercak) secara otomatis.

## 🎯 Tujuan
1.  **Ekstraksi Fitur Otomatis:** Menggunakan CNN untuk mempelajari fitur visual daun tanpa ekstraksi manual.
2.  **Klasifikasi Multi-Kelas:** Mampu membedakan 7 kondisi daun yang berbeda.
3.  **Akurasi Objektif:** Meminimalkan kesalahan diagnosis manual dengan sistem cerdas.

## 📂 Dataset
Dataset bersumber dari repositori publik (Kaggle) dan mencakup 7 kelas kategori:
1.  **Banana Black Sigatoka Disease**
2.  **Banana Yellow Sigatoka Disease**
3.  **Banana Panama Disease** (Layu Fusarium)
4.  **Banana Bract Mosaic Virus Disease**
5.  **Banana Moko Disease**
6.  **Banana Insect Pest Disease** (Serangan Hama)
7.  **Banana Healthy Leaf** (Daun Sehat)

## ⚙️ Metodologi
* **Model:** Convolutional Neural Network (CNN).
* **Preprocessing:**
    * *Resizing:* Penyeragaman dimensi citra (misal: 128x128 / 224x224).
    * *Normalisasi:* Rescaling nilai piksel (0-1).
    * *Augmentasi:* Rotasi, zoom, dan flip untuk memperkaya data latih.

## 📊 Hasil Evaluasi
Berdasarkan pengujian pada 652 sampel data uji, model mencapai performa berikut:

| Metrik | Nilai (Weighted Avg) |
| :--- | :--- |
| **Akurasi** | **77.91%** |
| **Presisi** | 79.46% |
| **Recall** | 77.91% |
| **F1-Score** | 77.10% |

**Analisis Hasil:**
* ✅ **Sangat Baik:** Deteksi *Healthy Leaf* (F1-Score 0.94) dan *Yellow Sigatoka* (Presisi 0.93).
* ⚠️ **Tantangan:** Deteksi *Black Sigatoka* (Recall 48%) masih rendah karena kemiripan visual yang tinggi dengan penyakit lain.
* ⚠️ **Sensitivitas:** Model cukup agresif mendeteksi serangan hama (*Insect Pest*), namun dengan presisi yang perlu ditingkatkan.

## 🚀 Pengembangan Selanjutnya (Future Work)
1.  **Data Balancing:** Menambah sampel pada kelas minoritas (seperti Yellow Sigatoka & Panama Disease).
2.  **Transfer Learning:** Mengimplementasikan model *pre-trained* (MobileNetV2, ResNet, VGG16) untuk meningkatkan akurasi >90%.
3.  **Mobile Integration:** Penerapan model ke aplikasi Android/iOS menggunakan TensorFlow Lite untuk deteksi *real-time* di lapangan.
4.  **Hyperparameter Tuning:** Optimasi *learning rate* dan *epoch* untuk mengurangi *loss*.

## 🛠️ Tech Stack
* **Bahasa:** Python
* **Library:** TensorFlow / Keras, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab

---
*Dibuat untuk memenuhi Tugas Besar Mata Kuliah Kecerdasan Buatan, Universitas Telkom, 2025.*
