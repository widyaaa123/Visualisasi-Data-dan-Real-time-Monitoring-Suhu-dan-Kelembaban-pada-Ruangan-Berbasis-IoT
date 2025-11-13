# IoT Monitoring Suhu dan Kelembaban

Proyek ini bertujuan untuk memantau **suhu dan kelembaban secara real-time** menggunakan sensor DHT22 dan mikrokontroler **Wemos D1 ESP8266** yang terhubung ke **Grafana** untuk visualisasi data.  
Data sensor disimpan ke dalam **PostgreSQL** melalui koneksi MQTT.

---

## Komponen yang Digunakan
- Wemos D1 ESP8266  
- Sensor DHT22  
- Kabel jumper  
- Box project  
- Broker MQTT (contoh: Mosquitto)  
- **PostgreSQL** sebagai database  
- **Grafana** untuk visualisasi data  

---

## Instalasi dan Koneksi Hardware

Sensor **DHT22** dipasang di dalam **box project** untuk melindungi dari lingkungan luar, namun tetap dapat mengukur suhu dan kelembaban dengan akurat.

Koneksi dilakukan menggunakan **kabel jumper** yang menghubungkan sensor DHT22 ke **board Wemos D1 ESP8266** pada pin data, VCC, dan GND.

Sumber daya diperoleh melalui **kabel USB** yang menghubungkan board Wemos D1 ke **laptop**. Saat kabel USB terhubung, rangkaian dapat berfungsi dengan semestinya dan data dari sensor dapat dikirim ke server untuk disimpan di PostgreSQL dan divisualisasikan di Grafana.

**Skema singkat koneksi:**
- DHT22 → Wemos D1  
  - VCC → 3.3V  
  - GND → GND  
  - Data → D4 (GPIO2)

---

## Visualisasi Dashboard (Grafana)
Berikut tampilan dashboard Grafana untuk monitoring suhu dan kelembaban secara real-time:

![alt text](https://github.com/widyaaa123/Visualisasi-Data-dan-Real-time-Monitoring-Suhu-dan-Kelembaban-pada-Ruangan-Berbasis-IoT/blob/main/Dashboard%20Grafana.png?raw=true)

---

## Rangkaian Alat IoT
Berikut foto alat yang digunakan dalam proyek ini:

![alt text](https://github.com/widyaaa123/Visualisasi-Data-dan-Real-time-Monitoring-Suhu-dan-Kelembaban-pada-Ruangan-Berbasis-IoT/blob/main/alat.png?raw=true)

---

## Cara Menjalankan Proyek

1. Upload kode Arduino ke board **Wemos D1 ESP8266**.  
2. Pastikan koneksi **WiFi** dan **broker MQTT** sudah dikonfigurasi dengan benar.  
3. Jalankan **PostgreSQL** sebagai database penyimpanan data sensor.  
4. Hubungkan **Grafana** ke PostgreSQL untuk menampilkan data secara visual.  
5. Buka dashboard Grafana untuk memantau data suhu dan kelembaban secara langsung.


