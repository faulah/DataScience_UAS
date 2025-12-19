# 📘 Judul Proyek
*KLASIFIKASI JENIS DRY BEAN MENGGUNAKAN MACHINE LEARNING DAN DEEP LEARNING*

## 👤 Informasi
- **Nama:** Khoirul Faulah Nur Rohmah
- **NIM:** 233307053
- **Kelas:** 5B
- **Repo:** https://github.com/faulah/DataScience_UAS
- **Video:** https://drive.google.com/drive/u/1/folders/1EoLViHlWg052erRLK-ozAKRyasT4vejB 

---

# 1. 🎯 Ringkasan Proyek
- Menyelesaikan permasalahan sesuai domain  
- Melakukan data preparation  
- Membangun 3 model: **Baseline**, **Advanced**, **Deep Learning**  
- Melakukan evaluasi dan menentukan model terbaik  

---

# 2. 📄 Problem & Goals
**Problem Statements:**  
Bagaimana cara membangun model yang mampu mengklasifikasi 7 jenis Dry Bean ( Kacang Kering) secara presisi berdasarkan 16 fitur morfologi?
 

**Goals:**  
Mendapatkan model klasifikasi terbaik dengan akurasi 92.95% untuk membedakan jenis kacang

---
## 📂 Struktur Folder 

```text
UAS_DataScience/
├── data/                  # Berisi dataset mentah (Dry_Bean_Dataset.csv) 
├── notebooks/             
│   └── UAS.ipynb  
|                
├── models/                
│   ├── best_model_rf.pkl               # Model Random Forest
│   ├── logistic_regression_model.pkl   # Model Logistic Regression
│   └── deep_learning_mlp_model.h5      # Model Deep Learning (MLP) 
├── images/                
│   ├── gambar1.png
│   ├── gambar2.png
|   ├── gambar3.png
|   ├── gambar4.png
│   └── gambar5.png
├── README.md              
├── requirements.txt       
├── .gitignore
├── CHECKLIST.pdf             
└── LAPORAN.pdf

```
---

# 3. 📊 Dataset
- **Sumber:** Dataset berasal dari UCI Machine Learning Repository (Dry Bean Dataset) 
- **Jumlah Data:** 13.611 baris data
- **Tipe:** Multivariate Classification (Data Tabular)

### Fitur Utama

| Fitur | Deskripsi |
| :--- | :--- |
| **Area** | Jumlah piksel dalam batas benih (ukuran luas). |
| **Perimeter** | Panjang keliling benih. |
| **MajorAxisLength** | Jarak antara dua ujung terjauh pada benih. |
| **MinorAxisLength** | Jarak antara dua ujung terpendek pada benih. |
| **Aspect Ratio** | Rasio antara Major Axis Length dan Minor Axis Length. |
| **Eccentricity** | Eksentrisitas elips yang memiliki momen kedua yang sama dengan benih. |
| **ConvexArea** | Luas poligon konveks terkecil yang melingkupi benih. |
| **EquivDiameter** | Diameter lingkaran dengan luas yang sama dengan benih. |
| **Extent** | Rasio piksel dalam kotak pembatas terhadap luas kotak tersebut. |
| **Solidity** | Rasio Area terhadap ConvexArea (tingkat kepadatan). |
| **Roundness** | Tingkat kebulatan benih (menggunakan rumus keliling). |
| **Compactness** | Seberapa padat bentuk benih dibandingkan dengan lingkaran |
| **ShapeFactor1** | Faktor bentuk 1 (dimensi fitur geometrik). |
| **ShapeFactor2** | Faktor bentuk 2 (dimensi fitur geometrik). |
| **ShapeFactor3** | Faktor bentuk 3 (dimensi fitur geometrik). |
| **ShapeFactor4** | Faktor bentuk 4 (dimensi fitur geometrik). |

---

# 4. 🔧 Data Preparation
- Cleaning : Dataset ini sudah bersih dari pabriknya jadi tidak ada missing values atau data yang duplikat  
- Transformasi  Dilakukan standardization menggunakan StandardScaler. Proses ini mengubah nilai agar memiliki rata-rata 0 dan standar deviasi 1, sangat penting untuk membantu konvergensi model Deep Learning agar proses training lebih stabil  
- Splitting : Data ini dipisahkan dengan rasio 80% untuk training set untuk melatih model & 20% untuk test set untuk mengevaluasi model pada data 

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:** [Logistic Regression]  
- **Model 2 – Advanced ML:** [Random Forest]  
- **Model 3 – Deep Learning:** [Multilayer Perceptron)]  

---

# 6. 🧪 Evaluation
**Metrik:** Accuracy / F1 / MAE / MSE (pilih sesuai tugas)

### Hasil Singkat
| Model | Score | Catatan |
|-------|--------|---------|
| Baseline | [92.69%] | sebagai model liniermenunjukkan bahwa fitur-fitur geometrik memiliki pemisahan yang cukup jelas |
| Advanced | [92.54%] | peningkatan akurasi terjadi karena ensemble dalam menangani hubungan non-linier antara fitur |
| Deep Learning | [92.95%] | ini mampu mempelajari pola yang sangat komplek, namun memerlukan proses training yang lebih lama dibandingkan model ML tradisional |

---

# 7. 🏁 Kesimpulan
- Model terbaik: [Multilayer Percetron (Deep Learning)]  
- Alasan: [hal ini menunjukkan bahwa fitur geometrik ini memiliki pola non-linier kompleks yang lebih baik ditangkap oleh algoritma cerdas dari pada model linier sederhana.]  
- Insight penting: [Fitur dimensi seperti Area dan Perimeter sangat menentukan jenis kacang, namun fitur bentuk (ShapeFactors) sangat krusial untuk membedakan varietas yang ukurannya mirip tetapi geometrinya berbeda]   

---

# 8. 🔮 Future Work
- [✅] Tambah data  
- [✅] Tuning model  
- [✅] Coba arsitektur DL lain  
- [✅] Deployment  

---

# 9. 🔁 Reproducibility
Gunakan environment:
