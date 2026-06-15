# Perhitungan Determinan dan Invers
# Soal

## 1.Hitunglah determinan matriks berikut dengan menggunakan rumus ekspansi baris

$
\det(A)=\sum_{k=1}^{n} (-1)^{i+k} a_{ik} M_{ik}
$

dengan $M_{ij}$ merupakan minor dari matriks $A$, yaitu

$
M_{ij}=\det(A_{ij})
$

di mana $A_{ij}$ adalah submatriks yang diperoleh dengan menghapus baris ke-$i$ dan kolom ke-$j$ dari matriks $A$, dengan

$
1 \leq i,j \leq n.
$

# 1. Matriks 2×2 (Determinan)
matriks :

$A=
\begin{bmatrix}
3 & 2\\
1 & 4
\end{bmatrix}$

Hitung determinan dengan ekspansi baris pertama :

$
\begin{aligned}
\det(A) &= 3(4) - 2(1) \\
        &= 12 - 2 \\
        &= 10
\end{aligned}$

$=3(4)-2(1)$

$=12-2$

$\boxed{\det(A)=10}$
 
# 2. Matriks 3x3 (Determinan)
Diberikan matriks :

$A=
\begin{bmatrix}
1 & 2 & 3\\
0 & 4 & 5\\
1 & 0 & 6
\end{bmatrix}$

Ekspansi pada baris pertama:

$\det(A)=1$

$\begin{vmatrix}
4 & 5 \\
0 & 6
\end{vmatrix}
-2
\begin{vmatrix}
0 & 5 \\
1 & 6
\end{vmatrix}
+3
\begin{vmatrix}
0 & 4 \\
1 & 0
\end{vmatrix}$

Hitung masing-masing minor ;

$
\det(A)=1$

$\begin{vmatrix}
4 & 5\\
0 & 6
\end{vmatrix}
-
2
\begin{vmatrix}
0 & 5\\
1 & 6
\end{vmatrix}
+
3
\begin{vmatrix}
0 & 4\\
1 & 0
\end{vmatrix}$

substitusi :

$
\det(A)=
1(24)-2(-5)+3(-4)
$

24+10-12

$
\boxed{\det(A)=22}
$

# 3. Matriks 4x4 (Determinan)
Diberikan matriks :

$
A=
\begin{bmatrix}
1 & 2 & 0 & 1\\
3 & 1 & 2 & 0\\
0 & 4 & 1 & 2\\
1 & 0 & 3 & 1
\end{bmatrix}
$

Ekspansi pada baris pertama:

$\det(A)=1M_{11}-2M_{12}+0M_{13}-1M_{14}$

minor pertama :

$M_{11}=
\begin{vmatrix}
1 & 2 & 0 \\
4 & 1 & 2 \\
0 & 3 & 1
\end{vmatrix}$

minor kedua :

$\begin{aligned}
M_{12}
&=
\begin{vmatrix}
3 & 2 & 0 \\
0 & 1 & 2 \\
1 & 3 & 1
\end{vmatrix}
\end{aligned}$

minor keempat :

$\begin{aligned}
M_{14}
&=
\begin{vmatrix}
3 & 1 & 2 \\
0 & 4 & 1 \\
1 & 0 & 3
\end{vmatrix}
\end{aligned}$

Sehingga

$\begin{aligned}
\det(A)
&= 1M_{11}-2M_{12}+0M_{13}-1M_{14} \\
&= 1(-13)-2(-11)+0-1(29) \\
&= -13+22-29 \\
&= 9-29 \\
&= -20
\end{aligned}$

$
\boxed{\det(A)=-20}
$

# 4. Matriks 2x2 (Invers)
Diberikan matriks

$
A=
\begin{bmatrix}
2 & 1\\
3 & 4
\end{bmatrix}
$

Determinan:

$\begin{aligned}
\det(A)
&= (2)(4) - (1)(3) \\
&= 8 - 3 \\
&= 5
\end{aligned}$

Rumus invers matriks 2x2:

A^{-1}
=
$\frac{1}{ad-bc}
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}$

Substitusi nilai:

$=\frac{1}{5}
\begin{bmatrix}
4 & -1 \\
-3 & 2
\end{bmatrix}$

A^{-1}
=
$\begin{bmatrix}
\frac{4}{5} & -\frac{1}{5} \\
-\frac{3}{5} & \frac{2}{5}
\end{bmatrix}$

# 5. Matriks 3X3 (Invers)
Diberikan matriks

$
A=
\begin{bmatrix}
1 & 2 & 1\\
0 & 1 & 1\\
2 & 3 & 4
\end{bmatrix}
$

# Langkah 1 : Menentukan Determinan

$\begin{aligned}
\det(A)
&=
1
\begin{vmatrix}
1 & 1 \\
3 & 4
\end{vmatrix}
-2
\begin{vmatrix}
0 & 1 \\
2 & 4
\end{vmatrix}
+1
\begin{vmatrix}
0 & 1 \\
2 & 3
\end{vmatrix}
\end{aligned}$

Karena $\det(A)\neq0$, maka invers ada

# Langkah 2 : Matriks Kofaktor

$
C=
\begin{bmatrix}
1 & 2 & -2\\
-5 & 2 & 1\\
1 & -1 & 1
\end{bmatrix}
$

# Langkah 3 : Adjoin

$\begin{aligned}
\operatorname{adj}(A)
&= C^{T} \\[6pt]
&=
\begin{bmatrix}
1 & -5 & 1 \\
2 & 2 & -1 \\
-2 & 1 & 1
\end{bmatrix}
\end{aligned}$

# Langkah 4 : Invers Matrik

A^{-1}
=
$\frac{1}{3}
\begin{bmatrix}
1 & -5 & 1 \\
2 & 2 & -1 \\
-2 & 1 & 1
\end{bmatrix}$

A^{-1}
=
$\begin{bmatrix}
\frac{1}{3} & -\frac{5}{3} & \frac{1}{3} \\
\frac{2}{3} & \frac{2}{3} & -\frac{1}{3} \\
-\frac{2}{3} & \frac{1}{3} & \frac{1}{3}
\end{bmatrix}$

# 6. Matriks 4x4 (Invers)
Diberikan matriks

$
A=
\begin{bmatrix}
1 & 0 & 0 & 0\\
2 & 1 & 0 & 0\\
1 & 3 & 1 & 0\\
2 & 1 & 4 & 1
\end{bmatrix}
$

Bentuk matriks augmented:

$
\left[
\begin{array}{cccc|cccc}
1&0&0&0&1&0&0&0\\
2&1&0&0&0&1&0&0\\
1&3&1&0&0&0&1&0\\
2&1&4&1&0&0&0&1
\end{array}
\right]
$

Lakukan Operasi Baris Elementer:
# OBE 1

$
R_2 \leftarrow R_2-2R_1
$

$
R_3 \leftarrow R_3-R_1
$

$
R_4 \leftarrow R_4-2R_1
$

$
\left[
\begin{array}{cccc|cccc}
1&0&0&0&1&0&0&0\\
0&1&0&0&-2&1&0&0\\
0&3&1&0&-1&0&1&0\\
0&1&4&1&-2&0&0&1
\end{array}
\right]
$

# OBE 2
$
R_3 \leftarrow R_3-3R_2
$

$
R_4 \leftarrow R_4-R_2
$

$
\left[
\begin{array}{cccc|cccc}
1&0&0&0&1&0&0&0\\
0&1&0&0&-2&1&0&0\\
0&0&1&0&5&-3&1&0\\
0&0&4&1&0&-1&0&1
\end{array}
\right]
$

# OBE 3
$
R_4 \leftarrow R_4-4R_3
$

$
\left[
\begin{array}{cccc|cccc}
1&0&0&0&1&0&0&0\\
0&1&0&0&-2&1&0&0\\
0&0&1&0&5&-3&1&0\\
0&0&0&1&-20&11&-4&1
\end{array}
\right]
$

Maka diperoleh hasil inversnya

$\begin{aligned}
A^{-1}
&=
\begin{bmatrix}
1 & 0 & 0 & 0 \\
-2 & 1 & 0 & 0 \\
5 & -3 & 1 & 0 \\
-20 & 11 & -4 & 1
\end{bmatrix}
\end{aligned}$