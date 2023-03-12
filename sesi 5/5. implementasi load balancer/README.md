# Sesi 5 - Implementasi Load Balancer

1. Jalankan aplikasi laravel dengan
     ```
     docker run --name laravel-app -p 7000:80 -d <username_docker_hub>/laravel-app:v1
     ```
     atau 
     ```
     docker run -it -d --privileged=true --name laravel-app1 -p 7000:80 -p 3021:22 -v /home/dockeruser/docker <nama image>
     ```
     ```
     curl ip:me
     ```
     cek browser <IP :7000>/login 
2. Jalankan aplikasi laravel kedua dengan
     ```
     docker run --name laravel-app -p 8000:80 -d <username_docker_hub>/laravel-app:v1
     ```
       atau 
     ```
     docker run -it -d --privileged=true --name laravel-app2 -p 8000:80 -p 3022:22 -v /home/dockeruser/docker <nama image>
     ```
     ```
     curl ip:me
     ```
     cek browser <IP :8000>/login
3. Jalankan aplikasi laravel kedua dengan
     ```
     docker run --name laravel-app -p 9000:80 -d <username_docker_hub>/laravel-app:v1
     ```
       atau 
     ```
     docker run -it -d --privileged=true --name laravel-app1 -p 9000:80 -p 3023:22 -v /home/dockeruser/docker <nama image>
     ```
     ```
     curl ip:me
     ```
     cek browser <IP :9000>/login
4. Buat Load balancer dengan settingan berikut.
    [source](https://raw.githubusercontent.com/agung3wi/panduan-kelasdevops/master/sesi%205/5.%20implementasi%load%20balancer/nginx.conf).

