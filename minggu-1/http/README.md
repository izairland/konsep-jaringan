## HTTP
**Pengenalan HTTP**
HTTP, singkatan dari "Hypertext Transfer Protocol," adalah protokol komunikasi yang digunakan untuk mentransfer data melalui World Wide Web (WWW) atau internet. HTTP digunakan untuk mengirim permintaan (request) dari klien (seperti browser web) ke server web, dan server kemudian merespons dengan data yang diminta, seperti halaman web, gambar, atau file lainnya.

**Analisa http.cap pada Wireshark**

 1. Header HTTP
	 Header HTTP adalah bagian penting dari permintaan (request) dan tanggapan (response) dalam protokol HTTP (Hypertext Transfer Protocol). Header HTTP mengandung informasi tambahan yang diperlukan untuk mengontrol dan mengelola permintaan dan tanggapan HTTP. Berikut adalah beberapa contoh header HTTP yang umum digunakan:

Header Permintaan (Request Headers):

1.  **Host**: Menunjukkan nama host (domain) yang akan diakses oleh klien.
2.  **User-Agent**: Mengidentifikasi agen pengguna atau perangkat yang melakukan permintaan, seperti browser web atau aplikasi.
3.  **Accept**: Menunjukkan jenis media yang diterima oleh klien, seperti tipe konten yang dapat diterima.
4.  **Accept-Language**: Menunjukkan preferensi bahasa klien untuk respons.
5.  **Accept-Encoding**: Menunjukkan metode kompresi yang diterima oleh klien untuk mengurangi ukuran respons.
6.  **Connection**: Menunjukkan apakah koneksi harus tetap terbuka setelah tanggapan diterima (biasanya "keep-alive").

Header Tanggapan (Response Headers):

1.  **Server**: Menunjukkan perangkat lunak server yang digunakan oleh server web.
2.  **Date**: Menunjukkan waktu ketika tanggapan dikirim oleh server.
3.  **Content-Type**: Menunjukkan tipe konten dari data yang dikirim dalam respons, seperti teks HTML, gambar JPEG, atau JSON.
4.  **Content-Length**: Menunjukkan panjang (ukuran) konten dalam byte.
5.  **Location**: Digunakan untuk pengalihan (redirect), mengarahkan klien ke URL lain.
6.  **Cache-Control**: Mengatur aturan caching untuk respons.
7.  **Set-Cookie**: Mengirim cookie kepada klien untuk pengelolaan sesi atau penyimpanan data di sisi klien.
8.  **Access-Control-Allow-Origin**: Menentukan domain yang diizinkan untuk mengakses sumber daya melalui permintaan lintas domain (CORS).

<div align="center">
<img src="assets/header-http">
<p><strong>Gambar:</strong> header http</p>
</div>

**Data Payload HTTP**

Data payload dalam HTTP merujuk pada konten aktual yang dikirim dalam tubuh permintaan (request) atau tanggapan (response) HTTP. Data payload ini bisa berupa teks, gambar, file biner, atau jenis data lainnya, tergantung pada jenis konten yang diakses melalui permintaan HTTP. Berikut adalah beberapa contoh data payload dalam HTTP:

**1. Data HTML:** Data HTML adalah salah satu jenis payload yang paling umum dalam permintaan HTTP. Ini adalah konten HTML yang digunakan untuk membuat halaman web. 
**2. Gambar:** Gambar seperti JPEG, PNG, atau GIF juga dapat menjadi payload dalam permintaan HTTP. Ini adalah data biner yang mewakili gambar.
**3. Data JSON:** JSON (JavaScript Object Notation) adalah format yang sering digunakan untuk pertukaran data antara server dan klien. Data JSON biasanya digunakan dalam permintaan dan tanggapan API web.
**4. File Binis (Binary Files):** Payload HTTP juga dapat berupa file biner seperti PDF, video, atau aplikasi.
**5. Data Formulir (Form Data):** Ketika klien mengirimkan data melalui formulir web, data tersebut menjadi payload permintaan HTTP. Data ini biasanya dikirim dalam format yang mudah dibaca oleh server, seperti x-www-form-urlencoded atau multipart/form-data.

<div align="center">
<img src="assets/data-payload-http">
<p><strong>Gambar:</strong> Data Payload HTTP</p>
</div>

**I/o Graph HTTP**

Grafik I/O (Input/Output) atau grafik aliran data HTTP adalah alat visual yang digunakan untuk memahami proses pertukaran data antara klien dan server melalui protokol HTTP. Grafik ini menggambarkan langkah-langkah atau tahapan yang terjadi selama permintaan HTTP (request) dan tanggapan HTTP (response).
<div align="center">
<img src="assets/io-graph-http">
<p><strong>Gambar:</strong> I/O Graph HTTP</p>
</div>


