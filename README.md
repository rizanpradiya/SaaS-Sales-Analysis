
## Ringkasan
Proyek ini menganalisis data penjualan SaaS untuk menilai kinerja sales dan profit di berbagai wilayah serta lini produk, sekaligus mengevaluasi dampak diskon terhadap profit margin pada level transaksi.

## Tujuan
Memberikan insight yang dapat ditindaklanjuti bagi perusahaan SaaS untuk mengoptimalkan strategi penjualan dan diskon, meningkatkan profitabilitas, serta memprioritaskan wilayah, produk, dan segmen pelanggan yang berkinerja tinggi melalui rekomendasi berbasis data.

## Pernyataan Masalah
Perusahaan ingin mendapatkan gambaran yang lebih jelas mengenai kinerja penjualan dan profit di berbagai wilayah serta lini produk, sekaligus memahami bagaimana diskon berperan dalam membentuk profit margin.

Sebagai seorang data analyst, kita akan mencoba menjawab pertanyaan berikut:
- Wilayah/region mana yang memberikan kontribusi penjualan dan profit tertinggi?
- Produk mana yang paling laris dan paling menguntungkan?
- Margin profit mana antar segmen yang paling menguntungkan?

## Dataset
- **Dataset Awal**: SaaS-Sales.csv
- **Dataset yang sudah bersih**: Clean-Saas-Sales.xlsx

**Key Features**

| Feature        | Description                                              | dtypes   |
| -------------- | -------------------------------------------------------- | -------- |
| `Row ID`       | A unique identifier for each transaction.                | int      |
| `Order ID`     | A unique identifier for each order.                      | str      |
| `Order Date`   | The date when the order was placed.                      | datetime |
| `Date Key`     | A numerical representation of the order date (YYYYMMDD). | int      |
| `Contact Name` | The name of the person who placed the order.             | str      |
| `Country`      | The country where the order was placed.                  | str      |
| `City`         | The city where the order was placed.                     | str      |
| `Region`       | The region where the order was placed.                   | str      |
| `Subregion`    | The subregion where the order was placed.                | str      |
| `Customer`     | The name of the company that placed the order.           | str      |
| `Customer ID`  | A unique identifier for each customer.                   | int      |
| `Industry`     | The industry the customer belongs to.                    | str      |
| `Segment`      | The customer segment (SMB, Strategic, Enterprise, etc.). | str      |
| `Product`      | The product was ordered.                                 | str      |
| `License`      | The license key for the product.                         | str      |
| `Sales`        | The total sales amount for the transaction.              | float    |
| `Quantity`     | The total number of items in the transaction.            | int      |
| `Discount`     | The discount applied to the transaction.                 | float    |
| `Profit`       | The profit earned from the transaction.                  | float    |


## Struktur Proyek
SaaS-Sales-Analysis/
│
├── README.md
├── SaaS-Sales Analysis_Rizan Pradiya.ipynb   # Notebook analisis
├── SaaS_Sales_Raw.csv                        # Dataset mentah
├── SaaS_Sales_Clean.csv                      # Dataset bersih
├── SaaS_Sales_Discount_Analysis.twbx         # Tableau
└── Capstone_Module2_Presentation.pptx        # Slide presentasi

## Kesimpulan
1. **Kinerja Regional & Subregional**  
   `EMEA` menjadi penyumbang sales dan profit terbesar, sedangkan `AMER` memiliki profit margin paling tinggi (22%).  
   `APJ` masih menjadi titik lemah karena mencatat margin negatif (–15%), terutama dari `JAPN` dan `ANZ` yang merugi.

2. **Kinerja Produk**  
   Produk terlaris belum tentu paling untung. `ContactMatcher` mencatat sales tertinggi tetapi margin sangat tipis (3%).  
   Profit utama datang dari produk bermargin tinggi seperti `Alchemy`, `Data Smasher`, `Support`, dan `Site Analytics`.  
   `Marketing Suite` justru merugi.

3. **Segmentasi Profit**  
   `SMB` mendominasi Sales dan Profit, tetapi margin paling rendah; sementara `Enterprise` punya margin tertinggi meski volumenya kecil, dan `Strategic` berada di posisi tengah yang stabil.

## Rekomendasi
1. **Perbaiki performa APJ terlebih dahulu**  
   Fokus evaluasi pada `JAPN` dan `ANZ` sebagai subregion penyebab kerugian.  
   Review pricing, aturan diskon, dan efisiensi biaya.

2. **Maksimalkan produk bermargin tinggi**  
   Prioritaskan promosi untuk `Alchemy`, `Data Smasher`, `Support`, dan `Site Analytics` karena kontribusi profitnya paling kuat.

3. **Strategi segmen**  
   Fokuskan strategi ganda: pertahankan volume `SMB` dengan kontrol diskon ketat, sambil mendorong pertumbuhan di `Enterprise` karena marginnya paling sehat (dengan `Strategic` sebagai target ekspansi moderat).

