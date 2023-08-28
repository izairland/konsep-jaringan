	## Port FTP
<div align="center">
<img src="assets/FTP/Port Networking.PNG">
<p><strong>Gambar:</strong> Port Networking</p>
</div>

Port dalam komputer dan jaringan adalah mekanisme yang digunakan untuk mengarahkan lalu lintas data ke aplikasi atau layanan tertentu di dalam perangkat. Secara umum, protokol FTP (File Transfer Protocol) menggunakan TCP (Transmission Control Protocol) sebagai protokol transportasinya. Namun, dalam beberapa kasus, mungkin terdapat pernyataan bahwa 1 port FTP bisa menggunakan UDP (User Datagram Protocol) atau TCP. 

**1. Penggunaan UDP dalam 1 Port FTP:**
Sangat tidak umum bagi protokol FTP untuk menggunakan UDP secara eksklusif pada satu port tertentu. UDP biasanya digunakan untuk aplikasi yang memerlukan latensi rendah, seperti permainan online atau streaming media, di mana kecepatan lebih diutamakan daripada keandalan. Penggunaan UDP dalam protokol FTP mungkin terjadi dalam kasus-kasus yang sangat spesifik dan tidak konvensional. Namun, ini akan menimbulkan risiko terkait dengan integritas data dan kemungkinan kehilangan paket.

**2. Penggunaan TCP dalam 1 Port FTP:**
Penggunaan TCP dalam protokol FTP jauh lebih umum dan dikenal sebagai pendekatan standar. TCP menyediakan komunikasi yang handal, dengan deteksi kesalahan, retransmisi paket, dan penjaminan urutan yang benar. Dalam hal protokol FTP, port kontrol (biasanya port 21) digunakan untuk menginisiasi dan mengatur sesi, sedangkan port data (misalnya, port 20) digunakan untuk transfer file aktual. Keandalan TCP memastikan bahwa file-file dapat dikirim dan diterima tanpa kerugian data dan dalam urutan yang benar.

**Kesimpulan:**
Meskipun mungkin ada pernyataan bahwa 1 port FTP bisa menggunakan UDP atau TCP, penggunaan UDP dalam protokol FTP sangat jarang terjadi dan biasanya melibatkan implementasi khusus atau kasus yang tidak konvensional. Dalam konteks umum, protokol FTP umumnya menggunakan TCP sebagai protokol transportasi untuk memastikan keandalan dan keintegritasan transfer file antara klien dan server.