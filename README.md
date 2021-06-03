
# Final Project : Hotel Booking Cancellation Prediction

by : Pandas Team
- Fardhina Amalia
- Harry Kurniansyah
- Rafif Abdul Aziz

Dataset : hotel_bookings.csv

<hr>

## Background

Pada Project kali ini kami berperan sebagai tim Data Scientist untuk sebuah hotel di negara Portugal. sebagai Data Scientist, kami diminta untuk membuat sebuah model Machine Learning yang dapat memprediksi kemungkinan customer yang akan melakukan cancel. Model ini nantinya akan digunakan oleh tim management dalam menentukan budget planning dan juga digunakan untuk meningkatkan revenue yang didapat dari jumlah reservasi. 

## Problem 
- Setiap hotel memiliki target penjualan setiap bulannya yang telah ditentukan oleh tim management hotel. Target ini dibuat menggunakan budget planning sebagai strategi agar tim management dapat mencapai target yang telah ditentukan. Tim management hotel melakukan budget planning based on revenue setiap priode, revenue yang didapatkan berdasarkan dari jumlah reservasi kamar pada bulan itu. Budget planning tersebut menjadi landasan bagi management hotel untuk merencanakan strategi penjualan hotel agar mencapai target. Sehingga ketepatan memeperkirakan jumlah reservasi yang cancel booking dapat mempengaruhi keuntungan pada bulan itu. Sehingga model prediksi cancellation booking hotel ini dapat memberikan impact kepada tim management yaitu bisa memperkirakan budget planning hotel pada bulan itu dengan lebih tepat.

- Model prediksi cancellation booking hotel ini dapat memberikan impact kepada tim management yaitu bisa memperkirakan budget planning hotel pada bulan itu dan mengetahui customer/reservation mana yang akan cancel, sehingga tim marketing/sales dapat memberikan treatment khusus kepada customer yang diprediksi berpotensi cancel dan tentu saja hal ini dilakukan untuk dapat memaksimalkan revenue hotel.


## Goals 
Goal yang ingin dicapai pada Project ini yaitu :

- Membangun Model Prediction Cancellation Booking Hotel. 
- Memaksimalkan revenue.
- Mengefisiensikan budget planning.

## Dataset

Dataset Diambil Dari: https://www.kaggle.com/jessemostipak/hotel-booking-demand

## Acknowledgements

Data ini ditulis dan disusun oleh Nuno Antonio, Ana Almeida, and Luis Nunes pada artikel Data in Brief, Volume 22, February 2019.
site : https://www.sciencedirect.com/science/article/pii/S2352340918315191#bib5

Lokasi pengambilan data : Kedua hotel berlokasi di Portugal, Hotel pertama berada di kawasan resort Algarve dan Hotel kedua berada di Kota Lisbon

<hr>

## Data Cleaning dan Exploratory Data Analysis
Hal pertama yang dilakukan yaitu melakukan import Dataset dan package yang akan digunakan untuk Expolatory Data Analysis, 
kemudian melakukan deskripsi data dan melakukan handling terhadap outliers dan Missing Value. Proses ini akan menghasilkan dataset baru yang sudah bersih dan siap digunakan untuk proses berikutnya yaitu EDA dan Modelling.
Eksploratory Data Analysis dilakukan menggunakan crosstab dan groupby serta plot untuk menampilkan visualisasi data untuk mendapatkan insight dari data.

<hr>

## Data Preparation
Pada proses ini kami melakukan Features Engineering dengan melakukan Label Encoding dan One Hot Encoding pada kolom kategorik dan merubahnya menjadi numerik, kemudian kami melihat Correlation untuk melakukan Feature Selection dan melakukan drop kolom yang dinilai memiliki korelasi yang rendah terhadap kolom target sesuai kebutuhan modelling.

<hr>

## Modelling
Sebelum melakukan modelling, kami melakukan split dataset untuk membagi dataset menjadi Data Train dan Test, kemudian kami menentukan beberapa base model pertama. Kami memilih 3 model untuk dijadikan Base model yaitu:
- Random Forest Regression
- Decision Tree Regression
- XGBoost Regresion

Masing-masing Base Model yang telah dicoba kemudian masuk ke proses Imporvement dengan menggunakan dua metode yaitu Polynomial dan Hyperparameter Tuning untuk meningkatkan score agar mendapat score yang lebih baik.

## Evaluation
Setelah melakukan Polynomial dan Hyperparameter Tuning, dilakukan Evaluation dengan membandingkan nilai Accuracy dari masing-masing model untuk memilih model yang terbaik.

![AccuracyScore](https://user-images.githubusercontent.com/79127874/120594740-94af6700-c46b-11eb-9ebc-f5a3f7ac6df9.png)


## Model Recommendation
Berdasarkan hasil Evaluasi, model yang kami pilih sebagai rekomendasi adalah model XGB_tuned yang telah melalui proses Hyperparameter Tuning, karena model ini memiliki nilai Evaluation Matrix yang paling baik dibanding model yang lain. Parameter awal yang kami tentukan untuk model XGB adalah : 

![param](https://user-images.githubusercontent.com/79127874/120598154-1ef9ca00-c470-11eb-86f2-3bdf8b3a40ac.png)

kemudian kami melakukan Random Search untuk mendapatkan parameter terbaik dari Parameter yang telah kami tentukan sebelumnya dan diperoleh parameter terbaik 
```
- best.params: 'n_estimators' : 500, 'max_depth' : 10, 'learning_rate' : 0.1, 'gamma' : 0.1
```
Setelah melakukan Tuned terhadap model XGB dengan parameter terbaik yang telah didapatkan, diperoleh Evaluation Matrix sebagai berikut.
![XGB](https://user-images.githubusercontent.com/79127874/120597948-e2c66980-c46f-11eb-83df-44b23a6cf6ee.png)



