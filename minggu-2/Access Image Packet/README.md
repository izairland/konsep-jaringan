## Access Image Packet in HTTP
Mengakses paket gambar dalam HTTP mengacu pada menemukan dan mengekstrak gambar dari lalu lintas data HTTP dengan menggunakan alat seperti Wireshark. Ini memungkinkan untuk melihat, menyimpan, atau menganalisis gambar yang dikirim melalui protokol HTTP dalam paket data.
1. Bukalah berkas tangkapan contoh (sample capture) dengan nama "http_with_jpegs.cap" menggunakan aplikasi Wireshark, dan pastikan Anda mengatur filter tangkapan untuk hanya menampilkan lalu lintas HTTP.
<div align="center">
<img src="assets/jpeg_cap.png">
</div>
2. Temukan paket yang menyertakan informasi "200 OK" dan juga merupakan gambar JPEG JFIF.
<div align="center">
<img src="assets/200_ok.png">
</div>
3. Klik pada paket tersebut, kemudian klik kanan pada format gambar JPEG File Interchange Format yang terdapat di jendela di bawah sebelah kiri. Selanjutnya, pilih opsi "Tampilkan Byte Paket" dengan mengkliknya, atau gunakan pintasan keyboard "CTRL + SHIFT + O."
<div align="center">
<img src="assets/left_bar.png">
</div>
4. Wireshark akan secara otomatis menampilkan konten gambar dari paket tersebut. Berikut adalah gambar contoh dari paket nomor 61.
<div align="center">
<img src="assets/61.png">
</div>
5. Ada 5 paket yang berisi data gambar dalam berkas tangkapan tersebut. Berikut ini adalah 4 paket sisanya yang juga berisi data gambar.
<div align="center">
<img src="assets/72.png">
</div>
<div align="center">
<img src="assets/259.png">
</div>
<div align="center">
<img src="assets/269.png">
</div>
<div align="center">
<img src="assets/479.png">
</div>
