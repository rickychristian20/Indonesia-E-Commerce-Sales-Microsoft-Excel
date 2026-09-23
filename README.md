# Supermarket Sales Dataset | Microsoft-Excel
  "Project analitis end-to-end menggunakan Excel untuk menganalisis pola penjualan berdasarkan produk, segmen pelanggan, lokasi, metode pembayaran, dan periode waktu guna mengidentifikasi perbedaan performa penjualan serta area yang perlu diperhatikan dalam pengambilan keputusan bisnis."

Table Of Contents
1. Business Understanding
2. Data Source
3. Tool 
4. Data Cleaning
5. Data Extraction & Feature Engineering
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

## 3. Environment & Tech Stack

```mermaid
graph LR
    A[1. RAW DATA<br><b>Kaggle Dataset</b><br><i>Supermarket Sales Data</i>] --> B[2. DATA CLEANING<br><b>Microsoft Excel</b><br><i>Power Query & Data Prep</i>]
    B --> C[3. DATA ANALYSIS<br><b>Microsoft Excel</b><br><i>Pivot Tables & Formulas</i>]
    C --> D[4. DASHBOARD<br><b>Microsoft Excel</b><br><i>Interactive Charts & Slicers</i>]
    D --> E[5. INSIGHT & ACTION<br><b>Final Output</b><br><i>Strategic Recommendations</i>]
