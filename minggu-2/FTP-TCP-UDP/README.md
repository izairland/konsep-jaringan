
## File Transfer Protocol
File Transfer Protocol (FTP) adalah protokol komunikasi untuk mentransfer file antara server dan klien di jaringan. Ini melibatkan autentikasi, dua mode transfer (biner dan ASCII), dan memiliki mode pasif dan aktif. FTP umumnya digunakan untuk mengakses dan berbagi file tetapi rentan terhadap ancaman keamanan, sehingga lebih baik menggunakan variasi lebih aman seperti FTPS atau SFTP.
<div align="center">
<img src="assets/ftp">
<p><strong>Gambar:</strong> FTP</p>
</div>

## Transmission Control Protocol
Transmission Control Protocol (TCP) adalah protokol jaringan yang memastikan pengiriman data terkendali, terjamin integritasnya, dan mengatur aliran data. Ini menggunakan koneksi berorientasi dan handshake tiga langkah untuk memulai koneksi.
<div align="center">
<img src="assets/tcp">
<p><strong>Gambar:</strong> TCP</p>
</div>
TCP bekerja dengan menginisialisasi koneksi, mengirim data dalam segmen terurut, dan memastikan data diterima dengan baik oleh penerima melalui nomor urut (sequence number) dan konfirmasi (acknowledgment).

## User Datagram Protocol
User Datagram Protocol (UDP) adalah protokol komunikasi dalam jaringan yang berfokus pada pengiriman data dengan cepat dan sederhana. UDP adalah protokol tanpa koneksi, artinya tidak ada konfirmasi penerimaan data atau penanganan otomatis kesalahan. Ini sering digunakan untuk aplikasi yang membutuhkan pengiriman cepat dan toleransi terhadap kehilangan data, seperti video streaming, game online, dan aplikasi real-time. UDP berbeda dari Transmission Control Protocol (TCP) yang menawarkan pengiriman data yang andal dengan konfirmasi dan pengendalian kesalahan.
<div align="center">
<img src="assets/udp">
<p><strong>Gambar:</strong> UDP</p>
</div>