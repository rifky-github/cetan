<div align="center">
  <img width="745" alt="Screenshot 2025-03-26 at 07 19 16" src="https://github.com/user-attachments/assets/14926067-b8d0-4145-8916-003004e9d230" />
</div>

# 🌱 CeTan (Cek Tanah)
<div align="center">
  <img src="https://github.com/user-attachments/assets/e3d7904d-a01a-4972-bfbd-51f6cc200ff4" width="500">
</div>

Sebuah alat yang bisa mengukur kadar tanah dengan bantuan sensor NPK (Nitrogen, Potassium, Kalsium), sensor pH, dan sensor Kelembaban Tanah. Alat ini sangat bagus untuk para petani yang ingin meningkatkan kesuburan tanamannya


## 📐 Perancangan Sistem
![Sistem](https://github.com/user-attachments/assets/dd4b391e-3c64-4203-9d11-49a948023c6a)

Sistem kerja alat ini didasari oleh modul ESP32 yang berfungsi sebagai mikrokontroler yang dilengkapi modul Wi-Fi. Modul ESP32 ini menggunakan koneksi Wi-Fi untuk mengkomunikasikan antara Sensor dan Monitor. Sensor Tanah seperti Sensor Temperatur dan Kelembapan Tanah, Sensor pH Tanah, Sensor NPK Tanah, dimasukkan ke dalam tanah kemudian sensor-sensor tersebut akan membaca kandungan mineral tanah dan kondisi tanah (NPK, Kelembapan Tanah dan pH Tanah), kemudian data kandungan mineral tanah dan kondisi tanah dikirim ke Monitor lewat mikrokontroler ESP32. Monitor memunculkan data yang telah dikirim dari Sensor.

# 🖥️ Monitor

<div align="center">
  <img src="https://github.com/user-attachments/assets/97261013-abb1-41b6-9efe-ea5774d3fbd6" width="500">
</div>

Alat monitor ini dilengkapi dengan fitur penggenggam tangan supaya tangan tidak kelelahan pada saat menggunakan alat monitor ini. Terdapat tombol navigasi dan enter yang berguna untuk memilih menu yang ada di layar e-ink ini. Alat ini juga dilengkapi PCB didalamnya yang berguna untuk saling komunikasi antara alat monitor dan alat sensor. Alat ini juga dilengkapi saklar yang berada di atas kanan yang berguna untuk menghidupkan monitor ini.

<div align="center">
  <br></br>
  <img width="1364" alt="Screenshot 2025-03-26 at 07 58 54" src="https://github.com/user-attachments/assets/9b965a9e-9213-49ca-a08b-5fac765f65c2" />
  <a href="https://github.com/user-attachments/files/19458811/PCB.pdf">Klik di sini Untuk Download</a>
  <br></br>
</div>

Gambar di atas ini adalah skematik dari PCB alat monitor. Module yang digunakan pada PCB ini adalah TP4056, MAX17048, XL6009 dan ESP32. TP4056 ini berguna untuk charge baterai yang ada di PCB ini. Baterai yang digunakan adalah Baterai Molicel P42A dengan spesifikasi 3.7 volt dan 4200 mAh. Baterai ini mengalir ke XL6009 dan MAX17048. XL6009 ini berguna untuk step up tegangan untuk menghidupi layar e-ink, tombol-tombol, dan ESP32 ini. MAX17408 ini berguna untuk membaca presentase nilai sisa dari kapasitas baterai tersebut. ESP32 berguna sebagai mikrokontroler untuk mengatur tindakan yang ada di alat monitor ini. Berikut adalah gambar PCB untuk alat monitor. 

<img width="860" alt="Screenshot 2025-03-26 at 16 22 30" src="https://github.com/user-attachments/assets/1a74beed-7b62-468d-b749-962e8c0fdee6" />

PCB ini didesain sedemikian rupa untuk memaksimalkan alur kerja yang ada di alat monitor ini. PCB ini menggunakan double layer agar tidak saling bertabrakan antara jalur satu ke jalur yang lain.
## 📡 Sensor

![174294871067561018 (1)](https://github.com/user-attachments/assets/d9797396-b3b2-4b92-9428-8721e3d3a5a3)

Alat sensor ini ditenagai oleh 2 baterai Molicel P42A disambung secara paralel dengan kapasitas total 8400 mAh. Alat sensor ini terdapat sensor NPK tanah, sensor pH tanah, sensor suhu dan kelembaban tanah yang diproduksi oleh perusahaan JXCT. Alat ini akan membaca kondisi tanah seperti kandungan NPK, pH tanah, suhu dan kelembaban tanah yang kemudian di kirim melewati ESP32. Alat sensor ini juga mempunyai PCB yang berguna untuk menata jalur kelistrikan. Skematik PCB bisa dilihat di bawah ini : 

<div align="center">
  <br></br>
  <img width="1296" alt="Screenshot 2025-03-26 at 16 38 44" src="https://github.com/user-attachments/assets/fc939abe-d99d-4f12-bf67-858df7623911" />
  <a href="https://github.com/user-attachments/files/19464249/PCB.Sensor.pdf">Klik di sini Untuk Download</a>
  <br></br>
</div>

Di dalam skematik ini terdapat module TP4056, MAX17048, XL6009, dan ESP32. TP4056 ini berguna untuk charge kedua baterai tersebut. MAX17048 digunakan untuk membaca presentase nilai sisa baterai. XL6009 sangat dibutuhkan karena sensor-sensor ini membutuhkan tegangan 12 volt, dengan step up menggunakan XL6009, sensor akan berkerja dengan lancar. Otak dari segala ini adalah ESP32 yang mengatur semua dari alat sensor ini. ESP32 akan mengambil data dari sensor-sensor yang kemudian data di kirim ke ESP32 yang berada di alat monitor. ESP32 yang berada di monitor itu juga akan memproses datanya yang kemudian menjadi rekomendasi NPK, pH maupun suhu dan kelembaban Untuk menciptakan kondisi tanah yang optimal bagi pertanian. Berikut ini adalah gambar PCB untuk alat sensor : 

<div align="center">
<img width="599" alt="Screenshot 2025-03-26 at 16 42 47" src="https://github.com/user-attachments/assets/def7f8ff-50ea-4e90-8bd4-ac26df03517e" />
</div>


## 📑 Datasheet

[esp32_datasheet_en.pdf](https://github.com/user-attachments/files/19464363/esp32_datasheet_en.pdf)

[soil-sensor-jxbs-3001-npk-rs (1).pdf](https://github.com/user-attachments/files/19464356/soil-sensor-jxbs-3001-npk-rs.1.pdf)

[RS485-Soil-PH-Sensor-JX-Instruction-Manual.pdf](https://github.com/user-attachments/files/19464355/RS485-Soil-PH-Sensor-JX-Instruction-Manual.pdf)

[jxbs3001trrs.pdf](https://github.com/user-attachments/files/19464353/jxbs3001trrs.pdf)

[Documentation](https://linktodocumentation)

## 📑 Note
Project ini masih dalam bentuk proposal yang berarti belum dieksekusi.
Belum ada budget untuk memproduksi alat ini.
Proposal ini bersifat open source yang berarti 
