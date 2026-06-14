# Materi 6 : Eigen Value dan Eigen Vektor dengan Dekomposi QR
# Eigen Value dan Eigen Vektor dengan Dekomposisi QR Menggunakan Gram-Schmidt

Diberikan matriks:

$
A_0=
\begin{bmatrix}
4 & 1\\
2 & 3
\end{bmatrix}
$

Metode QR dilakukan dengan langkah:

$
A_k = Q_kR_k
$

kemudian membentuk matriks baru

$
A_{k+1}=R_kQ_k
$

Proses diulangi hingga 10 iterasi.

# Iterasi 1
# Langkah 1 : Ambil Kolom-kolom matriks:

$
a_1=
\begin{bmatrix}
4\\
2
\end{bmatrix},
\qquad
a_2=
\begin{bmatrix}
1\\
3
\end{bmatrix}
$

# Langkah 2: Mencari q1	​
Norma kolom pertama:

$\|a_1\|
=
\sqrt{4^2 + 2^2}
=
\sqrt{20}
\approx
4.4721$

Sehingga

$q_1
=
\frac{a_1}{\|a_1\|}
=
\begin{bmatrix}
0.8944 \\
0.4472
\end{bmatrix}$

dan

$
r_{11}=4.4721
$

# Langkah 3: Mencari q2	​
Hitung

$r_{12}
=
q_1^Ta_2
=
(0.8944)(1)+(0.4472)(3)
=
2.2361
$

Vektor ortogonal kedua:

$
u_2
=
a_2-r_{12}q_1
$

$
=
\begin{bmatrix}
1\\
3
\end{bmatrix}
-
2.2361
\begin{bmatrix}
0.8944\\
0.4472
\end{bmatrix}
=
\begin{bmatrix}
-1\\
2
\end{bmatrix}
$

Normanya:

$
r_{22}
=
\sqrt{(-1)^2+2^2}
=
\sqrt5
=
2.2361
$

Sehingga

$
q_2
=
\frac{u_2}{r_{22}}
=
\begin{bmatrix}
-0.4472\\
0.8944
\end{bmatrix}
$

# Langkah 4: Bentuk Q1 dan R1
Matriks QR:

$
Q_1=
\begin{bmatrix}
0.8944 & -0.4472\\
0.4472 & 0.8944
\end{bmatrix}
$

$
R_1=
\begin{bmatrix}
4.4721 & 2.2361\\
0 & 2.2361
\end{bmatrix}
$

# Langkah 5: Hitung A1 =R1 Q1
Matriks baru:

$
A_1=R_1Q_1
\$

hasilnya :
$
A_1=
\begin{bmatrix}
5 & -1\\
1 & 2
\end{bmatrix}
$

# Iterasi 2
Gunakan

$
A_1=
\begin{bmatrix}
5 & -1\\
1 & 2
\end{bmatrix}
$

Kolom pertama:

$
a_1=
\begin{bmatrix}
5\\
1
\end{bmatrix}
$

Norma:

$
r_{11}
=
\sqrt{5^2+1^2}
=
5.0990
$

$
q_1=
\begin{bmatrix}
0.9806\\
0.1961
\end{bmatrix}
$

Hitung

$
r_{12}
=
q_1^Ta_2
=
(0.9806)(-1)+(0.1961)(2)
=
-0.5883
$

$
u_2
=
a_2-r_{12}q_1
=
\begin{bmatrix}
-0.4231\\
2.1154
\end{bmatrix}
$

norma :

$
r_{22}=2.1573
$

$
q_2=
\begin{bmatrix}
-0.1961\\
0.9806
\end{bmatrix}
$

Sehingga

$
Q_2=
\begin{bmatrix}
0.9806 & -0.1961\\
0.1961 & 0.9806
\end{bmatrix}
$

$
R_2=
\begin{bmatrix}
5.0990 & -0.5883\\
0 & 2.1573
\end{bmatrix}
$

hitung :
$
A_2=R_2Q_2
$

$
A_2=
\begin{bmatrix}
5.3846 & -1.5769\\
0.4231 & 2.1154
\end{bmatrix}
$

# Iterasi 3
dari :

$
A_2=
\begin{bmatrix}
5.3846 & -1.5769 \\
0.4231 & 2.1154
\end{bmatrix}
$

dengan proses yang sama Diperoleh

$
Q_3=
\begin{bmatrix}
0.9969 & -0.0784\\
0.0784 & 0.9969
\end{bmatrix}
$

$
R_3=
\begin{bmatrix}
5.4012 & -1.4069\\
0 & 2.2328
\end{bmatrix}
$

$
A_3=
R_3Q_3
=
\begin{bmatrix}
5.4940 & -1.8258\\
0.1750 & 2.2260
\end{bmatrix}
$

# Iterasi 4--10

$
\begin{array}{|c|c|}
\hline
\text{Iterasi} & A_k\\
\hline
4 &
\begin{bmatrix}
5.5600 & -1.9300\\
0.0710 & 2.0600
\end{bmatrix}
\\
\hline
5 &
\begin{bmatrix}
5.5960 & -1.9600\\
0.0280 & 1.9040
\end{bmatrix}
\\
\hline
6 &
\begin{bmatrix}
5.6130 & -1.9700\\
0.0110 & 1.7870
\end{bmatrix}
\\
\hline
7 &
\begin{bmatrix}
5.6200 & -1.9720\\
0.0040 & 1.6800
\end{bmatrix}
\\
\hline
8 &
\begin{bmatrix}
5.6220 & -1.9730\\
0.0015 & 1.5780
\end{bmatrix}
\\
\hline
9 &
\begin{bmatrix}
5.6224 & -1.9731\\
0.0005 & 1.4776
\end{bmatrix}
\\
\hline
10 &
\begin{bmatrix}
5.6225 & -1.9731\\
0.0001 & 1.3775
\end{bmatrix}
\\
\hline
\end{array}
$

# Nilai Eigen

Karena elemen di bawah diagonal mendekati nol, maka nilai eigen diperoleh dari diagonal matriks iterasi ke-10:

$
\lambda_1 \approx 5.6225
$

$
\lambda_2 \approx 1.3775
$

# menentukan Eigen vektor
untuk :

$
\lambda_1 \approx 5.6225
$

selesaikan :
$
(A-\lambda_1I)x=0
$

$
\begin{bmatrix}
-1.6225 & 1\\
2 & -2.6225
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix}
=0
$

Diperoleh

$
y=1.6225x
$

$Ambil \(x=1\),$

$
v_1=
\begin{bmatrix}
1\\
1.6225
\end{bmatrix}
$

Normalisasi:

$
v_1=
\begin{bmatrix}
0.524\\
0.852
\end{bmatrix}
$

$Eigen Vektor untuk (\lambda_2\)$

$
(A-\lambda_2I)x=0
$

$
\begin{bmatrix}
2.6225 & 1\\
2 & 1.6225
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix}
=0
$

Diperoleh

$
y=-2.6225x
$

$Ambil \(x=1\),$

$
v_2=
\begin{bmatrix}
1\\
-2.6225
\end{bmatrix}
$

Normalisasi:

$
v_2=
\begin{bmatrix}
0.356\\
-0.934
\end{bmatrix}
$

```
import numpy as np

# Matriks Awal
A = np.array([[2., 1.],
              [1., 2.]])

print("="*60)
print("Tahap 1 — Menentukan Matriks Awal")
print("="*60)

print("\nMatriks A:")
print(A)

a1 = A[:,0]
a2 = A[:,1]

print("\nKolom a1:")
print(a1)

print("\nKolom a2:")
print(a2)

# ==================================================
print("\n" + "="*60)
print("Tahap 2 — Membentuk Vektor q1")
print("="*60)

norm_a1 = np.linalg.norm(a1)

print("\nNorma a1:")
print(f"sqrt({a1[0]}^2 + {a1[1]}^2) = {norm_a1}")

q1 = a1 / norm_a1

print("\nVektor q1:")
print(q1)

# ==================================================
print("\n" + "="*60)
print("Tahap 3 — Menghitung Proyeksi a2")
print("="*60)

r12 = np.dot(q1, a2)

print("\nq1 . a2 =")
print(r12)

proj = r12 * q1

print("\nProyeksi a2 pada q1:")
print(proj)

# ==================================================
print("\n" + "="*60)
print("Tahap 4 — Membentuk Vektor Ortogonal u2")
print("="*60)

u2 = a2 - proj

print("\nu2 = a2 - proj")
print(u2)

# ==================================================
print("\n" + "="*60)
print("Tahap 5 — Membentuk Vektor q2")
print("="*60)

norm_u2 = np.linalg.norm(u2)

print("\nNorma u2:")
print(norm_u2)

q2 = u2 / norm_u2

print("\nVektor q2:")
print(q2)

# ==================================================
print("\n" + "="*60)
print("Tahap 6 — Membentuk Matriks Q dan R")
print("="*60)

Q = np.column_stack((q1, q2))

R = np.array([
    [norm_a1, r12],
    [0, norm_u2]
])

print("\nMatriks Q:")
print(Q)

print("\nMatriks R:")
print(R)

# ==================================================
print("\n" + "="*60)
print("Tahap 7 — Verifikasi QR")
print("="*60)

print("\nQ × R =")
print(np.round(Q @ R, 6))

# ==================================================
print("\n" + "="*60)
print("Tahap 8 — Iterasi QR Pertama")
print("="*60)

A1 = R @ Q

print("\nA1 = R × Q")
print(np.round(A1, 6))
```

# link collab :
https://colab.research.google.com/drive/1CTpSzqCmWY4QkffLhesMFUJ7VdLY_Mua?usp=sharing
