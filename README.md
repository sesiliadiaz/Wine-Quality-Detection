# Wine Quality Classification 

Project ini bertujuan untuk membangun model machine learning untuk mengklasifikasikan kualitas wine berdasarkan karakteristik kimia dan fisiknya. Dataset yang digunakan berisi berbagai parameter wine seperti acidity, pH, alcohol content, dan lainnya yang dapat mempengaruhi kualitas akhir dari wine tersebut.Model dibangun dengan mempertimbangkan ketidakseimbangan data (imbalanced data) dan disertai dengan proses synthetic oversampling , scaling, evaluasi performa, serta penyimpanan model untuk digunakan kembali



## Dataset

### Sumber Data
Dataset **Wine Quality** berisi 1,143 sampel wine dengan 12 fitur karakteristik:

### Fitur-fitur Dataset:
1. **fixed acidity** - Tingkat keasaman tetap
2. **volatile acidity** - Tingkat keasaman volatil
3. **citric acid** - Kandungan asam sitrat
4. **residual sugar** - Kandungan gula sisa
5. **chlorides** - Kandungan klorida
6. **free sulfur dioxide** - Kandungan sulfur dioksida bebas
7. **total sulfur dioxide** - Total kandungan sulfur dioksida
8. **density** - Kepadatan wine
9. **pH** - Tingkat keasaman/kebasaan
10. **sulphates** - Kandungan sulfat
11. **alcohol** - Kandungan alkohol
12. **quality** - Skor kualitas (target variable: 3-8)

### Distribusi Kelas:
Berdasarkan quality score, data dibagi menjadi 3 kategori:
- **Low Quality** (score ≤ 4): 39 samples (3.4%)
- **Medium Quality** (score 5-6): 945 samples (82.7%)
- **High Quality** (score ≥ 7): 159 samples (13.9%)



## Alur Pemodelan (Pipeline)

### 1. Exploratory Data Analysis (EDA)
- Analisis distribusi data
- Identifikasi missing values
- Analisis korelasi antar fitur
- Visualisasi distribusi kelas

### 2. Data Preprocessing
- Handling missing values (jika ada)
- Feature scaling menggunakan StandardScaler
- Mapping quality score ke 3 kategori (Low, Medium, High)

### 3. Mengatasi Class Imbalance
- **Synthetic Oversampling**: Membuat synthetic samples untuk minority class
- **Class Weighting**: Memberikan bobot lebih tinggi pada minority class
- **Combined Approach**: Kombinasi oversampling dan class weighting

### 4. Model Development
- Algoritma: **Random Forest Classifier**
- Hyperparameter tuning untuk optimal performance
- Cross-validation untuk robust evaluation

### 5. Model Evaluation
- Classification Report
- Confusion Matrix
- ROC Curve (multiclass)
- Feature Importance



## Struktur Project

```
wine-quality-classification/
│
├── WineQT.csv                          # Dataset 
├── Modeling.ipynb                      # Model 
├── EDA.ipynb                           # Exploratory Data Analysis
├── README.md         
├── Scaler.pkl                          
└── wine_quality_model.pkl                 
```



## Cara Menggunakan

### Install Dependency:
```bash
pip install pandas numpy scikit-learn matplotlib joblib
```

### Menjalankan Notebook:
- Buka dan jalankan:
```bash
Modeling.ipynb
```
Pastikan file WineQT.csv berada di direktori yang sama.


