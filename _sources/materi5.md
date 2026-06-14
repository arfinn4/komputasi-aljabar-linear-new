# Materi 5: Materi tentang Determinan dan Invers Matriks
# E. Menentukan Determinan dan Invers dengan Ekspansi Baris dan Metode Adjoin

# Bagian 1: Menentukan Determinan dengan Ekspansi Baris
Metode ekspansi baris dilakukan dengan memilih satu baris atau kolom, kemudian menghitung jumlah hasil perkalian setiap elemen dengan kofaktornya.
Secara umum:

$
\det(A)=\sum_{j=1}^{n} a_{ij}C_{ij}
$

dengan:

$a_{ij}$ = elemen pada baris ke-$i$ dan kolom ke-$j$
$C_{ij}$ = kofaktor dari elemen $a_{ij}$

# Soal 1: Determinan Matriks Orde 2x2
Diberikan matriks:

$
A=
\begin{bmatrix}
-5 & -3\\
2 & 3
\end{bmatrix}
$

Untuk matriks berukuran $2x2$, determinan dihitung dengan rumus:

$
\det(A)=ad-bc
$

Substitusikan nilai matriks:

$
\det(A)=(-5)(3)-(-3)(2)
$

$
=-15+6
$

$
=-9
$

$Jadi, determinan matriks $A$ adalah $-9$

# Soal 2: Determinan Matriks Orde 3x3
Diberikan matriks:

$
B=
\begin{bmatrix}
1 & -3 & -2\\
0 & 3 & 1\\
1 & 2 & 3
\end{bmatrix}
$

Ekspansi dilakukan pada baris pertama:

$
=
1
\begin{vmatrix}
3 & 1\\
2 & 3
\end{vmatrix}$
$
-
(-3)
\begin{vmatrix}
0 & 1\\
1 & 3
\end{vmatrix}$
$
+
(-2)
\begin{vmatrix}
0 & 3\\
1 & 2
\end{vmatrix}
$

Hitung masing-masing minor:

$
=1(9-2)+3(0-1)-2(0-3)
$

$
=7-3+6
$

$
=10
$

Maka diperoleh $\det(B)=10$.

# Soal 3: Determinan Matriks Orde 4x4

Misalkan diberikan matriks:

$
C=
\begin{bmatrix}
2 & -2 & 0 & 0\\
-1 & 3 & 0 & 0\\
0 & 0 & 3 & -1\\
0 & 0 & 2 & 3
\end{bmatrix}
$

Karena banyak elemen nol, ekspansi dapat dilakukan lebih mudah pada baris atau kolom yang mengandung nol terbanyak.
Matriks tersebut dapat dipisahkan menjadi dua blok:

$
\begin{bmatrix}
2 & -2\\
-1 & 3
\end{bmatrix}
\quad \text{dan} \quad
\begin{bmatrix}
3 & -1\\
2 & 3
\end{bmatrix}
$

Determinan masing-masing blok:

$
(2)(3)-(-2)(-1)=6-2=4
$

$
(3)(3)-(-1)(2)=9+2=11
$

Sehingga:

$
\det(C)=4\times11=44
$

Jadi determinan matriks $C$ adalah 44

# Bagian 2: Menentukan Invers Matriks dengan Metode Adjoin
Jika suatu matriks persegi memiliki determinan tidak sama dengan nol, maka inversnya dapat dicari menggunakan rumus:

$A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)$

dengan:

$\det(A)$ adalah determinan matriks
$\operatorname{adj}(A)$ adalah matrik

# Soal 4: Invers Matriks Orde 2x2
Diketahui:

$
A=
\begin{bmatrix}
-5 & -3\\
2 & 3
\end{bmatrix}
$

Karena:

$
\det(A)=-9
$

maka invers matriksnya:

$A^{-1}
=
-\frac{1}{9}
\begin{bmatrix}
3 & 3\\
-2 & -5
\end{bmatrix}
=
\begin{bmatrix}
-\frac{1}{3} & -\frac{1}{3}\\
\frac{2}{9} & \frac{5}{9}
\end{bmatrix}$

Sehingga:

$A^{-1}
=
\begin{bmatrix}
-\frac{1}{3} & -\frac{1}{3} \\
\frac{2}{9} & \frac{5}{9}
\end{bmatrix}$

# Soal 5: Invers Matriks Orde 3x3
Gunakan matriks:

$
B=
\begin{bmatrix}
1 & -3 & -2\\
0 & 3 & 1\\
1 & 2 & 3
\end{bmatrix}
$

Langkah-langkah yang dilakukan:

- Hitung determinan matriks.
- Tentukan seluruh kofaktor.
- Susun matriks kofaktor.
- Transposkan matriks kofaktor untuk memperoleh adjoin.
- Kalikan adjoin dengan $\frac{1}{\det(B)}$

Dengan cara tersebut diperoleh invers matriks:

$B^{-1}
=
\begin{bmatrix}
\frac{7}{10} & \frac{1}{2} & \frac{3}{10} \\
-\frac{1}{10} & \frac{1}{2} & -\frac{1}{10} \\
-\frac{1}{2} & -\frac{1}{2} & \frac{3}{10}
\end{bmatrix}$

# Soal 6: Invers Matriks Orde 4x4

Untuk matriks orde $4x4$, prosedurnya sama:

- Cari determinan matriks.
- Hitung semua kofaktor.
- Bentuk matriks kofaktor.
- Transposkan menjadi matriks adjoin.
- Kalikan dengan $\frac{1}{\det(A)}$

Karena jumlah elemen yang lebih banyak, perhitungan invers matriks $4\times4$ biasanya cukup panjang sehingga lebih praktis menggunakan bantuan perangkat lunak seperti MATLAB, SageMath, NumPy, atau Octave.

# Verifikasi menggunakan script python (NumPy)
```
import numpy as np

matriks = {
    "A": np.array([
        [-5, -3],
        [ 2,  3]
    ]),
    
    "B": np.array([
        [ 1, -3, -2],
        [ 0,  3,  1],
        [ 1,  2,  3]
    ]),
    
    "C": np.array([
        [ 2, -2,  0,  0],
        [-1,  3,  0,  0],
        [ 0,  0,  3, -1],
        [ 0,  0,  2,  3]
    ])
}

for nama, M in matriks.items():
    print(f"\n=== Matriks {nama} ===")
    print(M)
    print("\nDeterminan:")
    print(round(np.linalg.det(M), 6))
    print("\nInvers:")
    print(np.linalg.inv(M))
```

# Link collab :
https://colab.research.google.com/drive/1B6IjdZCB4Iq4qWrMH5oH7gfXUEh5268e?usp=sharing
