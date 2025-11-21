# Autonomous-and-Localization-Turtlebot-4
Lokalisasi dan Pemetaan/RE702 Midterm Exam
42222201014 Muhammad Ribfli RE 7 A Pagi

# RE702 Midterm Localization & Mapping
Repositori ini dibuat sebagai bagian dari pengerjaan asesmen tengah semester mata kuliah Lokalisasi dan Pemetaan (RE702). Package ROS2 ini bertujuan untuk menggerakkan TurtleBot4 dari satu posisi ke posisi lain serta mengaktifkan buzzer, sesuai instruksi asesmen.

## Persiapan Sebelum Menjalankan Package
Sebelum melakukan build dan menjalankan package ROS2 ini, pastikan Anda telah menghasilkan peta map sesuai dengan environment yang digunakan.
Peta hasil mapping disimpan pada folder maps/. Untuk membuat peta baru, Dapat mengikuti dokumentasi TurtleBot4:

https://turtlebot.github.io/turtlebot4-user-manual/tutorials/generate_map.html

Pastikan perangkat (laptop/PC) telah terhubung ke LAN atau WiFi yang sama dengan TurtleBot4, kemudian lakukan SSH ke robot.

## 1. Running Localization & Navigation
Di terminal TurtleBot4, jalankan:
```bash
ros2 launch turtlebot4_navigation localization.launch.py map:=path/ke/map.yaml
```
> Pastikan path/ke/map.yaml diganti dengan path file map yang benar.

## 2. Jalankan Nav2 (di robot TurtleBot4)
Di terminal TurtleBot4 lainnya, jalankan:
```bash
ros2 launch turtlebot4_navigation nav2.launch.py
```
## 3. Jalankan visualisasi RViz2 (di laptop/PC)
Pada terminal laptop/PC yang terhubung dengan TurtleBot4, jalankan:
```bash
ros2 launch turtlebot4_viz view_navigation.launch.py
```
> Pastikan pose robot di RViz sesuai dengan posisi fisik di lapangan.

---

## Build Package dari Repository Ini

Buat workspace:
```bash
mkdir -p ros2_ws/src
cd ros2_ws/src
```

Clone repository:
```bash
git clone https://github.com/RIBFLI/Autonomous-and-Localization-Turtlebot-4.git
```

Build workspace:
```bash
cd ../
colcon build
source install/setup.bash
```

Menjalankan program:
```bash
ros2 run re702_midterm_localization_mapping navigation
```

---

##  Demo

Video demonstrasi dapat dilihat di:
https://youtu.be/0ICtoX1--R0
