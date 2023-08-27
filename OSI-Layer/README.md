OSI (Open Systems Interconnection)
<div align="center">
<img src="assets/OSI-Layer.jpg">
<p><strong>Gambar:</strong> OSI layer</p>
</div>

OSI (Open Systems Interconnection) adalah sebuah model referensi yang digunakan untuk memahami dan menggambarkan bagaimana komunikasi jaringan komputer bekerja. Model OSI terdiri dari tujuh lapisan yang menyusun hierarki fungsional dari fungsi-fungsi yang diperlukan dalam komunikasi data. Setiap lapisan bertanggung jawab atas tugas-tugas tertentu dan bekerja bersama-sama untuk mengirimkan data dari satu perangkat ke perangkat lain dalam jaringan. Berikut adalah penjelasan lengkap mengenai masing-masing lapisan dalam model OSI:

1. Lapisan Fisik (Physical Layer):
 <div align="center">
<img src="assets/Physical.jpg">
<p><strong>Gambar:</strong> Physical</p>
</div>

Lapisan ini bertanggung jawab untuk mengirimkan bit-bit mentah melalui media transmisi fisik seperti kabel, serat optik, atau gelombang radio. Fungsi utamanya adalah mengatur aspek fisik dari transmisi data, termasuk tipe kabel, tegangan sinyal, kecepatan transmisi, dan topologi jaringan.

2. Lapisan Data Link (Data Link Layer):
 <div align="center">
<img src="assets/Data-Link.jpg">
<p><strong>Gambar:</strong> Data Link</p>
</div>

Lapisan ini bertanggung jawab untuk mengelola aliran data antara dua perangkat yang berdekatan dalam jaringan. Ini melibatkan deteksi dan koreksi kesalahan, pengaturan aliran data, dan pengalamatan fisik (MAC address).

3. Lapisan Jaringan (Network Layer):
 <div align="center">
<img src="assets/Network.jpg">
<p><strong>Gambar:</strong> Network</p>
</div>

Lapisan ini mengatur alamat logis (IP address) dan mengatur pengiriman data antar jaringan yang berbeda. Fungsi utamanya adalah pengalihan paket data dan pemilihan jalur terbaik untuk mengirimkan data dari sumber ke tujuan.

4. Lapisan Transport (Transport Layer):
 <div align="center">
<img src="assets/Transport.jpg">
<p><strong>Gambar:</strong> Transport</p>
</div>


Lapisan ini bertanggung jawab untuk memastikan pengiriman data yang andal antara sumber dan tujuan. Ini mencakup pengaturan kesalahan, pengurutan, dan pengelompokan data dalam segmen-segmen.

5. Lapisan Sesi (Session Layer):
 <div align="center">
<img src="assets/Session.jpg">
<p><strong>Gambar:</strong> Session</p>
</div>

Lapisan ini memungkinkan dua aplikasi di berbagai perangkat untuk memulai, mengelola, dan mengakhiri sesi komunikasi. Ini mencakup pengaturan pembukaan, pemeliharaan, dan penutupan koneksi.

6. Lapisan Presentasi (Presentation Layer):
 <div align="center">
<img src="assets/Presentation.jpg">
<p><strong>Gambar:</strong> Presentation</p>
</div>

Lapisan ini mengelola konversi, kompresi, dan enkripsi data agar dapat diinterpretasikan oleh aplikasi penerima. Ini juga memastikan bahwa data yang dikirim memiliki format yang kompatibel.

7. Lapisan Aplikasi (Application Layer):
 <div align="center">
<img src="assets/Application.jpg">
<p><strong>Gambar:</strong> Application</p>
</div>

Lapisan teratas ini berinteraksi langsung dengan aplikasi pengguna. Ini menyediakan antarmuka untuk akses ke layanan jaringan seperti email, web browsing, dan transfer berkas.

Komunikasi protokol adalah serangkaian aturan dan norma yang mengatur pertukaran data antara perangkat dalam sebuah jaringan. Protokol dapat berkaitan dengan berbagai lapisan OSI. Contohnya, protokol HTTP (Hypertext Transfer Protocol) bekerja pada lapisan aplikasi untuk mengatur pertukaran data dalam web browsing, sementara protokol TCP (Transmission Control Protocol) bekerja pada lapisan transport untuk mengatur pengiriman data yang andal.

Ketika dua perangkat ingin berkomunikasi, mereka harus setuju pada protokol yang akan mereka gunakan dan mematuhi aturan yang terkandung dalam protokol tersebut. Model OSI dan protokol komunikasi memungkinkan perangkat dengan perangkat yang berbeda untuk berkomunikasi secara efisien dalam jaringan yang kompleks.