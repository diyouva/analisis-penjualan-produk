# analisis-penjualan-produk
Data Wrangling and SQL — Analisis Penjualan Produk
https://diyouva.medium.com/data-wrangling-and-sql-analisis-penjualan-produk-837e510a24aa

Menganalisis kinerja penjualan dan mengidentifikasi produk unggulan menjadi salah satu cara yang dapat dilakukan untuk mengoptimalkan profit pada produk-produk yang lebih profitable bagi perusahaan.

Tujuan dari analisis ini terbagi menjadi 3:

Menentukan 5 item penjualan terbesar (berdasarkan total harga, jumlah item diorder, negara pembeli dan negara penjual)
Menentukan seller penjualan terbesar per kota/negara
Menentukan customer pembelian terbesar untuk mendapatnya program prioritas

Data yang digunakan:
order_id: order unique identifier
order_item_id: sequential number identifying number of items included in the same order
product_id: unique product identifier
product_category_name: root category of product (in english)
price: item price
freight_value: item freight value item (if an order has more than one item the freight value is splitted between items)
customers_id: key to the orders dataset. each order has a unique customer_id
customer_city: customer city name
customer_state: customer state
seller_id: seller unique identifier
seller_city: seller city name
seller_state: seller state

# Eksplorasi dan Pemrosesan Data
Memeriksa nilai NaN pada Dataset melalui method info() dan
data.isnull().sum().sort_values(ascending=False)/len(data)*100
tidak terdapat nilai NaN

Setelah memeriksa nilai NaN, dilakukan pengecekan outlier pada data price dan freight_value yang bertipe data numerik.

penghapusan data outlier dilakukan dengan menghitung quartile atas dan quartile bawah pada data freight_value dan data price,
setelah itu data outlier didrop dari dataset.

Dalam mengeksplor data duplikat, tidak terdapat duplikasi data pada dataset.

# Analisis Data
Setelah mengeksplorasi dan pemrosesan data, analisis dimulai dengan menentukan 5 item penjualan terbesar
Analisis lebih lanjut dilanjutkan untuk melihat performa seller untuk mendapatkan penghargaan atau apresiasi.
Identifikasi customer untuk mengenali customer lebih baik dan menjalin hubungan baik dengan pelanggan setia dengan memberikan program prioritas pelanggan setia
