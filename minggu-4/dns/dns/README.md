## DNS 
DNS, atau Domain Name System, adalah sistem yang digunakan untuk mengonversi nama domain yang mudah diingat menjadi alamat IP (Internet Protocol) yang digunakan oleh komputer dalam jaringan internet. DNS berfungsi sebagai direktori alamat yang memetakan nama domain, seperti [www.example.com](http://www.example.com/), ke alamat IP yang sesungguhnya, seperti 192.0.2.1. Ini memungkinkan kita untuk mengakses situs web, layanan, dan sumber daya online dengan mudah tanpa perlu menghafal alamat IP yang panjang.
 <div align="center">
<img src="assets/dns.png">
</div>


Berikut adalah komponen-komponen utama dari DNS:

1.  **Name Server (Server Nama)**: Ini adalah server komputer yang menyimpan basis data DNS. Ada beberapa jenis server DNS, termasuk server otoritatif (authority servers) yang menyimpan informasi tentang zona atau domain tertentu, dan server resolusi (resolver servers) yang digunakan oleh klien (seperti komputer atau perangkat mobile) untuk mencari informasi DNS.
    
2.  **DNS Record (Catatan DNS)**: Informasi DNS disimpan dalam catatan DNS. Beberapa jenis catatan DNS meliputi:
    
    -   **A Record (Address Record)**: Mengaitkan nama domain dengan alamat IPv4.
    -   **AAAA Record (IPv6 Address Record)**: Mengaitkan nama domain dengan alamat IPv6.
    -   **CNAME (Canonical Name)**: Mengaitkan nama domain dengan nama kanonikal (alias).
    -   **MX (Mail Exchanger)**: Menentukan server email yang bertanggung jawab untuk alamat email dalam domain.
    -   **NS (Name Server)**: Menginformasikan server DNS yang memiliki otoritas untuk zona atau domain tertentu.
3.  **Resolver (Pemecah)**: Ini adalah komponen perangkat lunak yang ada di komputer atau perangkat pengguna akhir yang bertugas untuk mengirim permintaan DNS ke server DNS resolusi. Resolver akan mencari alamat IP yang sesuai dengan nama domain yang diminta.
    

DNS bekerja dengan melakukan proses yang disebut DNS lookup atau resolusi. Proses ini melibatkan langkah-langkah berikut:

1.  **Permintaan dari Pengguna:** Pengguna memasukkan nama domain ke browser mereka.
    
2.  **Cari dalam Cache Lokal:** Browser memeriksa cache lokal untuk melihat apakah alamat IP telah disimpan sebelumnya. Jika iya, maka situs web dimuat dari cache.
    
3.  **Permintaan ke Server DNS Lokal (Resolver):** Jika informasi tidak ada di cache, browser mengirimkan permintaan ke server DNS lokal yang dikonfigurasi oleh penyedia layanan internet (ISP).
    
4.  **Pemeriksaan Cache Resolver:** Resolver memeriksa apakah informasi sudah ada dalam cache-nya. Jika ya, resolver akan mengembalikan alamat IP.
    
5.  **Tanya Server DNS Root:** Jika informasi tidak ada di cache resolver, resolver mengirimkan permintaan ke server DNS root untuk menemukan server DNS tingkat teratas (TLD) yang berkaitan dengan domain tersebut.
    
6.  **Tanya Server DNS TLD:** Server DNS root memberi tahu resolver tentang server DNS TLD yang sesuai dengan domain yang diminta.
    
7.  **Tanya Server DNS Otoritatif:** Resolver mengirimkan permintaan ke server DNS otoritatif yang memiliki informasi tentang alamat IP yang terkait dengan nama domain yang diminta.
    
8.  **Mendapatkan Alamat IP:** Server DNS otoritatif memberikan alamat IP kepada resolver.
    
9.  **Cache Hasil:** Resolver menyimpan informasi ini dalam cache-nya untuk penggunaan masa depan.
    
10.  **Mengirimkan Alamat IP ke Browser:** Resolver mengirimkan alamat IP ke browser pengguna.
    
11.  **Pemuatan Situs Web:** Browser menggunakan alamat IP untuk menghubungi server yang meng-host situs web yang diminta.
12.  **Tampilan Situs Web:** Akhirnya, situs web dimuat dan ditampilkan di browser pengguna.

DNS adalah bagian kunci dari infrastruktur internet, memungkinkan kita untuk mengakses berbagai layanan online dengan cara yang lebih mudah dan intuitif.