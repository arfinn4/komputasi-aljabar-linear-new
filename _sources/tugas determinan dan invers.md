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
\det(A)
=
3(4)-2(1)
=
12-2
=
10
$

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

$
\det(A)
=
1\begin{vmatrix}
4 & 5\\
0 & 6
\end{vmatrix}
-
2\begin{vmatrix}
0 & 5\\
1 & 6
\end{vmatrix}
+
3\begin{vmatrix}
0 & 4\\
1 & 0
\end{vmatrix}
$

Hitung masing-masing minor ;

$
\begin{aligned}
\begin{vmatrix}
4 & 5 \\
0 & 6
\end{vmatrix}
&= 24 \\[6pt]
\begin{vmatrix}
0 & 5 \\
1 & 6
\end{vmatrix}
&= -5 \\[6pt]
\begin{vmatrix}
0 & 4 \\
1 & 0
\end{vmatrix}
&= -4
\end{aligned}
$

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

$
\det(A)
=
1M_{11}
-2M_{12}
+0M_{13}
-1M_{14}
$

minor pertama :

$
M_{11}
=
\begin{vmatrix}
1 & 2 & 0 \\
4 & 1 & 2 \\
0 & 3 & 1
\end{vmatrix}
=
-13
$

minor kedua :

$
M_{12}
=
\begin{vmatrix}
3&2&0\\
0&1&2\\
1&3&1
\end{vmatrix}
=-11
$

minor keempat :

$
M_{14}
=
\begin{vmatrix}
3&1&2\\
0&4&1\\
1&0&3
\end{vmatrix}
=29
$

Sehingga

$
\det(A)
=
1(-13)-2(-11)-29
$

$
=
-13+22-29
$

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

$
\det(A)
=
(2)(4)-(1)(3)
=
5
$

Rumus invers matriks 2x2:

$
A^{-1}
=
\frac{1}{ad-bc}
\begin{bmatrix}
d & -b\\
-c & a
\end{bmatrix}
$

Substitusi nilai:

$
A^{-1}
=
\frac{1}{5}
\begin{bmatrix}
4 & -1\\
-3 & 2
\end{bmatrix}
$

$
\boxed{
A^{-1}
=
\begin{bmatrix}
\frac45 & -\frac15\\
-\frac35 & \frac25
\end{bmatrix}
}
$

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

$
\det(A)
=
1
\begin{vmatrix}
1 & 1\\
3 & 4
\end{vmatrix}
-
2
\begin{vmatrix}
0 & 1\\
2 & 4
\end{vmatrix}
+
1
\begin{vmatrix}
0 & 1\\
2 & 3
\end{vmatrix}
$

$
=
1(4-3)-2(0-2)+(0-2)
$

$
=
3
$

Karena $\det(A)\neq0$, maka invers ada.

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

$
\operatorname{adj}(A)
=
C^T
=
\begin{bmatrix}
1 & -5 & 1\\
2 & 2 & -1\\
-2 & 1 & 1
\end{bmatrix}
$

# Langkah 4 : Invers Matrik

$
A^{-1}
=
\frac{1}{3}
\begin{bmatrix}
1 & -5 & 1\\
2 & 2 & -1\\
-2 & 1 & 1
\end{bmatrix}
$

$
\boxed{
A^{-1}
=
\begin{bmatrix}
\frac13 & -\frac53 & \frac13\\
\frac23 & \frac23 & -\frac13\\
-\frac23 & \frac13 & \frac13
\end{bmatrix}
}
$

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

$
\boxed{
A^{-1}
=
\begin{bmatrix}
1 & 0 & 0 & 0\\
-2 & 1 & 0 & 0\\
5 & -3 & 1 & 0\\
-20 & 11 & -4 & 1
\end{bmatrix}
}
$