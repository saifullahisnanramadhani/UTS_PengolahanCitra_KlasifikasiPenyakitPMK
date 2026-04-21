# 🐄 Klasifikasi Penyakit Mulut dan Kuku (PMK) pada Sapi  
### Menggunakan HSV Histogram dan Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-SVM%20%7C%20KNN%20%7C%20RandomForest-orange)

---

## 📌 Deskripsi

Proyek ini merupakan implementasi **pengolahan citra digital** untuk melakukan **klasifikasi citra sapi** ke dalam dua kategori:

- 🟢 **Sehat**
- 🔴 **Terindikasi Penyakit Mulut dan Kuku (PMK)**

Metode yang digunakan:
- Ekstraksi fitur warna menggunakan **HSV Histogram**
- Klasifikasi menggunakan algoritma:
  - Support Vector Machine (SVM)
  - K-Nearest Neighbor (KNN)
  - Random Forest

Selain itu, ditambahkan visualisasi **heatmap** untuk melihat area citra yang berkontribusi terhadap hasil klasifikasi.

---

## 🧠 Metode yang Digunakan

### 🔹 1. Preprocessing
- Resize citra menjadi **128x128**
- Konversi warna dari **BGR → HSV**

### 🔹 2. Ekstraksi Fitur
- Menggunakan **HSV Histogram**
- Mengubah citra menjadi vektor numerik

### 🔹 3. Klasifikasi
- **SVM** → pemisahan data
- **KNN** → berdasarkan jarak terdekat
- **Random Forest** → ensemble decision tree

### 🔹 4. Evaluasi
- Accuracy
- Confusion Matrix
- Classification Report

### 🔹 5. Visualisasi
- Heatmap menggunakan **Sliding Window**

---

## 📊 Hasil Pengujian

| Metode          | Accuracy | Precision | Recall | F1-Score |
|----------------|---------|----------|--------|----------|
| SVM            | 0.605   | 0.69     | 0.61   | 0.57     |
| KNN            | 0.632   | 0.66     | 0.63   | 0.63     |
| Random Forest  | 0.776   | 0.82     | 0.78   | 0.77     |

✅ **Model terbaik: Random Forest**

---

## 📊 Confusion Matrix (Random Forest)

|               | Prediksi Sehat | Prediksi PMK |
|--------------|---------------|--------------|
| Aktual Sehat | 26            | 15           |
| Aktual PMK   | 2             | 33           |

---

## 📸 Output Program

Program menghasilkan:
- Prediksi kelas (Sehat / PMK)
- Visualisasi heatmap

> ⚠️ Catatan: Heatmap hanya menunjukkan area berdasarkan distribusi warna, bukan deteksi luka secara presisi.

---

## ⚙️ Instalasi

Pastikan Python sudah terinstall, kemudian install library berikut:

```bash
pip install opencv-python numpy matplotlib scikit-learn
