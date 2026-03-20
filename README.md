# 🛒 Customer Purchase Prediction using Stacking Ensemble Method

## 📌 Deskripsi
Project ini merupakan implementasi Data Mining untuk memprediksi status pembelian pelanggan (PurchaseStatus) menggunakan metode **Stacking Ensemble**. Dataset yang digunakan adalah data pelanggan berisi 500.000+ baris dengan 19 fitur yang mencakup informasi demografis, perilaku, dan transaksi pelanggan.

---

## 📂 Dataset
- **Nama File:** `customerData_500k.csv`
- **Jumlah Data:** 502.500 baris, 19 kolom
- **Target Variable:** `PurchaseStatus` (0 = Tidak Beli, 1 = Beli)

---

## ⚙️ Tahapan Pengerjaan

### 1. Data Understanding
- Eksplorasi awal dataset (shape, info, describe)
- Identifikasi missing values, duplikat, dan inkonsistensi data

### 2. Exploratory Data Analysis (EDA)
- Distribusi fitur numerik dan kategorikal
- Perbandingan distribusi fitur terhadap target
- Deteksi outlier menggunakan Boxplot dan metode IQR
- Correlation heatmap antar fitur numerik

### 3. Preprocessing
- Menghapus kolom `CustomerID` yang tidak relevan
- Standarisasi inkonsistensi data (`Gender`, `Region`)
- Menghapus 2.500 data duplikat
- Imputasi missing values (median untuk numerik, modus untuk kategorikal)
- Ordinal Encoding pada `CustomerSegment`
- One-Hot Encoding pada fitur nominal
- Train-Test Split (80:20) dengan stratifikasi
- Feature Scaling menggunakan StandardScaler

### 4. Modelling (Stacking Ensemble)
- **Base Learner 1:** Random Forest (n_estimators=100, max_depth=10)
- **Base Learner 2:** Gradient Boosting (n_estimators=100, learning_rate=0.1)
- **Meta Learner:** Logistic Regression
- Cross-validation: 5-fold

### 5. Evaluasi
| Metrik | Nilai |
|--------|-------|
| Accuracy | 92.18% |
| ROC-AUC | 97.86% |
| F1-Score (Macro) | 0.92 |

## 📁 Struktur File
```
├── main.ipynb               # Notebook utama (preprocessing + modelling)
├── customerData_500k.csv    # Dataset
└── README.md                # Dokumentasi project
```

---

## 🎥 Demo Video
Link video demo preprocessing dan hasil pemodelan:
https://drive.google.com/file/d/1tSojHPIgi-w_BlHuL_JXPqqMnSoHcIf3/view?usp=drive_link 



jjj
---

## 👤 Author
- **Nama:** Nazly Rafa Oktafian Nuzqu
- **NIM:** 2311103078
- **Mata Kuliah:** Data Mining
- **Kelas:**S1SI-REG02
