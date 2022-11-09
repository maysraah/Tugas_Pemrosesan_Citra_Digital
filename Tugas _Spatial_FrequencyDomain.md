Nama : Maysarah<br>
NIM : 2110131120006<br><br>

<h1 align="center">METODE SPASIAL DAN FREKUENSI DOMAIN</h1><br><br>

<p align="justify">Teknik peningkatan mutu/kualitas citra dapat dibagi menjadi dua yaitu:
<ol>
<li>Peningkatan mutu citra pada domain spasial</li>
<li>Peningkatan mutu citra pada domain frekuensi</li></ol></p><br>

**Domain Spasial**

<p align="justify">Adalah proses manipulasi kumpulan piksel dari sebuah citra secara langsung untuk menghasilkan citra baru.</p>

<p align="center"><img src="img_spasialfrekuensidomain/1.jpeg"></p><br>

**Domain Frekuensi**

<p align="justify">Adalah teknik pemrosesan yang didasarkan pada
manipulasi terhadap transformasi Fourier dari suatu citra.<br>
Tranformasi Fourier merupakan suatu proses untuk mengubah domain spasial menjadi domain frekuensi.</p>

<p align="center"><img src="img_spasialfrekuensidomain/2.jpeg"></p><br>

## **METODE SPASIAL DOMAIN**

<p align="justify">Peningkatan mutu citra pada domain spesial terbagi menjadi dua yaitu Point Processing dan Mask Processing.</p>

**1. Point Processing**

<p align="justify">Cara paling mudah untuk peningkatan mutu pada domain spasial adalah dengan melakukan pemrosesan yang hanya melibatkan satu piksel saja, tanpa menggunakan jendela ketetanggaan. 

- Citra Negatif<br>
Mengubah nilai grey-level piksel citra input dengan:

    Gbaru = 255 - Glama <br>
Hasilnya seperti klise foto<br><br>
<img src="img_spasialfrekuensidomain/3.jpeg"><br><br>

- Contrast Streching<br>
Mengubah kontras dari suatu image dengan cara mengubah greylevel piksel-piksel pada citra menurut fungsi s = T(r) tertentu

    r1 <= r2, s1 <= s2<br>
    r1 = r2, s1 = s2 --> tidak ada perubahan<br>
    r1 = r2, s1 = 0, s2 = 255 --> tresholding menjadi citra biner dengan ambang r1<br><br>
<img src="img_spasialfrekuensidomain/4.jpeg"><br>
<img src="img_spasialfrekuensidomain/5.jpeg"><br><br>

- Histogram Equalization<br>
Histogram processing : mengubah bentuk histogram agar pemerataan gray level pada citra juga berubah<br>
<img src="img_spasialfrekuensidomain/6.jpeg"><br>
<img src="img_spasialfrekuensidomain/7.jpeg"><br><br>

- Image Substraction<br>
Dilakukan jika ingin mengambil bagian tertentu dari citra.<br>
<img src="img_spasialfrekuensidomain/8.jpeg"><br><br>

- Image Averaging<br>
Dilakukan jika ada beberapa citra yang bergambar sama, namun semua citra memiliki noise (gangguan) dan noisenya berbeda satu sama lain (tidak berkorelasi). Cara memperbaikinya adalah dengan melakukan operasi rata-rata terhadap semua citra tersebut.<br><br>
<img src="img_spasialfrekuensidomain/9.jpeg"><br><br>

**2. Mask Processing**

<p align="justify"> Melakukan operasi terhadap suatu jendela ketetanggaan pada citra. Lalu menerapkan suatu <i>mask</i> terhadap jendela tersebut. <i>Mask</i> sering juga disebut <i>filter.</i><br><br>
<img src="img_spasialfrekuensidomain/10.jpeg"><br><br>















