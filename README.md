# Telco-Customer-Churn
Preprocessing, exploratory analysis, and create machine learning model


# Use Case

- Use case summary
- Objective Statement :
  * Memperoleh bisnis insight seberapa banyak pelanggan yang churn
  * Memperoleh bisnis insight bagaimana profil pelanggan yang churn
  * Untuk mendeteksi kemungkinan pelanggan yang churn dan meminimalisirnya
- Business Benefit :
  * Membantu mendeteksi pelanggan yang churn
  * Mendapatkan gambaran terkait bagaimana treatment yang bisa dilakukan untuk menghentikan churning pelanggan


# Business Understanding

- Berapa jumlah pengguna yang churn dan tidak churn?
- Dari golongan usia manakah pelanggan yang melakukan churn?
- Berapa banyak biaya bulanan yang dimiliki oleh pelanggan yang churn?
- Berapa bulan waktu yang dihabiskan pelanggan churn berada di company?
- Apa jenis internet yang digunakan oleh pelanggan yang churn?
- Apa jenis pembayaran yang dilakukan oleh pelanggan yang churn?
- Region mana yang sering terjadi churn?


# Data Understanding

- Data terdiri dari 7043 baris dan 21 kolom
- Kolom terdiri dari :
  * Customer Id : Id customer
  * Gender : Jenis kelamin
  * Senior citizen : Apakah customer lanjut usia atau tidak (1 atau 0)
  * Partner : Apakah pelanggan memiliki pasangan atau tidak (yes atu no)
  * Dependent : Apakah pelanggan memiliki tanggungan atau tidak
  * Tenure : Banyaknya bulan yang dihabiskan oleh pelanggan di perusahaan
  * Phoneservice : Apakah pelanggan memiliki servis telepon atau tidak
  * Multiplelines : Apakah pelanggan memiliki banyak saluran atau tidak (yes atau no)
  * Internet Service : Provider internet servis pelanggan (DSL, fiber optic, no)
  * Online Security : Apakah pelanggan memiliki keamanan online atau tidak
  * Online backup : Apakah pelanggan memiliki online back up atau tidak
  * Device protection : Apakah pelanggan memiliki pengamanan device atau tidak
  * Tech Support : Apakah pelanggan memiliki dukungan teknis atau tidak
  * Streaming TV : Apakah pelanggan memiliki streaming tv atau tidak
  * Streaming movie : Apakah pelanggan memiliki streaming film atau tidak
  * Contract : Jangka waktu kontrak pelanggan
  * Paperless Billing : Apakah pelanggan memiliki tagihan paperless atau tidak
  * Payment method : Metode pembayaran pelanggan
  * Monthlycharges : Jumlah yang dibebankan kepada pelanggan setiap bulan
  * Total Charges : Jumlah total yang dibebankan kepada pelanggan
  * Churn : Apakah pelanggan churn atau tidak


# Data Cleaning

- Data memiliki missing value sebesar 0.15%, kita bisa melakukan beberapa handling seperti input dengan median, modus, dan mean atau dilakukan drop. Disini saya melakukan inputasi missing value dengan median
- Tidak ada data yang duplikat


# Exploratory Data Analysis

- Berapa jumlah pengguna yang churn dan tidak churn?
![image](https://user-images.githubusercontent.com/97740444/162632901-a16717e0-d700-4b55-b357-f425dca08fdd.png)
Terdapat 26.5% pelanggan yang churn dan sekitar 73.5% pelanggan yang tidak churn

- Dari golongan usia manakah pelanggan yang melakukan churn?
![image](https://user-images.githubusercontent.com/97740444/162632921-d7847a10-420b-437f-bd56-16e7d41c6091.png)
Dari analisis tersebut, kebanyakan pelanggan yang churn berasal dari golongan muda

- Berapa banyak biaya bulanan yang dimiliki oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162632939-1bd018d6-cdb6-4afe-b3f8-80f1c5b9fc24.png)
Jumlah yang dibebankan kepada pelanggan yang churn setiap bulan sebagian besar berada di kisaran 75-125

- Berapa bulan waktu yang dihabiskan pelanggan churn untuk berada di company?
![image](https://user-images.githubusercontent.com/97740444/162632965-f2ff53b8-d010-4872-ad52-0df3374958db.png)
Pelanggan yang churn sebagian besar telah menetap di perusahaan paling tidak sekitar 0-20 bulan. Jika dibandingkan dengan pelanggan yang tidak churn, pelanggan yang churn termasuk orang-orang yang baru bergabung kedalam perusahaan

- Apa jenis internet yang digunakan oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162632986-0f420136-b00e-4dfc-af9c-d0a836e6d95a.png)
Sebagian besar pelanggan yang churn itu menggunakan fiber optic untuk internet service

- Apa jenis pembayaran yang dilakukan oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162633009-ad6d937d-882a-4c0d-b12e-035e42fd7cc4.png)
Electronic check lebih dominan digunakan oleh pelanggan yang churn

- Region mana yang sering terjadi churn?
![image](https://user-images.githubusercontent.com/97740444/162633033-eb76adf8-536e-4c64-b469-5e3401c3fe21.png)
Customer yang berasal dari Jerman yang paling banyak melakukan churn

# Modelling
## Random Forest
- Perbandingan value dari variable target
![image](https://github.com/ikrarmuhamad/Telco-Customer-Churn/assets/97740444/8de533a9-8824-4b7e-a77c-37445396584d)
Terdapat perbedaan ukuran dari variable target, masih tergolong cukup baik untuk dilakukan modelling tanpa mengatasi permasalahan imbalance data. Namun disini diatasi permasalahan imbalance data, menggunakan teknik SMOTE.
- Model Random Forest memiliki performa yang cukup baik dengan akurasi sekitar 85% dan tingkat presisi mencapai 86%
- ROC Curve
![image](https://github.com/ikrarmuhamad/Telco-Customer-Churn/assets/97740444/dc05f89a-a78f-4373-9cb5-c2d5176b672b)
Area ROC-AUC dari hasil model Random Forest memiliki performa yang baik, dengan area ROC berada di sekitar 0.85. Ini terbilang cukup baik karena peningkatan True Positif yang pesat tidak diiringi dengan peningkatan False positif. Sehingga model memiliki nilai True Positif Rate yang cukup baik
- Confusion Matrix
![image](https://github.com/ikrarmuhamad/Telco-Customer-Churn/assets/97740444/382e31e0-a1cb-4c61-b646-f538efadc69f)
Berdasarkan hasil dari modelling, Random Forest terlihat memiliki performa yang sangat baik dengan beberapa metrik sebagai berikut :
  * Presisi : 86%
  * Akurasi : 85%
  * F1-Score : 85%
  * Recall : 85%

