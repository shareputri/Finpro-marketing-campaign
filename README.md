# Marketing Campaign

Final Project Kelompok 10 DS Rakamin

Project ini menggunakan dataset yang dapat diunduh di[sini](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)

## EDA 
Exploratory Data Analysis untuk mencari insight dari dataset

### A. Descriptive Statistic

1. Cek Kesesuaian Dataset 
    menggunakan fungsi `.info() ` dan `.sample()` diketahui bahwa:
    *   terdapat 2240 baris data  
    *   Terdapat 29 kolom dimana : 3 jenis kategori, 26 jenis numerik
    * dilakukan perubahan tipe data pada kolom DT_Customer menjadi tipe datetime
    *   Terdapat 24 nilai kosong pada kolom *income*
    * nama kolom dan tipe data serta isi kolom sudah sesuai
  
2. Melihat Statistical Summary 
    Kesimpulan statistik menggunakan fungsi `.describe()`

    - Pada kolom income data maksimal **666666**, sementara 75% data hanya mencapai 68522, hal ini menandakan adanya outlier yang sangat besar. 
    - Pada year-birth, terdapat data yang memiliki rentang sangat jauh dari Q1
    - Z_CostContact dan Z_revenue memiliki nilai berupa konstanta ( nilai tetap) 
    - Marital_Status memiliki 8 nilai unique dengan 3 nilai yang kurang sesuai (YOLO, Alone, Absurd).

### B. Univariate Analysis
Analisis setiap kolom untuk melihat distribusi melalui chart

1. Berdasarkan tampilan boxplot :

    - Data yang tidak  memiliki outlier : kidhome, teenhome, recency dan - numstorepurchase
    - Outlier sangat besar : income dan year_birth
    - Kolom selain itu memiliki outlier namun tidak terlalu besar
    

2. Berdasarkan grafik `kdeplot()` maka sebaran data : 

    - Binomial : Kidhome dan Teenhome
    - Distribusi Normal : ID dan Recency
    - Positive Skewed : grafik selain kidhome, teenhome, id dan recency

Target / label yang digunakan adalah Response dimana perbandingan response diterima dan tidak adalah 334 : 1906, Rasio respon yang diterima adalah **14,91%**



### C. Multivariate Analysis
1. Perbandingan berbagai fitur terhadap label
   - Tidak ada korelasi linear yang cukup kuat antara masing-masing feature dan target, karena nilai korelasi pada fitur dan target di bawah 0.5, sehingga feature-feature yang akan dipertahankan baru dapat diketahui setelah perhitungan feature importance
    - Income dan Spending memiliki korelasi positif pada response, dimana semakin tinggi nilai income dan spending semakin besar tingkat respon sehingga fitur income dan spending perlu dipertahankan
    - Customer yang  berlangganan lebih lama memiliki tingkat response yang lebih besar
    - Customer dengan tingkat pendidikan lebih tinggi memiliki tingkat response yang lebih besar.
    
    
2. Perbandingan antar fitur
    - Setelah membandingkan  setiap accepted campaign, terdapat perubahan drastis dari campaign 1 ke campaign 3, akan tetapi hal ini belum memberikan informasi lebih jauh terkait campaign yang dilakukan






