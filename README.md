# tutorial-6

### Commit 1 Relflection
#### Method `handle_connection`

Method `handle_connection` berfungi untuk menangani koneksi TCP yang masuk dari pengguna melalui method `main` sebelumnya.  fungsi ini adalah menerima argumen `mut TcpStream` yang merepresentasikan koneksi dengan pengguna. `mut` berguna untuk memodifikasi streamnya (atau dalam kasus ini membaca data). Fungsi ini kemudian embuat `BufReader` yang akan membuat `TcpStream` menyediakan pembacaan data yang efisien dan terbuffer. `BufReader` meningkatkan kinerja dengan mengurangi jumlah panggilan sistem yang diperlukan untuk membaca potongan kecil data sekaligus. `BufReader` membaca setiap baris dan mengumpulkannya ke dalam sebuah vektor hingga menemukan baris kosong, yang kemungkinan menandakan akhir dari permintaan HTTP. Terakhir fungsi ini Mencetak seluruh vektor baris permintaan untuk debugging atau tujuan logging.

