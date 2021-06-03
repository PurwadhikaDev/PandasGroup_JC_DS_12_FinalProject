
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

The data is originally from the article https://www.sciencedirect.com/science/article/pii/S2352340918315191#bib5 Hotel Booking Demand Datasets, written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019.

Data source location : Both hotels are located in Portugal: H1 at the resort region of Algarve and H2 at the city of Lisbon

<hr>

## Data Cleaning dan Exploratory Data Analysis
Hal pertama yang dilakukan yaitu melakukan import Dataset dan package yang akan digunakan untuk Expolatory Data Analysis dan Modellig, 
kemudian melakukan deskripsi data kemudian melakukan handling terhadap outliers dan Missing Value.
Eksploratory Data Analysis dilakukan menggunakan crosstab dan groupby serta plot untuk menampilkan visualisasi data untuk mendapatkan insight dari data.

<hr>

## Data Preparation
Pada proses ini kami melakukan Features Engineering dengan melakukan Encoding, Adding Features dan Recategorize serta melihat correlation untuk melakukan Feature Selection sesuai kebutuhan modelling.

<hr>

## Modelling
Sebelum melakukan modelling, kami melakukan split dataset untuk membagi dataset menjadi Data Train dan Test, kemudian kami menentukan beberapa base model pertama. Kami memilih 3 model untuk dijadikan Base model yaitu:
- Random Forest Regression
- Decision Tree Regression
- XGBoost Regresion

Base Model yang telah dicoba kemudian diImprove dengan Polynomial dan Hyperparameter tuning untuk meningkatkan score agar mendapat score yang lebih baik.

## Evaluation
Setelah melakukan Hyperparameter Tuning, dilakukan Evaluation dengan membandingkan nilai Accuracy dari masing-masing model untuk memilih model yang terbaik.

![AccuracyScore](https://user-images.githubusercontent.com/79127874/120586898-94f53580-c45e-11eb-8cb4-dd14ae8a1e56.png)

## Model Recommendation
Berdasarkan hasil Evaluasi, model yang kami pilih sebagai rekomendasi adalah model XGB_tuned yang telah melalui proses Polynomial dan Hyperparameter Tuning.

