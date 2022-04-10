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
![image](https://user-images.githubusercontent.com/97740444/162630198-049319e2-f2bb-4e0d-a836-0d16ba7dfb5d.png)
Terdapat 26.5% pelanggan yang churn dan sekitar 73.5% pelanggan yang tidak churn

- Dari golongan usia manakah pelanggan yang melakukan churn?
![senior](https://user-images.githubusercontent.com/97740444/162630310-806bf4bb-58f1-48dc-891d-a1424c7c3074.png)
Dari analisis tersebut, kebanyakan pelanggan yang churn berasal dari golongan muda

- Berapa banyak biaya bulanan yang dimiliki oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162630371-a556436d-4eb4-473c-939e-3cba7789d0fa.png)
Jumlah yang dibebankan kepada pelanggan yang chur setiap bulan sebagian besar berada di kisaran 75-125

- Berapa bulan waktu yang dihabiskan pelanggan churn untuk berada di company?
![image](https://user-images.githubusercontent.com/97740444/162630422-620eeb05-c54d-42d5-a705-4f9c4f37bcd0.png)
Pelanggan yang churn sebagian besar telah menetap di perusahaan paling tidak sekitar 0-20 bulan. Jika dibandingkan dengan pelanggan yang tidak churn, pelanggan yang churn termasuk orang-orang yang baru bergabung kedalam perusahaan

- Apa jenis internet yang digunakan oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162630476-248af1ec-dbe4-4951-8067-441b4684fc30.png)
Sebagian besar pelanggan yang churn itu menggunakan fiber optic untuk internet service

- Apa jenis pembayaran yang dilakukan oleh pelanggan yang churn?
![image](https://user-images.githubusercontent.com/97740444/162630505-603120c5-b993-42d0-9cfd-28a3f62294fc.png)
Electronic check lebih dominan digunakan oleh pelanggan yang churn

- Region mana yang sering terjadi churn?
![image](https://user-images.githubusercontent.com/97740444/162630530-3292ff10-f7f1-4b00-ac37-e15846ec6a96.png)
Customer yang berasal dari Jerman yang paling banyak melakukan churn


# Modelling

## Random Forest Classifier

- Random forest classifier adalah supervised machine learning yang digunakan untuk mengklasifikasikan
- 

