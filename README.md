Autonomous-and-Localization-Turtlebot-4

Lokalisasi dan Pemetaan — RE702 Midterm Exam
42222201044 Abdi Wijaya Sasmita — RE 7B Pagi

Deskripsi

Repositori ini merupakan bagian dari pengerjaan ujian tengah semester mata kuliah Lokalisasi dan Pemetaan/RE702. Paket ROS2 yang disertakan berfungsi untuk mengarahkan TurtleBot4 bergerak dari satu titik ke titik lain serta mengaktifkan buzzer sesuai instruksi asesmen.

Persiapan

Sebelum melakukan build dan menjalankan paket ini, pastikan Anda telah membuat peta (map) untuk lingkungan yang digunakan.
Peta disimpan di direktori maps/.

Panduan pembuatan peta TurtleBot4 dapat dilihat pada dokumentasi resmi:
https://turtlebot.github.io/turtlebot4-user-manual/tutorials/generate_map.html

Pastikan laptop/PC berada pada jaringan yang sama dengan TurtleBot4, kemudian lakukan SSH ke robot sebelum menjalankan perintah.

1. Menjalankan Localization & Navigation

Pada terminal TurtleBot4, jalankan:

ros2 launch turtlebot4_navigation localization.launch.py map:=path/ke/map.yaml

Pastikan path menuju map.yaml sudah benar.

2. Menjalankan Nav2 (di robot)

Buka terminal kedua di TurtleBot4 dan jalankan:

ros2 launch turtlebot4_navigation nav2.launch.py

3. Menjalankan RViz2 (di laptop/PC)

Pada terminal laptop/PC yang terhubung ke robot:

ros2 launch turtlebot4_viz view_navigation.launch.py


Pastikan pose robot di RViz sesuai dengan posisi fisiknya di lapangan.

Build Package

Buat workspace:

mkdir -p ros2_ws/src
cd ros2_ws/src


Clone repository:

git clone https://github.com/AbdiWijaya02/UTS-RE702---Turtlebot4.git


Build workspace:

cd ../
colcon build
source install/setup.bash


Menjalankan program utama:

ros2 run abdi_pkg abdinode 

Demo
Video demonstrasi dapat dilihat pada tautan berikut:
