# Customer Shopping Behavior Analysis

Proyek ini menganalisis perilaku belanja pelanggan menggunakan data transaksi sebanyak 3.900 pembelian dari berbagai kategori produk. Tujuan utama proyek ini adalah mengidentifikasi pola belanja, segmen pelanggan, preferensi produk, serta perilaku pelanggan lain yang dapat membantu pengambilan keputusan strategis bisnis.

## Ringkasan Dataset

- Rows: 3,900
- Columns: 18
- Fitur Utama:
  - Demografi Pelanggan: Usia, Jenis Kelamin, Lokasi, Status Langganan
  - Detail Pembelian: Produk, Kategori, Jumlah Pembelian, Musim, Ukuran, Warna
  - Perilaku Belanja: Diskon, Kode Promo, Frekuensi Pembelian, Rating, Jenis Pengiriman
- Data Missing: 37 nilai hilang pada kolom Review Rating

## Proses Analisis

1. Exploratory Data Analysis (EDA) menggunakan Python
- Loading dataset menggunakan pandas
- Pemeriksaan struktur data dengan .info() dan .describe()
- Visualisasi awal distribusi umur, jumlah pembelian, dan pola rating
2. Data Cleaning
- Imputasi nilai hilang pada Review Rating menggunakan median per kategori produk
- Standarisasi nama kolom menjadi format snake_case
- Pengecekan konsistensi antara discount_applied dan promo_code_used
3. Feature Engineering
- Pembuatan fitur baru:
  - age_group berdasarkan rentang usia
  - purchase_frequency_days berdasarkan riwayat pembelian
- Penghapusan kolom yang tidak relevan setelah validasi
4. Integrasi ke PostgreSQL
- Mengunggah data yang sudah dibersihkan ke database PostgreSQL
- Melakukan query berbasis kebutuhan bisnis

## Analisis Menggunakan SQL (Business Transactions)

Berikut ringkasan analisis utama yang dilakukan:
1. Pendapatan Berdasarkan Gender – Mengukur total revenue dari pria vs wanita
2. High-Spending Discount Users – Mencari pelanggan yang tetap berbelanja tinggi meski menggunakan diskon
3. Top 5 Produk Berdasarkan Rating
4. Perbandingan Jenis Pengiriman – Standar vs Ekspres
5. Customer Subscription Analysis – Pengeluaran pelanggan berlangganan vs tidak
6. Top Discount-Dependent Products
7. Customer Segmentation (New, Returning, Loyal)
8. Top 3 Produk per Kategori
9. Repeat Buyers & Subscription Behavior
10. Revenue per Age Group

## Dashboard Power BI

Dashboard interaktif dibuat untuk menampilkan insight berikut:
- Total pelanggan, rata-rata pembelian, dan rating rata-rata
- Komposisi pelanggan berdasarkan status langganan
- Revenue by Category
- Sales by Category
- Revenue by Age Group
- Sales by Age Group

## Business Recommendations
- Boost Subscriptions – Tawarkan manfaat eksklusif untuk meningkatkan jumlah pelanggan berlangganan
- Customer Loyalty Programs – Berikan insentif bagi pembeli berulang untuk naik ke segmen Loyal
- Review Discount Policy – Optimalkan margin tanpa menurunkan penjualan
- Product Positioning – Fokuskan promosi pada produk terlaris & rating tinggi
- Targeted Marketing – Prioritaskan segmen usia dengan pendapatan tertinggi dan pengguna Express Shipping

## Tech Stack
- Python: Pandas, NumPy
- SQL: PostgreSQL
- Visualization: Power BI
- Tools: Jupyter Notebook  

## Key Outcomes
- Berhasil mengolah dan menganalisis 3.900+ transaksi
- Menghasilkan 10+ insight bisnis berbasis SQL
- Membuat dashboard interaktif untuk kebutuhan decision-making
- Menghasilkan rekomendasi strategis berbasis data
