# Materi 1 : Pengantar Materi KAL

# A. Apa yang dimaksud dengan Aljabar Linear ?
Aljabar Linear adalah cabang matematika yang mempelajari cara mengolah dan menganalisis angka-angka yang disusun dalam bentuk tabel (matriks) serta besaran yang memiliki nilai dan arah (vektor) untuk menyelesaikan berbagai masalah.

# Definisi Aljabar Linear
Aljabar linear adalah cabang matematika yang mempelajari cara menyelesaikan masalah menggunakan angka-angka yang disusun dalam bentuk tabel (matriks) dan persamaan sederhana yang memiliki hubungan satu sama lain.

# Contoh Kasusnya(Representasi Geometris Geogebra)
Misalkan kita memiliki dua persamaan linear:

$\begin{aligned}
x + y &= 4 \\
x - y &= 2
\end{aligned}$

Representasi Geometris
Di GeoGebra, kedua persamaan tersebut akan digambar sebagai dua garis lurus.

Garis pertama : $x+y=4$
Garis kedua : $x−y=2$

Kedua garis akan berpotongan di satu titik.

Untuk mencari titik potongnya:
1. Jumlahkan kedua persamaan:

$\begin{aligned}
(x+y) + (x-y) &= 4 + 2 \\
2x &= 6 \\
x &= 3
\end{aligned}$


2. Substitusikan x=3 ke persamaan pertama:

$
\begin{aligned}
3 + y &= 4 \\
y &= 1
\end{aligned}
$

Jadi titik potongnya adalah :
$(3,1)$

Makna Geometris
- Setiap garis menunjukkan semua pasangan (x,y) yang memenuhi persamaan tersebut.
- Titik perpotongan (3,1) adalah solusi dari kedua persamaan sekaligus.
- Dalam aljabar linear, solusi sistem persamaan linear dapat dilihat secara visual sebagai titik pertemuan dua garis.

# Gambar
![alt text](image1.png)

GeoGebra menampilkan titik potong (3, 1) yang merupakan solusi dari sistem persamaan linear tersebut.

Kesimpulan: Pada representasi geometris di GeoGebra, aljabar linear dapat divisualisasikan sebagai garis-garis yang berpotongan. Titik potong tersebut menunjukkan solusi dari sistem persamaan linear.

# Bukti Komputasi Numerik Menggunakan Python (NumPy)
```
import numpy as np

# Matriks koefisien
A = np.array([[1, 1],
              [1, -1]])

# Vektor konstanta
B = np.array([4, 2])

# Mencari solusi
X = np.linalg.solve(A, B)

print("Nilai x =", X[0])
print("Nilai y =", X[1])
```

# Link Collab :
https://colab.research.google.com/drive/1MMR1lmKsOMnRD4SXlqpelPUuI7dCcdY4?usp=sharing