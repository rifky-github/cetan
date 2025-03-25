
![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)


# CeTan (Cek Tanah)
<div align="center">
  <img src="https://github.com/user-attachments/assets/e3d7904d-a01a-4972-bfbd-51f6cc200ff4" width="500">
</div>

Sebuah alat yang bisa mengukur kadar tanah dengan bantuan sensor NPK (Nitrogen, Potassium, Kalsium), sensor pH, dan sensor Kelembaban Tanah. Alat ini sangat bagus untuk para petani yang ingin meningkatkan kesuburan tanamannya


## 📐 Perancangan Sistem
![Logo](https://github.com/user-attachments/assets/dd4b391e-3c64-4203-9d11-49a948023c6a)

Sistem kerja alat ini didasari oleh modul ESP32 yang berfungsi sebagai mikrokontroler yang dilengkapi modul Wi-Fi. Modul ESP32 ini menggunakan koneksi Wi-Fi untuk mengkomunikasikan antara Sensor dan Monitor. Sensor Tanah seperti Sensor Temperatur dan Kelembapan Tanah, Sensor pH Tanah, Sensor NPK Tanah, dimasukkan ke dalam tanah kemudian sensor-sensor tersebut akan membaca kandungan mineral tanah dan kondisi tanah (NPK, Kelembapan Tanah dan pH Tanah), kemudian data kandungan mineral tanah dan kondisi tanah dikirim ke Monitor lewat mikrokontroler ESP32. Monitor memunculkan data yang telah dikirim dari Sensor.

## ✨ 3D Design
<gambar></gambar>
Alat ini didesain sedemikian rupa untuk melindungi komponen elektronikanya dengan spesifikasi tahan terhadap suhu dan kelembaban untuk bisa menggunakan alat ini di mana saja. Terdapat layar dengan berteknologi e-ink yang berguna untuk bisa membaca hasil sensor walaupun diterjang silau matahari. 


# 🖥️ Monitor

Gambar 14 Desain 3D Alat Monitor 

 

Alat monitor ini dilengkapi dengan fitur penggenggam tangan supaya tangan tidak kelelahan pada saat menggunakan alat monitor ini. Terdapat tombol navigasi dan enter yang berguna untuk memilih menu yang ada di layar e-ink ini. Alat ini juga dilengkapi PCB didalamnya yang berguna untuk saling komunikasi antara alat monitor dan alat sensor. Alat ini juga dilengkapi saklar yang berada di samping kanan yang berguna untuk menghidupkan monitor ini.

..gambar skematik..

Gambar di atas ini adalah skematik dari PCB alat monitor. Module yang digunakan pada PCB ini adalah TP4056, MAX17048, XL6009 dan ESP32. TP4056 ini berguna untuk charge baterai yang ada di PCB ini. Baterai yang digunakan adalah Baterai Molicel P42A dengan spesifikasi 3.7 volt dan 4200 mAh. Baterai ini mengalir ke XL6009 dan MAX17048. XL6009 ini berguna untuk step up tegangan untuk menghidupi layar e-ink, tombol-tombol, dan ESP32 ini. MAX17408 ini berguna untuk membaca presentase nilai sisa dari kapasitas baterai tersebut. ESP32 berguna sebagai mikrokontroler untuk mengatur tindakan yang ada di alat monitor ini. Berikut adalah gambar PCB untuk alat monitor. 

.. gambar pcb...

PCB ini didesain sedemikian rupa untuk memaksimalkan alur kerja yang ada di alat monitor ini. PCB ini menggunakan double layer agar tidak saling bertabrakan antara jalur satu ke jalur yang lain.
## 📡 Sensor
Gambar 17 Desain 3D Alat Sensor 

 

Alat sensor ini ditenagai oleh 2 baterai Molicel P42A disambung secara paralel dengan kapasitas total 8400 mAh. Alat sensor ini terdapat sensor NPK tanah, sensor pH tanah, sensor suhu dan kelembaban tanah yang diproduksi oleh perusahaan JXCT. Alat ini akan membaca kondisi tanah seperti kandungan NPK, pH tanah, suhu dan kelembaban tanah yang kemudian di kirim melewati ESP32. Alat sensor ini juga mempunyai PCB yang berguna untuk menata jalur kelistrikan. Skematik PCB bisa dilihat di bawah ini : 

.. gambar Skematik ..

Gambar 18 Skematik PCB untuk Alat Sensor  

 

Di dalam skematik ini terdapat module TP4056, MAX17048, XL6009, dan ESP32. TP4056 ini berguna untuk charge kedua baterai tersebut. MAX17048 digunakan untuk membaca presentase nilai sisa baterai. XL6009 sangat dibutuhkan karena sensor-sensor ini membutuhkan tegangan 12 volt, dengan step up menggunakan XL6009, sensor akan berkerja dengan lancar. Otak dari segala ini adalah ESP32 yang mengatur semua dari alat sensor ini. ESP32 akan mengambil data dari sensor-sensor yang kemudian data di kirim ke ESP32 yang berada di alat monitor. ESP32 yang berada di monitor itu juga akan memproses datanya yang kemudian menjadi rekomendasi NPK, pH maupun suhu dan kelembaban Untuk menciptakan kondisi tanah yang optimal bagi pertanian. Berikut ini adalah gambar PCB untuk alat sensor : 

Gambar 19 PCB untuk Alat Sensor 
## 📑 Datasheet

[Documentation](https://linktodocumentation)

