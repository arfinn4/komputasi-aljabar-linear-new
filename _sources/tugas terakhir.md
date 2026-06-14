# Tugas Singular Value Decomposition (SVD) pada Kompresi Citra
# SVD Eigentface
https://colab.research.google.com/drive/1z4moT04MU3egMHzWTHW5TgDzFPlFPd7F?usp=sharing

# Hasil Output Program Face Recognition Menggunakan EigenFace dan SVD
Pada program:
```
U, S, VT = np.linalg.svd(
    A,
    full_matrices=False
)
```

diperoleh output seperti:

```
Dataset ditemukan di: ./dataset

Loading dataset...
Andi -> 10 gambar
Budi -> 10 gambar
Citra -> 10 gambar

Shape faces : (30, 10000)
Jumlah label : 30

Shape A : (30, 10000)

Menghitung SVD...
Jumlah EigenFace : 20

Training selesai

FACE RECOGNITION
Orang paling mirip : Andi
Distance : 128.45
```

Artinya sistem berhasil melakukan proses Face Recognition menggunakan metode EigenFace berbasis Singular Value Decomposition (SVD).

# Tujuan utama metode EigenFace adalah:
$
\begin{itemize}
\item Mengekstraksi ciri-ciri penting wajah.
\item Mengurangi dimensi data wajah.
\item Mengenali identitas seseorang dari gambar wajah.
\end{itemize}$

# Membaca Dataset Wajah
Saat program dijalankan, setiap gambar dibaca dalam bentuk grayscale.
Ukuran gambar yang digunakan adalah:

$
100x100
$

Artinya:
$
\item Lebar = 100 piksel
\item Tinggi = 100 piksel
$

Jumlah piksel:

$
100x100 = 10000
$

Setiap gambar wajah direpresentasikan sebagai 10000 nilai intensitas piksel.

# Mengubah Gambar Menjadi Vektor

Gambar berukuran $100x100$ diubah menjadi vektor satu dimensi.

Contoh:

$
\begin{bmatrix}
10 & 20\\
30 & 40
\end{bmatrix}
\rightarrow
[10,20,30,40]
$

Untuk gambar wajah:

$
100x100 = 10000
$

maka setiap wajah direpresentasikan sebagai:

$
x_i = (1x10000)
$

# Membentuk Matriks Wajah
Setelah seluruh gambar dibaca, diperoleh output:

```
Shape faces : (30,10000)
```

Artinya matriks data wajah:

$
X = (30x10000)
$

dengan:
$
\begin{itemize}
\item 30 baris = jumlah gambar wajah
\item 10000 kolom = jumlah piksel
\end{itemize}$

Setiap baris mewakili satu wajah.

# Menghitung Mean Face
Wajah rata-rata dihitung menggunakan:

$
\mu =
\frac{1}{N}
\sum_{i=1}^{N} x_i
$

dengan:
$
\begin{itemize}
\item N = jumlah gambar
\item x_i = wajah ke-i
\end{itemize}$

Mean Face digunakan sebagai wajah rata-rata seluruh dataset.

# Membentuk Matriks A
Setiap wajah dikurangi dengan wajah rata-rata:

$
A = X - \mu
$

Output:
```
Shape A : (30,10000)
```

Tujuannya adalah menghilangkan informasi umum dan menyisakan karakteristik unik setiap wajah.

# Tujuan Dilakukan SVD
Metode EigenFace menggunakan dekomposisi:
$
A = U\Sigma V^T
$

untuk memecah data wajah menjadi beberapa komponen utama.

$
\begin{center}
\begin{tabular}{|c|c|}
\hline
Matriks & Fungsi \\
\hline
u & Hubungan antar gambar wajah \\
\Sigma & Tingkat kepentingan fitur \\
V^T & EigenFace \\
\hline
\end{tabular}
\end{center}$

Secara sederhana:

$\begin{itemize}
\item U = pola kemunculan wajah
\item \Sigma = kekuatan informasi
\item V^T = ciri-ciri utama wajah
\end{itemize}$

# Menghitung SVD

Misalkan:

$
A=(30 \times 10000)
$

Maka hasil SVD:

$
U=(30 \times 30)
$

$
S=(30)
$

$
V^T=(30 \times 10000)
$

SVD digunakan untuk menemukan arah variasi terbesar pada kumpulan wajah.

# Singular Value
Singular value diperoleh dalam bentuk:

$
S =
[\sigma_1,\sigma_2,\sigma_3,\ldots,\sigma_n]
$

Nilai singular menunjukkan tingkat kepentingan suatu fitur wajah.

Semakin besar nilai:

$
\sigma_i
$

maka semakin penting fitur tersebut.

# Membentuk EigenFace

Program menggunakan:
```
eigenfaces = VT[:20]
```

Output:

```
Jumlah EigenFace : 20
```

Artinya hanya 20 komponen terpenting yang digunakan.
Secara matematis:

$
E=
\begin{bmatrix}
e_1\\
e_2\\
e_3\\
\vdots\\
e_{20}
\end{bmatrix}
$

Setiap $e_i$ disebut EigenFace.
EigenFace menyimpan informasi penting seperti:

$\begin{itemize}
\item Bentuk mata
\item Bentuk hidung
\item Bentuk mulut
\item Kontur wajah
\item Pencahayaan
\end{itemize}$

# Menampilkan EigenFace
EigenFace yang ditampilkan bukan wajah asli seseorang.
EigenFace merupakan pola matematis hasil kombinasi seluruh wajah pada dataset.
Biasanya terlihat sebagai bayangan wajah hitam putih yang samar.

# Mengubah Wajah Menjadi Weight
Setiap wajah diproyeksikan ke ruang EigenFace:

$
w = Ex
$

dengan:
$
\begin{itemize}
\item E = EigenFace
\item X = wajah
\end{itemize}$

Hasilnya:

$
w =
[w_1,w_2,w_3,\ldots,w_{20}]
#
$

Weight vector digunakan sebagai representasi wajah.

# Training Selesai

Output:

```
Training selesai
```

Artinya seluruh wajah training berhasil diubah menjadi weight vector.
Sistem tidak lagi membandingkan gambar asli, tetapi membandingkan weight vector yang jauh lebih kecil dimensinya.

# Memproses Gambar Test
Gambar uji diproyeksikan ke ruang EigenFace:

$
w_{test}=E x_{test}
$

Hasilnya adalah weight vector dari wajah yang akan dikenali.

# Menghitung Jarak Kemiripan
Kemiripan dihitung menggunakan jarak Euclidean:

$
d=
\sqrt{
\sum_{i=1}^{n}
(x_i-y_i)^2
}
$

Semakin kecil nilai $d$, maka semakin mirip kedua wajah.

# Menentukan Wajah Terdekat
Sistem mencari nilai jarak terkecil:

$
\text{best}
=
\arg\min(d_i)
$

Contoh:

$\begin{center}
\begin{tabular}{|c|c|}
\hline
Orang & Distance \\
\hline
Andi & 128 \\
Budi & 310 \\
Citra & 275 \\
\hline
\end{tabular}
\end{center}$

Karena nilai terkecil dimiliki Andi, maka wajah tersebut dipilih sebagai hasil pengenalan.

# Hasil Face Recognition

Output:

```
FACE RECOGNITION

Orang paling mirip : Andi

Distance : 128.45
```

Artinya gambar test memiliki kemiripan tertinggi dengan wajah milik Andi pada dataset.
Nilai distance sebesar:

$
128.45
$

menunjukkan tingkat kemiripan hasil pencocokan.
Semakin mendekati nol, maka wajah semakin mirip.

# Alur Lengkap Face Recognition dengan EigenFace

$\begin{enumerate}
\item Membaca seluruh gambar wajah.
\item Resize menjadi 100x100
\item Mengubah gambar menjadi vektor 10000 piksel.
\item Menghitung Mean Face.
\item Membentuk matriks:
\[
A = X - \mu
\]
\item Menghitung SVD:
\[
A = U\Sigma V^T
\]
\item Mengambil 20 EigenFace.
\item Memproyeksikan data training menjadi weight vector.
\item Memproyeksikan gambar test menjadi weight vector.
\item Menghitung jarak Euclidean.
\item Mencari jarak terkecil.
\item Menampilkan identitas wajah yang paling mirip.
\end{enumerate}
$

# Kesimpulan
Metode EigenFace berbasis Singular Value Decomposition (SVD) digunakan untuk mengekstraksi fitur-fitur penting dari wajah dan mengurangi dimensi data dari 10000 piksel menjadi 20 komponen utama (EigenFace). Setiap wajah kemudian direpresentasikan dalam bentuk weight vector dan dibandingkan menggunakan jarak Euclidean. Wajah dengan jarak terkecil terhadap gambar uji dianggap sebagai wajah yang paling mirip dan ditampilkan sebagai hasil pengenalan wajah. Dengan cara ini, proses identifikasi menjadi lebih cepat, efisien, dan tetap mampu mempertahankan karakteristik utama wajah.