Nama : Maysarah<br>
NIM : 2110131120006<br><br>

<h1 align="center">TUGAS MEMBUAT PSEUDOCODE</h1><br><br>

<h3><b>Patterning</b></h3><br>
<p align="justify">
<ul>
<li>Menentukan banyak pola patterning yang akan digunakan, jika matriks yang digunakan adalah 3x3 maka jumlah pola pattern yang dihasilkan adalah sebanyak 10. Jika matriks yang digunakan adalah 4x4 maka jumlah pola yang dihasilkan sebanyak 17. Rumusnya = ukuran matriks ditambah 1.</li>
<li>Menghitung persebaran range nilai dengan mengoperasikan 255 dibagi banyaknya jumlah pola pattern.</li>
<li>Jika matriks yang digunakan berukuran 3x3 dan font biner yang digunakan berukuran 2x2 maka hasil akhir matriks yang dihasilkan adalah 6x6</li>
<li>Untuk setiap matriks 3x3 yang berada pada matriks 6x6 mewakili salah satu pola pattern yang ada.</li>
</ul><br>

<h3><b>Dithering</b></h3><br>
<p align="justify">
<ul>
<li>Menghitung matriks treshold yang akan digunakan untuk membandingkan matriks</li>
<li>Setelah mendapatkan nilai matriks tresholdnya, bandingkan nilai yang ada pada matriks dengan nilai treshold.</li>
<li>Jika nilai matriks lebih besar dari treshold maka matriks akan bernilai 0 atau warna yang ditampiilkan adalah hitam.</li>
<li>Jika nilai matriks lebih kecil dari treshold maka matriks akan bernilai 1 atau berwarna putih.</li>
</ul><br>

<h3><b>Histogram Equalization</b></h3><br>
<p align="justify">
<ul>
<li>Menghitung seluruh nilai histogram</li>
<li>Menormalisasikan jumlah histogram dengan membaginya pada seluruh nilai histogram(jumlah pixel)</li>
<li>Mengalikan hasil normalisasi histogram dengan banyaknya level bit gambar kemudian dibagi dengan jumlah dari keseluruhan pixel</li>
<li>Menentukan jumlah masing-masing gray level dengan menjumlahkan number of pixel dengan gray level yang sama</li>
</ul><br>

<h3><b>Bit Plane Slicing</b></h3><br>
<p align="justify">
<ul>
<li>Mengubah setiap angka yang ada pada matriks menjadi bilangan biner.</li>
<li>Menyimpan nilai biner yang didapatkan dari matriks.</li>
<li>Tiap 1 buah angka yang ada pada matriks disimpan lagi ke dalam matriks baru sehingga terdapat 8 buah matriks baru dari bilangan biner yang sudah dihasilkan.</li>
<li>Bilangan biner yang berada di sisi paling kanan adalah less significant bit (LSB)</li>
<li>Bilangan biner yang berada di sisi paling kanan adalah most significant bit (MSB)</li>
</ul><br>