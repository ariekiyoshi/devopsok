# Sesi 5 - Inisialisasi Backing Service

sebelum membangun infrastuktur persiapkan media sbb :

a. local master (untuk test aplikasi di lokal kita dan membuat master image )
install (apache2, php7.4, docker, docker-compose, composer)
    
b. VM aws 1 (untuk instalasi docker mysql, mino, redis) install (Docker, Docker-Compose)
    
c. VM aws 2 (untuk instalasi app laravel di dalam docker) install (Docker, Docker-Compose)

1. Buat file baru dengan nama docker-compose.yml di VM aws 1
```
nano docker-compose.yml
```
Isikan kontent dari [docker-compose.yml](https://raw.githubusercontent.com/ariekiyoshi/devopsok/master/sesi%205/3.%20inisialisasi%20backing%20service/docker-compose.yml) berikut, kemudian simpan.

2. Kemudian jalankan
```
docker-compose up -d
```

I. Setelah itu masuk ke Local master 
lakukan instalasi sesuai petunjuk di atas, setelah itu lakukan clone di /home/"username"
```
git clone git@github.com:ariekiyoshi/bootcamp-laravel-master.git
```
II. Kemudian setting file ".env.example" 
```
cp /home/username/laravel/.env.example .env
```
III. lakukan setting easy an file .Env

sesuaikan dengan masing-masing connection server database, Minio, Redis (yang ada di docker compose yang kita compile tadi)
kemudian test
