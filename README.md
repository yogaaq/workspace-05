# MODUL 5 - DOCKER, NGINX, DAN BLACKSHEEP

- Nama: Yoga Prima Aditama  
- NIM : 235410034   
- Teknologi: Docker, Docker Compose, Nginx, BlackSheep

---

##  Latar Belakang
Containerization menggunakan Docker memungkinkan aplikasi berjalan dalam environment yang terisolasi sehingga lebih mudah dalam deployment, konsisten, dan tidak bergantung pada sistem operasi host.

Pada praktikum ini, digunakan Docker untuk menjalankan aplikasi web sederhana yang terdiri dari backend BlackSheep dan web server Nginx yang diorkestrasi menggunakan Docker Compose.

---

##  Tujuan Praktikum
Adapun tujuan dari praktikum ini adalah:
- Memahami konsep dasar Docker (image, container)
- Mengimplementasikan multi-container application
- Menggunakan Docker Compose untuk orkestrasi layanan
- Menghubungkan backend dan reverse proxy
- Menjalankan aplikasi web berbasis container

---


---

## Penjelasan Komponen

### 1. Docker
Docker digunakan untuk membuat container yang berisi aplikasi dan dependency sehingga dapat berjalan di berbagai environment tanpa konflik sistem.

---

### 2. BlackSheep (Backend)
BlackSheep adalah framework Python ringan yang digunakan sebagai backend service untuk menangani request HTTP dan menyediakan endpoint API.

Fungsi utama:
- Menyediakan response API
- Menangani request dari Nginx

---

### 3. Nginx (Reverse Proxy)
Nginx digunakan sebagai web server sekaligus reverse proxy yang bertugas:
- Menerima request dari user
- Meneruskan request ke backend BlackSheep
- Mengatur routing HTTP

---

### 4. Docker Compose
Docker Compose digunakan untuk menjalankan beberapa container sekaligus dalam satu konfigurasi.

Dengan Docker Compose:
- Backend dan Nginx berjalan bersamaan
- Networking antar container otomatis diatur
- Deployment lebih mudah

---

## Alur Sistem
1. User mengakses browser (localhost)
2. Request masuk ke Nginx container
3. Nginx meneruskan request ke BlackSheep backend
4. BlackSheep memproses request
5. Response dikirim kembali ke user melalui Nginx

---

## Cara Menjalankan Project

Jalankan perintah berikut di root folder project:

```bash
docker-compose up --build