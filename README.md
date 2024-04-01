# **Amazing Web Services's SaaS Sales**

![aws_logo_smile_1200x630](https://github.com/valeriatrisna/AWS-SaaS-Sales-Capstone-2/assets/160201503/67d12361-ab5b-40de-a51c-89852b92cd6a)

# Table of Content
* Business Problem [#Business Problem]
* Data Understanding and Preparation
* Explanatory Data Analysis

    
## Business Problem
AWS atau yang dikenal sebagai Amazon Web Services merupakan platform komputasi awan yang disediakan oleh Amazon.com. AWS menawarkan berbagai layanan komputasi, penyimpanan, jaringan, basis data, analitik, kecerdasan buatan (AI), Internet of Things (IoT), pengembangan aplikasi, keamanan, dan berbagai layanan lainnya untuk membantu organisasi mengembangkan dan menjalankan aplikasi mereka dengan lebih efisien dan fleksibilitas di lingkungan komputasi awan.

AWS memiliki banyak keunggulan, termasuk skalabilitas, keamanan, ketersediaan, dan fleksibilitas. Platform ini telah menjadi pemimpin pasar dalam komputasi awan dan menyediakan infrastruktur yang mendasari bagi banyak bisnis dan aplikasi online yang kita gunakan setiap hari. 

Dalam project ini, terdapat rekap penjualan SaaS selama th 2020 sd th 2023 yang berisikan informasi Product yang dijual, Customer yang melakukan transaksi, Sales dari Product berikut juga Profit yang diperoleh. Sekilas, penjualan SaaS dari tahun ke tahun meningkat, baik itu secara nominal dan juga quantity produk yang terjual. 

Seperti yang kita ketahui bahwa dalam bisnis retail ada 2 variabel yang memengaruhi Sales, yaitu Price & Quantity. Semakin tinggi Price maka semakin tinggi Sales yang akan diperoleh, dan semakin tinggi Quantity yang kita jual maka semakin tinggi juga Sales yang kita peroleh. Namun apabila kita hanya berfokus pada menignkatkan Price, kita bisa saja kehilangan customer loyal kita yang akan berpindah ke kompetitor kita, sedangkan apabila kita berfokus pada meningkatkan Quantity artinya kita memperkuat dan mempeluas customer kita.

Selanjutnya kita perlu meneliti lebih lanjut, Produk apa aja yang dapat dioptimalkan penjualannya dan bagaimana pengaruh quantity terhadap Sales & Profit yang akan diperoleh perusahaan. Hal itu akan membantu perusahaan untuk mengambil keputusan dan langkah kedepannya untuk menentukan program dan promosi yang tepat.

Dari pernyataan tersebut, dapat dirumuskan pertanyaan-pertanyaan lanjutan yang lebih rinci sebagai berikut:
1.   Bagaimana tren penjualan dari AWS dari sisi Sales, Profit, dan Quantity dari tahun ke tahun? 
2.   Bagaimana hubungan antara Produk yang diberikan diskon dengan quantity yang terjual dan profit yang dihasilkan?
3.   Apa strategi yang tepat untuk program pemasaran AWS?
3.   Produk apa sajakah yang dapat dioptimalkan untuk dijual dan dipromosikan lebih lanjut?
5.   Bagaimana pengaruh peningkatan quantity produk tertentu terhadap Sales & Profit Perusahaan?

## Data Understanding and Preparation
Dataset SaaS Sales ini dapat diakses melalui [disini](https://www.kaggle.com/datasets/nnthanh101/aws-saas-sales).
Dataset ini berisi informasi terkait aktivitas penjualan layanan software selama tahun 2020 sd th 2023. Ada 18 kolom di dalam dataset AWS SaaS Sales, yaitu:  

1. `Order ID`: Kode unik yang berbeda di setiap transaski.
2. `Order Date`: Tanggal ketika transaski dilakukan. 
3. `Date Key`: Angka yang merepresentasikan tanggal transaksi (YYYYMMDD). 
4. `Contact Name`: Contact Person (PIC) dari yang melakukan transaksi.
5. `Country`: Negara asal dari Perusahaan yang melakukan transaksi. 
6. `City`: Kota asal dari Perusahaan yang melakukan transaksi. 
7. `Region`: Wilayah dari Negara yang melakukan transaksi. 
8. `Subregion`: sub-Wilayah dari Negara yang melakukan transaksi.
9. `Customer`: Nama Perusahaan yang melakukan transaksi. 
10. `Customer ID`: Kode unik dari Customer. 
11. `Industry`: Industri dari Perusahaan. 
12. `Segment`: Segmen Perusahaan dari Customer (`SMB = Small, Medium Business (UMK)`, `Enterprise`, `Strategic`).
13. `Product`: Product yang dibeli. 
14. `License`: Kode lisensi dari produk. 
15. `Sales`: Jumlah total penjualan dari transaksi. 
16. `Quantity`:  Jumlah item kuantitas dari transaksi. 
17. `Discount`: Diskon yang diberikan pada transaksi.
18. `Profit`: Keuntungan yang diperoleh dari transaksi. 

Dalam data understanding dan preparation, kita melakukan sebagai berikut: 
1. Pengecakan Missing Values -> dalam dataset ini tidak ada missing values sehingga tidak diperlukan adanya data manipulation.
2. Numerik Understanding -> melakukan stastika deskriptif untuk mengetahui mean, nilai min & max, melihat distribusi data, mengecek outliers dan juga melihat menghitung korelasi antar kolom numerik.
3. Kategorik Undestading -> menghitung jumlah unique values dari kolom kategorik, dan melihat modus dari masing-masing kolom.
4. Data Cleaning -> melakukan perubahan tipe data pada kolom Order Date menjadi datetime, dan melihat kembali outliers dari data tersebut bersifat anomali atau tidak.  
