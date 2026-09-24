# Supermarket Sales Dataset | Microsoft-Excel
![sales](Images/dataset-cover.jpg)
  > Project analisis end-to-end menggunakan Excel untuk menganalisis pola penjualan berdasarkan produk, segmen pelanggan, lokasi, metode pembayaran, dan periode waktu guna mengidentifikasi perbedaan performa penjualan serta area yang perlu diperhatikan dalam pengambilan keputusan bisnis.

Table Of Contents
1. Business Understanding
2. Data Source
3. Tool 
4. Data Cleaning
5. Sales Performance & Customer Segment Analysis.
6. Key Findings
7. Dashboard
8. Insight
9. Recommendations

## 1. Business Understanding

### 1.1 Business Background
Bisnis retail supermarket dengan beberapa cabang dan berbagai kategori produk. Perusahaan melayani pelanggan Member dan Normal melalui metode pembayaran Cash, Credit Card, dan Ewallet. Data transaksi digunakan untuk menganalisis performa penjualan berdasarkan produk, pelanggan, lokasi, pembayaran, dan periode waktu.

### 1.2 Business Problem
Manajemen supermarket belum memiliki gambaran yang jelas tentang di mana performa penjualan kuat dan di mana masih lemah. Penjualan berfluktuasi antar periode tanpa diketahui dimensi bisnis apa yang mendorongnya, dan belum diketahui apakah program membership berkaitan dengan nilai belanja yang lebih besar. Tanpa pemahaman ini, keputusan untuk mempertahankan atau meningkatkan area bisnis (produk, lokasi, segmen pelanggan, metode pembayaran) berisiko tidak tepat sasaran.

### 1.3 Project Objectives
  * Membandingkan pola penjualan berdasarkan segmen pelanggan, produk, lokasi, dan metode pembayaran.
  * Mengidentifikasi area yang perlu dipertahankan dan area yang berpotensi ditingkatkan.
  * Menganalisis perubahan sales antar bulan beserta dimensi bisnis yang berkontribusi.
  * Mengevaluasi pola pembelian dan efektivitas membership.
  * Menyusun rekomendasi bisnis berbasis temuan.
    
### 1.4 Business Questions
* Apakah terdapat perbedaan pola penjualan berdasarkan segmen pelanggan, produk, lokasi, dan metode pembayaran?
* Area mana yang perlu dipertahankan dan area yang memiliki potensi peningkatan?
* Bagaimana pola perubahan sales antar periode dan dimensi bisnis apa yang berkontribusi terhadap perbedaannya?
* Seberapa efektif membership dan pola pembelian pelanggan?

---

## 2. Data Source

| Dimensi | Keterangan |
| :--- | :--- |
| **Source** | Public Supermarket Sales Dataset |
| **Period** | Jan–Mar 2019 |
| **Records** | 1,000 transactions |
| **Coverage** | 3 branches, 3 cities, 6 product categories |
| **Key Dimensions** | Customer, Product, Location, Payment & Time |
| **Key Metrics** | Sales, Quantity, Gross Income & Rating |

## 3. Tools
![tools](Images/tools.png)

## 4. Data Cleaning
Seluruh pembersihan data menggunakan Microsoft Excel, sehingga menghasilkan tabel-tabel bersih yang akan menjadi fondasi bagi analisis selanjutnya."

### 4.1 Strategi Pembersihan Data
  * Mengubah type data column unit price dan rating (Text to Numeric/Value) menggunakan formula 'Substitute' dan 'Value'.
  * Mengubah format Date menjadi MM/DD/YYYY menggunakan Text to Columns.
  * Melakukan recalculation pada kolom COGS berdasarkan Unit Price × Quantity
  * Menghitung kembali Tax 5% berdasarkan COGS × 5% karena ditemukan ketidaksesuaian pada sebagian nilai.
  * Menghitung kembali Sales/Total berdasarkan COGS + Tax 5%.
  * Menghitung kembali Gross Income berdasarkan Sales − COGS.
  * Menghitung kembali Gross Margin % berdasarkan Gross Income / Sales.
    
### 4.2 Audit Column
Melakukan data validation menggunakan pengecekan tipe data (ISNUMBER) untuk memastikan kolom numerik dan tanggal telah berhasil dikonversi.

![Data Cleaning](Images/unit-price.png) |![Data Cleaning](Images/cogs.png) | ![Data Cleaning](Images/tax.png) |![Data Cleaning](Images/sales.png)

## 5. Sales Performance Analysis & Metrics

### 5.1 Sales Performance Analysis
Analisis dilakukan berdasarkan beberapa dimensi bisnis yang tersedia dalam dataset, yaitu *product category*, *branch*,*city*, *customer type*, *gender*, *payment method*, dan *date*.

## 5.1 Sales Performance Analysis

Analisis dilakukan pada 6 dimensi bisnis, ditambah analisis waktu dan analisis silang untuk menjelaskan perubahan sales antar bulan.

| No | Dimension | Metric yang dianalisis | Tujuan |
|----|-----------|------------------------|--------|
| 1 | **Product Category** | Total Sales, Sales Contribution %, Quantity | Menilai kontribusi dan performa tiap kategori produk | 
| 2 | **Branch & City** | Total Sales, Sales Contribution %, Quantity, Avg Rating | Membandingkan performa dan pengalaman pelanggan antar lokasi |
| 3 | **Customer Type** | Total Sales, Transaction Count, Quantity, AOV | Membandingkan nilai transaksi Member vs Normal |
| 4 | **Gender** | Total Sales, Transaction Count, Quantity, AOV | Mengidentifikasi pola pembelian Female vs Male | 
| 5 | **Payment Method** | Transaction Count, Total Sales, Sales Contribution % | Memahami preferensi pembayaran dan kontribusinya |
| 6 | **Month** | Total Sales, Transaction Count, Quantity, MoM Growth % | Melihat perubahan sales antar bulan (Jan-Mar) | 
| 7 | **Hour** | Transaction Count, Total Sales, Sales Contribution % | Menemukan jam puncak transaksi |
| 8 | **Month × Customer Type / City** | Total Sales, Transaction Count, Selisih antar bulan | Menemukan dimensi yang berkontribusi pada perubahan sales |
---

### 5.2 Performance Metrics
Metrik utama yang digunakan dalam analisis ini meliputi:

* **Total Sales:** Total amount pendapatan dari seluruh transaksi penjualan.
* **Total Quantity:** Total unit produk yang berhasil terjual.
* **Gross Income:** Total keuntungan kotor yang diperoleh.
* **Gross Margin %:** Persentase margin keuntungan kotor terhadap total penjualan.
* **Average Customer Rating:** Rata-rata skor kepuasan pelanggan (skala 1–10).
* **Sales Contribution %:** Persentase kontribusi penjualan dari setiap segmen/kategori terhadap total pendapatan.

## 6. Key Findings

### 1. Sales Performance by Branch
* **Giza** mencatatkan *sales* tertinggi sebesar $ 110,57 K, sedangkan **Cairo** mencatat *sales* terendah sebesar $ 106,2 K. 
 Perbedaannya relatif kecil (stabil), sehingga secara keseluruhan performa penjualan antar cabang cukup merata.

### 2. Product Category Performance
* **Food And Beverages Menjadi Product Paling Banyak Terjual sebesar 952 Pcs dengan total Sales sebesar $ 56,14 K, sedangkan Health and beauty menjadi product paling sedikit terjual sebesar 854 Pcs dengan total sales sebesar $ 49,19 K.
**.
 > **Insight:** Terdapat perbedaan kontribusi antar kategori produk yang dapat dijadikan dasar dalam mengevaluasi strategi *product mix* dan alokasi stok.

### 3. Customer Segment
* **Member** menghasilkan *sales* sebesar $ 189,69 K (*volume* 3,181 unit), jauh lebih tinggi dibandingkan **Normal Customer** sebesar $ 133,27 K (*volume* 2,329 unit).
 > **Insight:** Segmen *Member* merupakan pendorong utama kontribusi penjualan bisnis.

### 4. Payment Behavior
* **Cash** menjadi metode pembayaran utama dengan *sales* tertinggi sebesar **$112,206.57**, diikuti oleh **Credit Card** sebesar **$100,767.07**.
 > **Insight:** Transaksi tunai (*Cash*) masih menjadi preferensi dominan pelanggan selama periode pengamatan.

### 5. Sales Trend (Monthly Performance)
* Penjualan tertinggi terjadi pada **Januari ($116,291.87)**, kemudian mengalami penurunan pada **Februari ($97,219.37)**, sebelum akhirnya bangkit kembali pada **Maret ($109,455.51)**.
 > **Insight:** Performa penjualan menunjukkan pola fluktuasi periodik, bukan tren penurunan yang konsisten secara jangka panjang.

### 6. Customer Experience (Rating)
* Rata-rata kepuasan pelanggan (*rating*) berada pada angka **7.0 / 10.0**. 
* **Giza** memiliki *rating* tertinggi (**7.1**), sedangkan **Cairo** mencatatkan *rating* terendah (**6.8**).
 > **Insight:** Variasi *rating* antar cabang relatif tipis, sehingga evaluasi pengalaman pelanggan perlu dipadukan dengan metrik volume penjualan untuk analisis lebih mendalam.
  
## 7. Dashboard
Project ini dirancang sebagai analisis end-to-end yang membentuk satu alur cerita, mulai dari identifikasi business problem, eksplorasi data, penemuan insight, hingga penyusunan dasar rekomendasi bisnis.

![Dashboard](Dashboard/dashboard-super.png)

## 8. Insight
1. Penjualan relatif merata antar kota (32,9-34,2%), produk (15,2-17,4%), dan metode pembayaran (31,2-34,7%), sehingga tidak ada satu dimensi yang terlalu dominan. Perbedaan paling jelas ada pada gender: Female menyumbang 60,3% total sales dan Male 39,7%. Dari sisi pembayaran, Cash memiliki sales tertinggi ($112,21K), sedangkan jumlah transaksi E-wallet dan Cash hampir sama (345 vs 344)
2.Naypyitaw dipertahankan karena sales ($110,57K) dan rating (7,1) tertinggi di antara kota lain. Yangon dan Mandalay memiliki potensi peningkatan. Yangon mencatat unit terjual tertinggi (1.859 pcs) tetapi total sales lebih rendah dan sales-nya paling fluktuatif antar bulan. Mandalay memiliki rating terendah (6,8) dibanding kota lainnya.
3. Sales turun 16,4% dari Januari ke Februari ($116,29K → $97,22K), lalu pulih 12,6% di Maret tetapi masih 5,9% di bawah Januari. Penurunan Februari terutama didorong oleh jumlah transaksi yang turun (352 → 303), dengan kontribusi terbesar dari pelanggan Normal (64% dari total penurunan). Dari sisi kota, Yangon dan Naypyitaw menyumbang sekitar 85% penurunan tersebut. Dari sisi produk, penurunan terbesar terjadi pada kategori Sports and travel & Home and lifestyle.
4. Member cenderung membeli dengan quantity (5,63 vs 5,35 pcs per transaksi) dan nominal (rata-rata $336 vs $306 per transaksi) lebih besar daripada pelanggan Normal, meskipun selisih nominalnya bervariasi antar bulan. Dari sisi waktu, pembelian memuncak pada pukul 19:00 (12,3% sales), disusul pukul 13:00 dan 15:00. Karena dataset tidak memiliki customer ID, temuan ini menunjukkan korelasi dan belum membuktikan bahwa membership yang menyebabkan belanja lebih besar.

## 9. Recommendations
1. Fokus pada segmen pelanggan karena perbedaannya paling nyata. Naikkan nilai belanja Male (sekitar $299 vs $341 Female) lewat promo bundling.
2. Jadikan Naypyitaw acuan untuk kota lain. Dorong upselling di Yangon agar nilai per unit naik, dan evaluasi layanan di Mandalay untuk memperbaiki rating (6,8) serta AOV-nya.
3. Buat promo awal Februari yang menyasar pelanggan Normal, dan pantau jumlah transaksi mingguan sebagai indikator dini.
4. Dorong konversi Normal menjadi Member di kasir, dan siapkan staf serta stok lebih banyak pada jam puncak 19:00.

## 7. Limitations & Methodology Notes

> **Catatan Metodologi & Keterbatasan Data:**
> Beberapa batasan dan konteks metodologi yang perlu diperhatikan dalam menginterpretasikan hasil analisis proyek ini.

* **Cakupan Data Terbatas:** Dataset terbatas pada **1.000 transaksi** dalam rentang waktu Januari hingga Maret 2019.
* **Ketiadaan *Customer ID*:** Tidak terdapat variabel *Customer ID* unik, sehingga analisis tingkat individu seperti **RFM, Customer Lifetime Value (CLV), Churn, dan Retention** tidak dapat dilakukan.
* **Korelasi Lokasi:** Variabel *Branch* (Cabang) dan *City* (Kota) memiliki hubungan *1-to-1* (saling berpasangan secara identik) dalam dataset ini.
* **Sifat Analisis:** Temuan analisis ini bersifat **deskriptif dan diagnostik** (*descriptive/diagnostic*), bukan menunjukkan hubungan sebab-akibat (*causal relationship*).
* **Ketersediaan Data Operasional:** Tidak tersedia data pendukung seperti *inventory/stok*, biaya promosi, biaya pemasaran (*marketing cost*), maupun biaya operasional (*operational cost*).
* **Penggunaan *Customer Rating*:** Indikator *Customer Rating* digunakan hanya sebagai **indikator pendukung** (*supporting indicator*), bukan sebagai pemicu utama (*causal driver*) dari penjualan.

Dataset  : https://www.kaggle.com/datasets/faresashraf1001/supermarket-sales
Microsoft Excel  :
EDA      : 
Dashboard  :
