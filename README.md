# Supermarket Sales Dataset | Microsoft-Excel
  "Project analitis end-to-end menggunakan Excel untuk menganalisis pola penjualan berdasarkan produk, segmen pelanggan, lokasi, metode pembayaran, dan periode waktu guna mengidentifikasi perbedaan performa penjualan serta area yang perlu diperhatikan dalam pengambilan keputusan bisnis."

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
Perusahaan perlu memahami pola dan variasi performa penjualan berdasarkan produk, pelanggan, lokasi, metode pembayaran, dan waktu untuk mengidentifikasi segmen yang berkontribusi besar serta area yang perlu diperhatikan.

### 1.3 Project Objectives
Menganalisis pola penjualan berdasarkan produk, pelanggan, lokasi, metode pembayaran, dan waktu untuk mengidentifikasi kontribusi setiap segmen serta menghasilkan insight yang mendukung pengambilan keputusan bisnis.

### 1.4 Business Questions
* Apakah terdapat perbedaan pola penjualan berdasarkan segmen pelanggan, produk, lokasi, dan metode pembayaran?
* Area mana yang perlu dipertahankan dan area yang memiliki potensi peningkatan?
* Apa penyebab perubahan sales antar periode?
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


## 4. Data Cleaning
Seluruh pembersihan data menggunakan Microsoft Excel, sehingga menghasilkan tabel-tabel bersih yang akan menjadi fondasi bagi analisis selanjutnya."

### 4.1 Strategi Pembersihan Data (*Cleaning Strategy*)
  * Mengubah type data column unit price dan rating (Text to Numeric/Value) menggunakan formula 'Substitute' dan 'Value'.
  * Mengubah format Date menjadi MM/DD/YYYY menggunakan Text to Columns.
  * Melakukan recalculation pada kolom COGS berdasarkan Unit Price × Quantity
  * Menghitung kembali Tax 5% berdasarkan COGS × 5% karena ditemukan ketidaksesuaian pada sebagian nilai.
  * Menghitung kembali Sales/Total berdasarkan COGS + Tax 5%.
  * Menghitung kembali Gross Income berdasarkan Sales − COGS.
  * Menghitung kembali Gross Margin % berdasarkan Gross Income / Sales.
    
### 4.2 Audit Column is_clean
Melakukan data validation menggunakan pengecekan tipe data (ISNUMBER) untuk memastikan kolom numerik dan tanggal telah berhasil dikonversi.

## 5. Sales Performance Analysis & Metrics

### 5.1 Sales Performance Analysis
Analisis dilakukan berdasarkan beberapa dimensi bisnis yang tersedia dalam dataset, yaitu *product category*, *branch*, *customer type*, *gender*, *payment method*, dan *month*.

## 5.1 Sales Performance Analysis

Analisis dilakukan berdasarkan beberapa dimensi dan metrik bisnis yang tersedia dalam dataset untuk mengidentifikasi pola serta performa penjualan.

| Dimension | Metric yang dianalisis | Tujuan |
| :--- | :--- | :--- |
| **Product Category** | Total Sales, Sales Contribution %, Quantity, Gross Income | Menilai kontribusi dan performa tiap kategori produk |
| **Branch / City** | Total Sales, Average Transaction Value, Quantity, Rating | Membandingkan performa dan *customer experience* antar lokasi |
| **Customer Type** | Total Sales, Sales Contribution %, Avg. Transaction Value, Quantity | Memahami kontribusi dan nilai transaksi Member vs Normal |
| **Gender** | Total Sales, Quantity, Avg. Transaction Value | Mengidentifikasi pola pembelian berdasarkan gender |
| **Payment Method** | Transaction Count, Total Sales, Sales Contribution % | Memahami preferensi pembayaran dan kontribusinya terhadap transaksi |
| **Month** | Total Sales, MoM Growth %, Quantity, Average Transaction Value | Mengidentifikasi perubahan dan fluktuasi performa penjualan |
| **Product Category × Customer Type** | Sales, Quantity, Avg. Transaction Value | Menemukan kombinasi produk dan segmen pelanggan yang potensial |
| **Product Category × Branch** | Sales, Sales Contribution %, Quantity | Mengidentifikasi kategori yang kuat/lemah di setiap cabang |

---

### 5.2 Performance Metrics
Metrik utama yang digunakan dalam analisis ini meliputi:

* **Total Sales:** Total amount pendapatan dari seluruh transaksi penjualan.
* **Total Quantity:** Total unit produk yang berhasil terjual.
* **Average Transaction Value (ATV):** Rata-rata rating per transaksi.
* **Gross Income:** Total keuntungan kotor yang diperoleh.
* **Gross Margin %:** Persentase margin keuntungan kotor terhadap total penjualan.
* **Average Customer Rating:** Rata-rata skor kepuasan pelanggan (skala 1–10).
* **Sales Contribution %:** Persentase kontribusi penjualan dari setiap segmen/kategori terhadap total pendapatan.

### 5.4 Table analisa Final

| Analytical Table | Digunakan untuk |
| :--- | :--- |
| **sales_performance_summary** | Overall business performance |
| **product_category_summary** | Product performance |
| **branch_performance_summary** | Branch comparison |
| **customer_segment_summary** | Member vs Normal analysis |
| **monthly_sales_summary** | Sales trend analysis |

## 6. Key Findings

### 1. Sales Performance by Branch
* **Giza** mencatatkan *sales* tertinggi sebesar **$110,568.71**, sedangkan **Cairo** mencatat *sales* terendah sebesar **$106,197.67**. 
 Perbedaannya relatif kecil (stabil), sehingga secara keseluruhan performa penjualan antar cabang cukup merata.

### 2. Product Category Performance
* **Food & Beverages** menghasilkan *sales* tertinggi sebesar **$56,144.84**, sementara **Health & Beauty** mencatatkan *sales* terendah sebesar **$49,193.74**.
 > **Insight:** Terdapat perbedaan kontribusi antar kategori produk yang dapat dijadikan dasar dalam mengevaluasi strategi *product mix* dan alokasi stok.

### 3. Customer Segment
* **Member** menghasilkan *sales* sebesar **$189,694.76** (*volume* 3,181 unit), jauh lebih tinggi dibandingkan **Normal Customer** sebesar **$133,271.99** (*volume* 2,329 unit).
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

## 8. Insight

## 9. Recommendations


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
