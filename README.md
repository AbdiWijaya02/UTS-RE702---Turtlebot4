#Autonomous and Localization TurtleBot4
Lokalisasi dan Pemetaan — RE702 Midterm Exam
42222201044 — Abdi Wijaya Sasmita (RE 7B Pagi)

##Deskripsi

Repositori ini digunakan untuk memenuhi Ujian Tengah Semester mata kuliah Lokalisasi dan Pemetaan (RE702).
Paket ROS2 di dalamnya menjalankan:

Localization TurtleBot4

Navigation (Nav2)

Pergerakan robot menuju titik tujuan

Aktivasi buzzer sesuai instruksi asesmen

Persiapan Awal
1. Pembuatan Peta

Pastikan Anda sudah membuat map untuk lingkungan pengujian.
Simpan peta pada direktori:

maps/

Panduan pembuatan peta resmi:
https://turtlebot.github.io/turtlebot4-user-manual/tutorials/generate_map.html

2. Koneksi ke Robot

Laptop/PC dan TurtleBot4 harus satu jaringan Wi-Fi

Lakukan SSH sebelum menjalankan perintah:

ssh ubuntu@192.168.185.3

###Menjalankan Sistem
1. Localization

Pada terminal TurtleBot4:

ros2 launch turtlebot4_navigation localization.launch.py map:=path/ke/map.yaml

2. Navigation (Nav2)

Terminal kedua:

ros2 launch turtlebot4_navigation nav2.launch.py

3. Menampilkan RViz2

Pada laptop/PC:

ros2 launch turtlebot4_viz view_navigation.launch.py


Pastikan posisi robot di RViz sesuai posisi fisik di lapangan.

###Build ROS2 Workspace
Membuat workspace
mkdir -p ros2_ws/src
cd ros2_ws/src

###Clone repository
git clone https://github.com/AbdiWijaya02/UTS-RE702---Turtlebot4.git

###Build workspace
cd ../
colcon build
source install/setup.bash

###Menjalankan Node Utama
ros2 run abdi_pkg abdinode

###Demo

Video demonstrasi tersedia pada tautan berikut:
(tambahkan link video di sini)