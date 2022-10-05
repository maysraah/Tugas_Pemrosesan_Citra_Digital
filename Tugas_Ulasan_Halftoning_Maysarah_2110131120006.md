Nama: Maysarah<br>
NIM: 2110131120006<br><br>

<h1 align="center"><b>ULASAN TENTANG HALFTONING, PATTERNING DAN DITHERING</b></h1><br>


<h3><b>Halftoning</b></h3>
<p align="justify">
Halftoning atau halftoning analog adalah proses yang mensimulasikan nuansa abu-abu dengan memvariasikan ukuran titik-titik hitam kecil yang diatur dalam pola yang teratur. Teknik ini digunakan dalam printer, serta industri penerbitan. Jika Anda memeriksa sebuah foto di koran, Anda akan melihat bahwa gambar itu terdiri dari titik-titik hitam meskipun tampaknya terdiri dari abu-abu. Hal ini dimungkinkan karena integrasi spasial yang dilakukan oleh mata kita. Mata kita memadukan detail halus dan merekam intensitas keseluruhan.</p><br>

<p align="center"><img src="img_ulasan/1.jpeg"><br>Contoh Halftoning</p><br>

Tiga metode umum untuk menghasilkan gambar halftoning digital adalah:
<ol>
<li>patterning</li>
<li>dithering</li>
<li>error diffusion</li>
</ol><br>

<h3><b>Patterning</b></h3>
<p align="justify">
Patterning (Pola) adalah yang paling sederhana dari tiga teknik untuk menghasilkan gambar halftoning digital. Ini menghasilkan gambar yang memiliki resolusi spasial lebih tinggi daripada gambar sumber. Jumlah sel halftone citra keluaran sama dengan jumlah piksel citra sumber. Namun, setiap sel halftone dibagi lagi menjadi kotak 4x4. Setiap nilai piksel input diwakili oleh jumlah kotak terisi yang berbeda dalam sel halftone. Karena kisi 4x4 hanya dapat mewakili 17 tingkat intensitas yang berbeda, gambar sumber harus dikuantisasi. Gambar di bawah menunjukkan matriks pola rekursif Rylander.</p><br>

<p align="center"><img src="img_ulasan/2.jpeg"><br>Matriks pola rekursif Rylander</p><br>

<p align="center"><img src="img_ulasan/3.jpeg"><br>Operasi Patterning</p><br>

<p align="justify">
Pattern menghasilkan gambar halftoning digital dari gambar input menggunakan teknik pola. Pola program membaca gambar input, mengkuantisasi nilai piksel, dan memetakan setiap piksel ke pola yang sesuai. Gambar yang dihasilkan 16 kali lebih besar dari aslinya. Gambar yang dihasilkan ditulis ke file output sebagai file TIFF. Sebuah kata peringatan: "pola" membutuhkan banyak perhitungan, gambar berukuran kurang dari 100x100 direkomendasikan.<br> Contoh ini menghasilkan gambar halftoning digital dari PAINTER menggunakan teknik pola</p><br>

<p align="center"><img src="img_ulasan/4.jpeg"><br>Gambar halftoning digital PAINTER melalui pola</p><br>

<h3><b>Dithering</b></h3>
<p align="justify">
Teknik lain yang digunakan untuk menghasilkan gambar halftoning digital adalah dithering. Tidak seperti pola, dithering membuat gambar keluaran dengan jumlah titik yang sama dengan jumlah piksel pada gambar sumber. Dithering dapat dianggap sebagai thresholding gambar sumber dengan matriks gentar. Matriks diletakkan berulang kali di atas gambar sumber. Dimanapun nilai piksel gambar lebih besar dari nilai dalam matriks, titik pada gambar output diisi. Gambar dibawah menunjukkan contoh operasi dithering.</p><br>

<p align="center"><img src="img_ulasan/5.jpeg"></p><br><br>

# Cara Menentukan Pola dari Patterning dan Dithering

- Patterning

 <p align="justify">
 Untuk menentukan banyaknya pola pada patterning kita bisa mengetahui secara langsung dengan menghitung banyaknya font biner atau pattern pengganti terlebih dahulu kemudian ditambahkan dengan 1.<br>
 Misalkan dari 4 x 4 font biner dapat menghasilkan 17 pola yang berbeda.<br>
 Pola yang ada pada patterning tidak boleh sama antara satu sama lain.</p>

 <p align="center"><img src="img_ulasan/2.jpeg"></p><br><br>

 - Dithering

<p align="justify">
 Karena sistem visual manusia cenderung meratakan suatu area di sekitar piksel,
bukan melihat setiap piksel secara sendiri-sendiri, sehingga memungkinkan untuk
membuat ilusi dari beberapa tingkat keabuan di dalam sebuah citra biner yang dalam
kenyataanya hanya terdiri dari dua tingkat abu-abu.<br><br>
Untuk sebagian besar tujuan dithering, cukup menambahkan nilai ambang batas ke setiap piksel (tanpa melakukan normalisasi dengan mengurangi 1⁄2), atau secara setara, untuk membandingkan nilai piksel dengan ambang batas: jika nilai kecerahan piksel <b>kurang dari</b> nomor di sel matriks yang sesuai, plot piksel itu <b>hitam</b>, jika <b>tidak</b>, plot <b>putih.</b></p>

<p align="center"><img src="img_ulasan/5.jpeg"></p><br><br>

# Cara Menentukan Matriks Dither (Matriks Threshold)

<p align="justify">
Thresholding merupakan salah satu metode segmentasi citra di mana prosesnya didasarkan pada perbedaan derajat keabuan citra. Dalam proses ini dibutuhkan suatu nilai batas yang disebut nilai threshold. <br><br>
Nilai intensitas citra yang lebih dari atau sama dengan nilai threshold akan diubah menjadi 1 (berwarna putih) sedangkan nilai intensitas citra yang kurang dari nilai threshold akan diubah menjadi 0 (berwana hitam). Sehingga citra keluaran dari hasil thresholding adalah berupa citra biner.</p>

<p align="justify">
Persamaan yang digunakan untuk mengkonversi nilai piksel citra grayscale menjadi biner pada metode thresholding adalah:</p>

<p align="center"><img src="img_ulasan/6.jpeg"></p><br>

di mana<br>
f(x,y) adalah citra grayscale<br>
g(x,y) adalah citra biner<br>
T adalah nilai threshold<br><br>

# Mengapa hasil dithering dengan matriks 2x2 tidak sebagus hasil matriks dither 16x16

<p align="justify">
Perbedaan antara keluaran yang dihasilkan antara citra menggunakan 4x4 matriks dithering dan 16x16 matriks dithering terletak pada sensitifitas nilai piksel aslinya. Citra yang dihasilkan dari penggunaaan matriks 4x4 memiliki pola halftone yang kurang dibandingkan dengan citra yang diproses menggunakan matriks dithering 16x16. Karena itu hasil dari citra dengan 4x4 matriks dithering memiliki banyak daerah dengan pola yang sama, sehingga hasil yang ditampilkan menjadi kurang baik dibandingkan dithering dengan matriks 16x16.</p>









