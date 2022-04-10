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
![churn](https://user-images.githubusercontent.com/97740444/162631076-9a90e4a4-b7c0-465e-b5f9-da59cf4ccf6c.png)
Terdapat 26.5% pelanggan yang churn dan sekitar 73.5% pelanggan yang tidak churn

- Dari golongan usia manakah pelanggan yang melakukan churn?
![senior](https://user-images.githubusercontent.com/97740444/162630310-806bf4bb-58f1-48dc-891d-a1424c7c3074.png)
Dari analisis tersebut, kebanyakan pelanggan yang churn berasal dari golongan muda

- Berapa banyak biaya bulanan yang dimiliki oleh pelanggan yang churn?
![month](https://user-images.githubusercontent.com/97740444/162631096-93801d33-3133-4704-8515-c89a17853e81.png)
Jumlah yang dibebankan kepada pelanggan yang churn setiap bulan sebagian besar berada di kisaran 75-125

- Berapa bulan waktu yang dihabiskan pelanggan churn untuk berada di company?
![tenure](https://user-images.githubusercontent.com/97740444/162631107-fd9eba14-783b-4e45-822c-ad5ab586325c.png)
Pelanggan yang churn sebagian besar telah menetap di perusahaan paling tidak sekitar 0-20 bulan. Jika dibandingkan dengan pelanggan yang tidak churn, pelanggan yang churn termasuk orang-orang yang baru bergabung kedalam perusahaan

- Apa jenis internet yang digunakan oleh pelanggan yang churn?
![internet](https://user-images.githubusercontent.com/97740444/162631123-3394f544-6ee5-4001-9310-690f0b01c867.png)
Sebagian besar pelanggan yang churn itu menggunakan fiber optic untuk internet service

- Apa jenis pembayaran yang dilakukan oleh pelanggan yang churn?
![payment](https://user-images.githubusercontent.com/97740444/162631145-f5a929b1-8399-4f93-a379-51784061558a.png)
Electronic check lebih dominan digunakan oleh pelanggan yang churn

- Region mana yang sering terjadi churn?
![image](https://user-images.githubusercontent.com/97740444/162631389-22779326-3cb2-4ac8-b4cd-653b10cc436f.png)
Customer yang berasal dari Jerman yang paling banyak melakukan churn
