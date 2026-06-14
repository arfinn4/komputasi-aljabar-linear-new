# Materi 2 : Persamaan linear

penyelesaian sistem dengan 5 persamaan dan 5 variabel menggunakan beberapa metode yang berbeda.
Contoh sistem persamaan linear 5×5:

$
\begin{cases}
x + y + z + w + v = 15 \\
2x - y + z + w - v = 8 \\
x + 2y - z + w + v = 12 \\
3x + y + z - w + v = 14 \\
x - y + 2z + w + 2v = 13
\end{cases}
$

# 1. Metode Eliminasi gauss

Langkah 1: Bentuk Matriks Augmented

$
\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
2&-1&1&1&-1&8\\
1&2&-1&1&1&12\\
3&1&1&-1&1&14\\
1&-1&2&1&2&13
\end{array}
\right]
$

Langkah 2: Hilangkan Elemen di Bawah Pivot Pertama
Operasi baris:

$
\begin{aligned}
R_2 &\leftarrow R_2 - 2R_1 \\
R_3 &\leftarrow R_3 - R_1 \\
R_4 &\leftarrow R_4 - 3R_1 \\
R_5 &\leftarrow R_5 - R_1
\end{aligned}
$

Hasil:
$
\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&-3&-1&-1&-3&-22\\
0&1&-2&0&0&-3\\
0&-2&-2&-4&-2&-31\\
0&-2&1&0&1&-2
\end{array}
\right]
$

Langkah 3: Tukar Baris Agar Pivot Kedua Bernilai 1

$R_2 \leftrightarrow R_3$

Hasil :

$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -2 & 0 & 0 & -3 \\
0 & -3 & -1 & -1 & -3 & -22 \\
0 & -2 & -2 & -4 & -2 & -31 \\
0 & -2 & 1 & 0 & 1 & -2
\end{array}
\right]
$

Langkah 4: Hilangkan Elemen di Bawah Pivot Kedua

$
\begin{aligned}
R_3 &\leftarrow R_3 + 3R_2 \\
R_4 &\leftarrow R_4 + 2R_2 \\
R_5 &\leftarrow R_5 + 2R_2
\end{aligned}
$

Hasil :

$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -2 & 0 & 0 & -3 \\
0 & 0 & -7 & -1 & -3 & -31 \\
0 & 0 & -6 & -4 & -2 & -37 \\
0 & 0 & -3 & 0 & 1 & -8
\end{array}
\right]
$

Langkah 5: Bentuk Pivot Ketiga

$
R_3 \leftarrow -\frac{1}{7}R_3
$

$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -2 & 0 & 0 & -3 \\
0 & 0 & 1 & \frac{1}{7} & \frac{3}{7} & \frac{31}{7} \\
0 & 0 & -6 & -4 & -2 & -37 \\
0 & 0 & -3 & 0 & 1 & -8
\end{array}
\right]
$

Langkah 6: Hilangkan Elemen di Bawah Pivot Ketiga

$
\begin{aligned}
R_4 &\leftarrow R_4 + 6R_3 \\
R_5 &\leftarrow R_5 + 3R_3
\end{aligned}
$

hasillnya :

$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -2 & 0 & 0 & -3 \\
0 & 0 & 1 & \frac{1}{7} & \frac{3}{7} & \frac{31}{7} \\
0 & 0 & 0 & -\frac{22}{7} & \frac{4}{7} & -\frac{73}{7} \\
0 & 0 & 0 & \frac{3}{7} & \frac{16}{7} & \frac{37}{7}
\end{array}
\right]
$

Langkah 7: Lanjutkan Hingga Bentuk Eselon
Setelah eliminasi selesai diperoleh:

$
\left[
\begin{array}{ccccc|c}
1 & 0 & 0 & 0 & 0 & 3 \\
0 & 1 & 0 & 0 & 0 & 4 \\
0 & 0 & 1 & 0 & 0 & 2 \\
0 & 0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 5
\end{array}
\right]
$

Solusi
$x=3, y=4, z=2, w=1, v=5$

# 2. Metode Gauss–Jordan
Dari bentuk eselon:

$
\left[
\begin{array}{ccccc|c}
1 & 0 & 0 & 0 & 0 & 3 \\
0 & 1 & 0 & 0 & 0 & 4 \\
0 & 0 & 1 & 0 & 0 & 2 \\
0 & 0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 5
\end{array}
\right]
$

Eliminasi elemen di atas pivot kelima:

$\[
\begin{aligned}
R_4 &\leftarrow R_4 + \frac{2}{11}R_5 \\
R_3 &\leftarrow R_3 - \frac{3}{7}R_5 \\
R_1 &\leftarrow R_1 - R_5
\end{aligned}
\]$

Lanjutkan hingga seluruh elemen di atas pivot menjadi nol.
Hasil akhirnya:

$
\left[
\begin{array}{ccccc|c}
1 & 0 & 0 & 0 & 0 & 3 \\
0 & 1 & 0 & 0 & 0 & 4 \\
0 & 0 & 1 & 0 & 0 & 2 \\
0 & 0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 5
\end{array}
\right]
$

maka :
$(x,y,z,w,v)=(3,4,2,1,5)$

# 3. Metode Matriks Invers
Tuliskan :

$\[
AX = B
\]$

dengan 

$
A=
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 \\
2 & -1 & 1 & 1 & -1 \\
1 & 2 & -1 & 1 & 1 \\
3 & 1 & 1 & -1 & 1 \\
1 & -1 & 2 & 1 & 2
\end{bmatrix}
$

$
X=
\begin{bmatrix}
x\\
y\\
z\\
w\\
v
\end{bmatrix}
$

$\[
B=
\begin{bmatrix}
15\\
8\\
12\\
14\\
13
\end{bmatrix}
\]$

Gunakan rumus :

$\[
X = A^{-1}B
\]$

Setelah invers matriks dihitung:

$\[
A^{-1}=
\left[
\cdots
\right]
\]$

(dapat dihitung menggunakan Gauss–Jordan).
Kemudian:

$\[
X = A^{-1}B =
\begin{bmatrix}
3\\
4\\
2\\
1\\
5
\end{bmatrix}
\]$

Sehingga :

$x=3,y=4,z=2,w=1,v=5$

# 4.Metode Cramer

Hitung determinan matriks koefisien:

$\[
D = \det(A)
\]$

Kemudian bentuk:

$\[
D_x,\; D_y,\; D_z,\; D_w,\; D_v
\]$

dengan mengganti kolom yang bersesuaian menggunakan vektor konstanta.

Rumus:
$\[
\begin{aligned}
x &= \frac{D_x}{D}, \\[6pt]
y &= \frac{D_y}{D}, \\[6pt]
z &= \frac{D_z}{D}, \\[6pt]
w &= \frac{D_w}{D}, \\[6pt]
v &= \frac{D_v}{D}.
\end{aligned}
\]$

Hasil perhitungan:

$\[
D = 44
\]$

$\[
D_x = 132,\quad
D_y = 176,\quad
D_z = 88,\quad
D_w = 44,\quad
D_v = 220
\]$

sehingga :

$\[
\begin{aligned}
x &= \frac{132}{44} = 3, \\[6pt]
y &= \frac{176}{44} = 4, \\[6pt]
z &= \frac{88}{44} = 2, \\[6pt]
w &= \frac{44}{44} = 1, \\[6pt]
v &= \frac{220}{44} = 5.
\end{aligned}
\]$


# Validasi Kode Program Menggunakan Python (NumPy)
Validasi ini bertujuan untuk memastikan bahwa solusi yang diperoleh secara manual sudah benar dan konsisten

```
import numpy as np

# Matriks koefisien
A = np.array([
    [1, 1, 1, 1, 1],
    [2, -1, 1, 1, -1],
    [1, 2, -1, 1, 1],
    [3, 1, 1, -1, 1],
    [1, -1, 2, 1, 2]
], dtype=float)

# Matriks konstanta
B = np.array([15, 8, 12, 14, 13], dtype=float)

# Menyelesaikan SPL
X = np.linalg.solve(A, B)

print("Solusi SPL:")
print("x =", X[0])
print("y =", X[1])
print("z =", X[2])
print("w =", X[3])
print("v =", X[4])
```

Link collab :
https://colab.research.google.com/drive/17TedJMeiGrQSLCl7ee1k3r1ZPX2Tk9YJ?usp=sharing
