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
