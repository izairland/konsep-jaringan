## TCP in HTTP
TCP (Transmission Control Protocol) dalam HTTP (Hypertext Transfer Protocol) adalah protokol yang digunakan untuk mengatur pengiriman data antara server web dan klien web. HTTP adalah protokol aplikasi yang berjalan di atas TCP. TCP memastikan pengiriman data yang andal dengan memeriksa kesalahan, mengatur urutan paket data, dan mengelola koneksi antara server dan klien. Dengan kata lain, TCP adalah dasar yang memungkinkan HTTP untuk bekerja dengan efisien dalam pertukaran data antara browser web Anda dan server web.
<div align="center">
<img src="assets/HTTPCap">
<p><strong>Gambar:</strong> HTTP sample capture</p>
</div>
Untuk memfilter paket yang terkait dengan protokol HTTP dari 43 paket yang ada, Anda dapat melakukan langkah berikut: Klik kanan pada salah satu paket, lalu pilih opsi "Follow," dan kemudian pilih "TCP Stream." Ini akan membuka jendela yang hanya menampilkan paket-paket yang terkait dengan komunikasi HTTP, memudahkan analisis data HTTP dalam percakapan tersebut.
<div align="center">
<img src="assets/HTTPCapFiltered">
<p><strong>Gambar:</strong> HTTP sample capture filtered</p>
</div>
Wireshark akan secara otomatis menerapkan filter yang akan menampilkan hanya 34 paket dari total 43 paket yang ada, sehingga hanya paket-paket yang relevan dengan HTTP yang akan ditampilkan dalam tampilan.

## Flow Graph
Jendela Flow Graph digunakan untuk menampilkan informasi tentang koneksi antara dua host (klien dan server). Ini mencakup rincian seperti waktu pengiriman paket, arah komunikasi, serta tahapan koneksi mulai dari pembentukan koneksi, transfer data, hingga penutupan koneksi.
<div align="center">
<img src="assets/FlowGRaph">
<p><strong>Gambar:</strong> Flow Graph</p>
</div>

Tahap pembentukan koneksi dengan tiga langkah (Three-Way Handshake) melibatkan tiga paket awal. Berikut adalah detailnya:

1. Connect Estabilishment
<div align="center">
<img src="assets/TWH">
<p><strong>Gambar:</strong> Three Way Handshake</p>
</div>

->Pada saat 0.0000 detik, klien mengirim paket SYN (Synchronize Sequence Number) ke server dengan nomor urutan (sequence number) 0.
->Sekitar 0.9113 detik kemudian, server merespons dengan paket SYN-ACK yang memiliki nomor urutan 0 dan acknowledgment number 1, menandakan persetujuan koneksi dari klien dan memberikan sinyal kepada klien untuk mengirim paket selanjutnya dengan nomor urutan 1.
->Pada saat 0.9113 detik yang sama, klien merespons server dengan mengirim paket persetujuan (ACK) dengan nomor urutan 1 sesuai dengan sinyal dari server.

Setelah tiga langkah ini selesai, koneksi antara klien dan server telah berhasil dibentuk.

2. Data transfer
<div align="center">
<img src="assets/DT">
<p><strong>Gambar:</strong> Data Transfer Process</p>
</div>
Setelah koneksi terbentuk, klien dan server dapat memulai proses transfer data. Berikut adalah rincian tentang bagaimana proses transfer data berlangsung:

->Pada saat 0.9113 detik, klien mengirimkan sebuah segmen data dengan panjang 479 bit dan menandai segmen tersebut dengan flag PSH (Push) yang mengindikasikan kepada server untuk segera mengirimkan data kepada klien. Selain itu, klien juga mengirimkan paket ACK dengan nilai 1, yang memberi tahu server untuk mengirimkan segmen dengan nomor urutan (sequence number) 1.
->Pada saat 1.4721 detik, server merespons dengan mengirimkan dua segmen kepada klien, masing-masing memiliki nomor urutan 1. Segmen-segmen ini berisi data sepanjang 1380 bit. Server juga mengirimkan paket ACK dengan nilai 480, yang menunjukkan bahwa klien akan menerima segmen dengan nomor urutan 480 pada segmen berikutnya. Ini disebabkan oleh segmen sebelumnya dari klien yang berukuran 479 bit.

Proses transfer data akan berlanjut terus menerus hingga salah satu dari kedua host, baik klien atau server, mengirimkan flag FIN untuk mengakhiri koneksi. Banyaknya segmen yang dikirimkan oleh klien atau server selama proses transfer data ini akan tergantung pada lebar pita (bandwidth). Selain itu, panjang segmen-segmen tersebut juga dapat berubah selama proses transfer data berlangsung.

3. Connection Termination
<div align="center">
<img src="assets/CT">
<p><strong>Gambar:</strong> Connection Termination Process</p>
</div>
Proses terminasi koneksi dimulai ketika salah satu host mengirimkan flag FIN, yang menandakan niat untuk memutuskan koneksi. Proses terminasi ini berakhir ketika host lain juga mengirimkan FIN, sehingga kedua host mengakhiri koneksi. Berikut adalah rincian proses ini:

->Pada saat 17.9057 detik, server mengirimkan flag FIN dengan nomor urutan (sequence number) 18365 dan ACK 480, menandakan bahwa server memulai proses terminasi dan menunggu segmen selanjutnya dengan nomor urutan 480.
->Pada saat yang sama, klien merespons dengan mengirimkan acknowledgment untuk mengonfirmasi penerimaan FIN dari server. Selanjutnya, klien juga mengirimkan segmen FIN.
->Pada saat 30.0632 detik, klien mengirimkan segmen FIN dengan nomor urutan 480 sesuai dengan ACK dari server, dan memberitahu server bahwa klien juga akan mengakhiri koneksi.
->Pada saat 30.3937 detik, server merespons dengan mengirimkan acknowledgment untuk mengkonfirmasi penerimaan FIN dari klien.

Proses terminasi koneksi ini memastikan bahwa koneksi antara klien dan server diakhiri dengan benar, dan keduanya setuju untuk menghentikan komunikasi.

## Ilustrasi Data Transfer
<div align="center">
<img src="assets/ilt">
<p><strong>Gambar:</strong> Ilustrasi Data Tranfer</p>
</div>

## Packet Counter
Penghitung paket (Packet counter) berguna untuk melacak jumlah permintaan dan respon antara klien dan server. Dalam gambar di atas, kita dapat melihat bahwa ada total 4 Paket HTTP yang terdiri dari 2 permintaan dan 2 respon. Informasi ini juga memungkinkan kita untuk mengidentifikasi metode permintaan seperti GET, POST, PUT, PATCH, DELETE, dan sebagainya. Selain itu, kita bisa mengetahui status respons dari server, apakah 2xx (Sukses), 4xx (Kesalahan Klien), 5xx (Kesalahan Server), dan sejenisnya.
<div align="center">
<img src="assets/PC">
<p><strong>Gambar:</strong> Packet Counter</p>
</div>

## Throughput
TCP Throughput adalah ukuran efisiensi pengiriman data melalui koneksi TCP dalam suatu periode waktu. Ini mencerminkan jumlah data yang berhasil ditransmisikan melalui koneksi TCP dalam satuan data per waktu, seperti byte per detik atau bit per detik.

Grafik throughput dalam gambar tersebut menunjukkan perubahan dalam kecepatan transmisi data selama sesi koneksi. Grafik ini berguna untuk memantau puncak throughput, penurunan kinerja, atau tren dalam koneksi jaringan.

Titik puncak pada grafik mengindikasikan saat throughput mencapai nilai tertinggi.
Penurunan tajam atau fluktuasi dalam throughput dapat mengindikasikan masalah dalam koneksi jaringan, seperti kehilangan paket data atau konflik.
Melalui grafik throughput ini, kita dapat dengan cepat mengenali tren dan perubahan dalam kinerja koneksi TCP, membantu kita dalam memecahkan masalah jaringan, memantau kinerja aplikasi, atau melakukan analisis lebih lanjut terhadap sesi koneksi tertentu.
<div align="center">
<img src="assets/TP">
<p><strong>Gambar:</strong> Throughput</p>
</div>