# Materi 7: Transformasi Matriks dan Implementasinya pada Vektor 2D
# F. Transformasi Matriks dalam Implementasi Mesin Vektor 2D

# 1. Konsep Dasar Transformasi Matriks
Transformasi matriks adalah metode untuk mengubah posisi atau bentuk suatu vektor dengan menggunakan operasi matriks. Dalam grafika komputer, transformasi digunakan untuk memindahkan, memutar, memperbesar, atau mencerminkan objek.

Bentuk umum transformasi dapat dituliskan sebagai:

$
y = Ax
$

dengan:
$
- A adalah matriks transformasi,
- x adalah vektor awal,
- y adalah hasil transformasi.
$

Transformasi matriks memungkinkan perubahan koordinat dilakukan secara sistematis dan efisien.

# 2. Refleksi terhadap Sumbu Y
Refleksi terhadap sumbu Y merupakan proses pencerminan suatu titik terhadap garis sumbu Y. Pada transformasi ini, nilai koordinat $x$ berubah tanda, sedangkan koordinat $y$ tetap.

Matriks refleksi terhadap sumbu Y adalah:

$
R_y=
\begin{bmatrix}
-1 & 0\\
0 & 1
\end{bmatrix}
$

Jika suatu titik direpresentasikan sebagai vektor kolom, maka hasil refleksi diperoleh dengan mengalikan matriks refleksi dengan vektor tersebut.

# 3. Pembuktian Aljabar Linear pada Refleksi Sumbu Y
Misalkan terdapat titik:

$
v=
\begin{bmatrix}
x\\
y
\end{bmatrix}
$

Kemudian dilakukan transformasi menggunakan matriks refleksi:

$
R_y=
\begin{bmatrix}
-1 & 0\\
0 & 1
\end{bmatrix}
$

Maka:

$
R_y v=
\begin{bmatrix}
-1 & 0\\
0 & 1
\end{bmatrix}
\cbegin{bmatrix}
x\\
y
\end{bmatrix}
$


$\begin{bmatrix}
(-1)(x)+(0)(y)\\
(0)(x)+(1)(y)
\end{bmatrix}
$

$
\begin{bmatrix}
-x\\
y
\end{bmatrix}
$

Hasil tersebut menunjukkan bahwa koordinat $x$ berubah menjadi $-x$, sedangkan koordinat $y$ tetap. Dengan demikian, titik telah tercermin terhadap sumbu Y.

# 4. Contoh Perhitungan pada Satu Titik
Misalkan terdapat titik:

$
P=
\begin{bmatrix}
3\\
5
\end{bmatrix}
$

Lakukan refleksi terhadap sumbu Y.
Perhitungannya:

$
R_yP=
\begin{bmatrix}
-1 & 0\\
0 & 1
\end{bmatrix}
\begin{bmatrix}
3\\
5
\end{bmatrix}
=
\begin{bmatrix}
-3\\
5
\end{bmatrix}
$

Jadi, setelah dicerminkan terhadap sumbu Y, titik $(3,5)$ berubah menjadi $(-3,5)$

# 5. Implementasi Simultan pada Bentuk Geometri
Dalam grafika komputer, objek biasanya terdiri dari banyak titik yang saling terhubung membentuk suatu bangun. Oleh karena itu, transformasi dilakukan pada seluruh titik penyusun objek.

Sebagai contoh, sebuah segitiga memiliki titik-titik:

$
A(2,1), \quad B(4,3), \quad C(1,4)
$

Masing-masing titik direfleksikan terhadap sumbu Y:

$
A'(-2,1)
$

$
B'(-4,3)
$

$
C'(-1,4)
$

Dengan menghubungkan kembali titik-titik hasil refleksi tersebut, diperoleh bentuk segitiga baru yang merupakan bayangan cermin dari segitiga awal.

# 6. Analisis Karakteristik Matriks Refleksi
Beberapa sifat penting dari matriks refleksi adalah sebagai berikut:

# a. Determinan Bernilai -1
Determinan matriks refleksi terhadap sumbu Y adalah:

$
\det(R_y)=(-1)(1)-0(0)=-1
$

Nilai determinan negatif menunjukkan bahwa orientasi objek berubah setelah transformasi dilakukan.

# b. Panjang Vektor Tetap
Refleksi tidak mengubah ukuran atau panjang vektor. Yang berubah hanyalah posisi dan arahnya terhadap sumbu tertentu.

# c. Bentuk Objek Tidak Berubah
Walaupun posisi objek berpindah akibat pencerminan, ukuran dan bentuk objek tetap sama. Oleh karena itu, refleksi termasuk transformasi yang mempertahankan bentuk (isometri).

# cara Menjalankan Aplikasi Mesin Vektor 2D
Bagian ini menjelaskan langkah-langkah penggunaan aplikasi sederhana yang memanfaatkan transformasi matriks untuk memvisualisasikan perubahan posisi objek pada bidang dua dimensi.

# Deskripsi Sistem
Program dibuat menggunakan bahasa Python dan menampilkan objek grafis pada layar. Pengguna dapat melakukan beberapa operasi transformasi, seperti:

$
- Translasi (pergeseran),
- Rotasi (perputaran),
- Refleksi (pencerminan),
- Skala (perbesaran atau pengecilan)$

Setiap transformasi dihitung menggunakan operasi matriks sehingga hasilnya sesuai dengan teori aljabar linear.

# Kebutuhan Lingkungan Eksekusi
Sebelum menjalankan program, pastikan perangkat telah memenuhi kebutuhan berikut:

$
- Python versi 3.8 atau lebih baru.
- Pustaka NumPy untuk perhitungan matriks.
- Pustaka Pygame untuk menampilkan grafis.
- Sistem operasi Windows, Linux, atau macOS.
$

# Instalasi Dependensi
Untuk memasang pustaka yang diperlukan, jalankan perintah berikut pada terminal:

```
pip install numpy pygame
```

Setelah instalasi selesai, program siap dijalankan dan digunakan untuk mempelajari transformasi matriks pada objek dua dimensi secara interaktif.