# Tugas Ujian Tengah semester
# Matriks A (5×5)
A =
$\begin{bmatrix}
a & b & c & d & e \\
f & g & h & i & j \\
k & l & m & n & o \\
p & q & r & s & t \\
u & v & w & x & y
\end{bmatrix}$


# 2. Determinan Matriks 5×5
ekspansi baris pertama: $det(A) = aC_{11} - bC_{12} + cC_{13} - dC_{14} + eC_{15}$

$C_{ij} = (-1)^{i+j} M_{ij}$
$M_{ij} = \text{determinan matriks } 4 \times 4 \text{ hasil hapus baris } i \text{ kolom } j$

Contoh Kofaktor:
 
$C_{11} = (+1)$
$\begin{vmatrix}
g & h & i & j \\
l & m & n & o \\
q & r & s & t \\
v & w & x & y
\end{vmatrix}$

$C_{12} = (-1)$
$\begin{vmatrix}
f & h & i & j \\
k & m & n & o \\
p & r & s & t \\
u & w & x & y
\end{vmatrix}$

# 3. Bentuk matriks kofaktor:
${Cof}(A) =$
$\begin{bmatrix}
C_{11} & C_{12} & C_{13} & C_{14} & C_{15} \\
C_{21} & C_{22} & C_{23} & C_{24} & C_{25} \\
C_{31} & C_{32} & C_{33} & C_{34} & C_{35} \\
C_{41} & C_{42} & C_{43} & C_{44} & C_{45} \\
C_{51} & C_{52} & C_{53} & C_{54} & C_{55}
\end{bmatrix}$

setiap elemen : $C_{ij} = (-1)^{i+j} M_{ij}$

# 4. Adjoin Matriks (adj A)
Adjoin adalah transpose dari matriks kofaktor:
${adj}(A) =$
$\begin{bmatrix}
C_{11} & C_{21} & C_{31} & C_{41} & C_{51} \\
C_{12} & C_{22} & C_{32} & C_{42} & C_{52} \\
C_{13} & C_{23} & C_{33} & C_{43} & C_{53} \\
C_{14} & C_{24} & C_{34} & C_{44} & C_{54} \\
C_{15} & C_{25} & C_{35} & C_{45} & C_{55}
\end{bmatrix}$

# 5. Invers Matriks (A⁻¹)
Rumus utama: $A^{-1} = \frac{1}{\det(A)} \cdot \operatorname{adj}(A)$

# 6.Ringkasan Langkah

Urutan pengerjaan:
- Hitung semua minor 4×4

- Hitung semua kofaktor

- Bentuk matriks kofaktor

- Transpose → jadi adj(A)

- Hitung determinan
Gunakan: $A^{-1} = \frac{1}{\det(A)} \cdot \operatorname{adj}(A)$

# 7. Contoh Sederhana
$A = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}$

$det(A) = (1)(4) - (2)(3) = -2$

${adj}(A) = \begin{bmatrix}
4 & -2 \\
-3 & 1
\end{bmatrix}$

$A^{-1} = \frac{1}{-2}$
$\begin{bmatrix}
4 & -2 \\
-3 & 1
\end{bmatrix}$