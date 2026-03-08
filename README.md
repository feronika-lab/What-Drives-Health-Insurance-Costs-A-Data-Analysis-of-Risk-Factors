# What-Drives-Health-Insurance-Costs-A-Data-Analysis-of-Risk-Factors-Using-Machine-Learning

## Latar Belakang

Biaya layanan kesehatan merupakan salah satu komponen utama dalam industri asuransi kesehatan. Oleh karena itu, memahami **faktor-faktor yang mempengaruhi besarnya biaya klaim kesehatan** menjadi sangat penting untuk membantu **menentukan premi yang lebih adil dan sesuai dengan tingkat risiko tertanggung** . Sementara itu, bagi peserta asuransi, pemahaman terhadap faktor risiko dapat membantu menjelaskan mengapa biaya atau premi kesehatan dapat berbeda antar individu.

Penelitian ini bertujuan untuk membangun model prediktif yang dapat mengestimasi biaya asuransi kesehatan berdasarkan karakteristik individu, seperti usia, indeks massa tubuh (BMI), jumlah tanggungan, serta status merokok.

Dataset yang digunakan berisi informasi profil kesehatan individu beserta total biaya medis yang ditagihkan oleh perusahaan asuransi.

Melalui pendekatan **machine learning**, penelitian ini membandingkan beberapa model regresi untuk menentukan model yang paling optimal dalam memprediksi biaya asuransi kesehatan.

---

# Tujuan Penelitian

Penelitian ini bertujuan untuk:

- memahami faktor-faktor yang mempengaruhi biaya asuransi kesehatan
- membandingkan performa berbagai model machine learning
- mengembangkan model prediksi yang akurat dan stabil
- menyediakan pendekatan data-driven dalam analisis risiko kesehatan

---

# Dataset

Dataset yang digunakan berisi **1.338 data individu** dengan beberapa variabel yang berkaitan dengan profil risiko kesehatan.

### Variabel dalam dataset

| Variabel | Tipe | Deskripsi |
|---|---|---|
| age | Numerik | Usia peserta |
| sex | Kategorikal | Jenis kelamin |
| bmi | Numerik | Body Mass Index |
| children | Numerik | Jumlah tanggungan |
| smoker | Kategorikal | Status merokok |
| region | Kategorikal | Wilayah tempat tinggal |
| charges | Numerik | Total biaya medis yang ditagihkan |

Variabel **charges** merupakan variabel target yang akan diprediksi oleh model.

---

# Metodologi Penelitian

Penelitian ini dilakukan melalui beberapa tahapan utama dalam analisis data dan pemodelan prediktif.

## 1. Eksplorasi Data (Exploratory Data Analysis)

Tahap awal penelitian adalah memahami karakteristik data melalui:

- Statistik deskriptif
- Distribusi variabel
- Visualisasi hubungan antar variabel
- Analisis korelasi

Tujuan dari tahap ini adalah untuk mengidentifikasi pola hubungan antara variabel risiko dengan biaya asuransi.

---

## 2. Deteksi Outlier

Outlier atau nilai ekstrem dapat mempengaruhi performa model prediktif.

Deteksi outlier dilakukan dengan menggunakan:

- Boxplot
- Analisis distribusi variabel numerik

Tujuan tahap ini adalah untuk memastikan bahwa data yang digunakan dalam pemodelan tidak mengandung nilai yang terlalu menyimpang.

---

## 3. Data Cleaning dan Preprocessing

Tahap ini bertujuan untuk menyiapkan data agar siap digunakan dalam proses pemodelan.

Proses yang dilakukan antara lain:

- Transformasi variabel kategorikal menjadi numerik
- Penghapusan variabel yang tidak digunakan
- Penanganan outlier
- Pemisahan data training dan testing

Data kemudian dibagi menjadi:

- **Training set (80%)**
- **Testing set (20%)**

---

# Pembuatan Model Prediksi

Beberapa model regresi digunakan dan dibandingkan untuk menemukan model dengan performa terbaik.

Model yang digunakan dalam penelitian ini antara lain:

### 1. Linear Regression

Model regresi linear digunakan sebagai model dasar untuk memprediksi hubungan antara variabel independen dan biaya asuransi.

Kelebihan model ini adalah sederhana dan mudah diinterpretasikan, namun memiliki keterbatasan dalam menangkap hubungan non-linear.

---

### 2. Random Forest Regressor

Random Forest merupakan model berbasis **ensemble learning** yang menggunakan banyak decision tree untuk meningkatkan akurasi prediksi.

Model ini mampu menangkap hubungan non-linear serta interaksi antar variabel risiko.

---

### 3. Gradient Boosting Regressor

Gradient Boosting membangun model secara bertahap dengan memperbaiki kesalahan dari model sebelumnya.

Metode ini sering digunakan dalam berbagai aplikasi machine learning karena mampu menghasilkan performa prediksi yang tinggi.

---

### 4. XGBoost Regressor

XGBoost merupakan algoritma boosting yang dioptimalkan untuk kecepatan dan performa.

Model ini banyak digunakan dalam kompetisi data science karena kemampuannya dalam menangani dataset kompleks.

---

# Hyperparameter Tuning

Untuk meningkatkan performa model, dilakukan proses **hyperparameter tuning** menggunakan metode:

- GridSearchCV
- Cross-validation

Proses ini bertujuan untuk menemukan kombinasi parameter terbaik bagi setiap model.

---

# Evaluasi Model

Performa model dievaluasi menggunakan beberapa metrik berikut:

### R² Score

R² digunakan untuk mengukur seberapa baik model mampu menjelaskan variasi dalam data.

Evaluasi dilakukan pada:

- Training data
- Testing data
- Cross-validation

Pendekatan ini digunakan untuk memastikan bahwa model tidak mengalami **overfitting** maupun **underfitting**.

---

# Hasil dan Perbandingan Model

Beberapa model menunjukkan performa yang berbeda dalam memprediksi biaya asuransi.

Model boosting seperti:

- **Gradient Boosting**
- **XGBoost**

menunjukkan performa yang lebih stabil dan akurat dibandingkan model lain.

Model-model ini mampu menangkap hubungan kompleks antara faktor risiko kesehatan dengan biaya medis.

---

# Implementasi Estimasi Biaya Asuransi

Model terbaik kemudian digunakan untuk melakukan estimasi biaya asuransi bagi individu baru.

Contoh penggunaan model:

Input:
- Age = 19
- BMI = 27.9
- Children = 0
- Smoker = Yes

Output:
Estimasi biaya asuransi kesehatan


Estimasi ini dapat digunakan sebagai dasar dalam:

- simulasi premi
- analisis risiko kesehatan
- perencanaan biaya medis

---

# Insight 

Beberapa faktor risiko yang memiliki pengaruh signifikan terhadap biaya asuransi antara lain:

### Status Merokok
Peserta yang merokok memiliki biaya medis yang secara signifikan lebih tinggi dibandingkan non-perokok.

### Usia
Biaya kesehatan cenderung meningkat seiring bertambahnya usia.

### BMI
BMI yang tinggi berhubungan dengan peningkatan risiko kesehatan dan biaya medis.

Variabel-variabel ini dapat digunakan sebagai **risk rating factors** dalam proses penentuan premi asuransi kesehatan.

---

# Teknologi yang Digunakan

Penelitian ini menggunakan beberapa library Python, antara lain:
Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, XGBoost

---

# Penutup

Pendekatan machine learning memberikan peluang baru dalam analisis aktuaria, khususnya dalam pemodelan risiko dan estimasi biaya kesehatan. Dengan memanfaatkan data historis dan teknik pemodelan yang tepat, perusahaan asuransi dapat memperoleh estimasi biaya yang lebih akurat serta meningkatkan kualitas pengambilan keputusan dalam manajemen risiko.

