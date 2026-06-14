# Materi 3 : eliminasi gaussion

C. Analisis Kasus Eliminasi Gaussian pada SPL Berordo 5×5
Pada bagian ini akan dibahas proses penyelesaian Sistem Persamaan Linear (SPL) berordo 5×5 menggunakan metode Eliminasi Gaussian. Metode ini merupakan salah satu teknik yang paling umum digunakan dalam aljabar linear untuk menentukan nilai variabel yang memenuhi seluruh persamaan dalam suatu sistem.

Representasi Sistem Persamaan Linear ke dalam Bentuk Matriks

Sebelum melakukan proses eliminasi, sistem persamaan terlebih dahulu dinyatakan dalam bentuk matematis sebagai berikut:

$\begin{align}
x_1 + x_2 + x_3 + x_4 + x_5 &= 1 \\
x_2 + x_3 + x_4 + x_5 &= 2 \\
x_3 + x_4 + x_5 &= 3 \\
x_4 + x_5 &= 4 \\
x_5 &= 5
\end{align}$

Untuk mempermudah proses perhitungan, koefisien setiap variabel dan konstanta pada ruas kanan dituliskan ke dalam bentuk matriks augmented sebagai berikut:

$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 1 \\
0 & 1 & 1 & 1 & 1 & 2 \\
0 & 0 & 1 & 1 & 1 & 3 \\
0 & 0 & 0 & 1 & 1 & 4 \\
0 & 0 & 0 & 0 & 1 & 5
\end{array}
\right]
$

Matriks augmented tersebut akan menjadi dasar dalam penerapan metode Eliminasi Gaussian. Dengan melakukan serangkaian Operasi Baris Elementer, bentuk matriks dapat disederhanakan hingga solusi untuk setiap variabel diperoleh secara sistematis dan efisien.

# Proses Transformasi Matriks dengan Operasi Baris Elementer (OBE)
Tujuan dari proses ini adalah mengubah matriks augmented menjadi bentuk yang lebih sederhana sehingga nilai setiap variabel dapat ditentukan dengan mudah. Metode yang digunakan adalah Operasi Baris Elementer (OBE) secara bertahap hingga diperoleh matriks identitas pada bagian kiri.

# Tahap 1: Menentukan Pivot pada Kolom Pertama
Langkah pertama adalah memastikan bahwa elemen pertama pada baris pertama dapat digunakan sebagai pivot utama. Pivot ini akan menjadi acuan untuk menghilangkan elemen-elemen lain yang berada di bawahnya pada kolom yang sama.

Pada tahap ini, kondisi matriks sudah memungkinkan proses dilanjutkan tanpa perlu pertukaran baris.

# Tahap 2: Menghilangkan Elemen pada Kolom Kelima
Setelah kolom pertama hingga keempat berada pada posisi yang sesuai, langkah berikutnya adalah menghilangkan nilai yang berada di atas elemen pivot pada kolom kelima.

Operasi yang digunakan:

$
B_4 \leftarrow B_4 - 4B_5
$

Melalui operasi ini, elemen pada kolom kelima selain pivot akan berubah menjadi nol sehingga bentuk matriks semakin mendekati matriks identitas.

# Tahap 3: Menghilangkan Elemen pada Kolom Keempat
Berikutnya dilakukan eliminasi pada kolom keempat. Tujuannya adalah menjadikan seluruh elemen selain pivot pada kolom tersebut bernilai nol.

Operasi yang dilakukan:

$B_3 \leftarrow B_3 - B_4$

Dengan langkah ini, bagian kiri matriks berubah menjadi matriks identitas, yang menandakan bahwa proses eliminasi telah selesai.
Menentukan Himpunan Penyelesaian

Hasilnya, kolom keempat hanya memiliki satu elemen bernilai satu sebagai pivot, sedangkan elemen lainnya menjadi nol.

# Tahap 4: Menghilangkan Elemen pada Kolom Ketiga

Proses yang sama diterapkan pada kolom ketiga agar hanya tersisa satu pivot.
Operasi yang digunakan:

$
B_2 \leftarrow B_2 - 4B_3
$

Setelah operasi ini, kolom ketiga telah memenuhi syarat matriks identitas.

# Tahap 5: Menyelesaikan Kolom Kedua
Tahap terakhir adalah membersihkan kolom kedua sehingga seluruh elemen di atas dan di bawah pivot menjadi nol.
Operasi yang dilakukan:

$
B_1 \leftarrow B_1 - 4B_2
$

Dengan langkah ini, bagian kiri matriks berubah menjadi matriks identitas, yang menandakan bahwa proses eliminasi telah selesai.

# Menentukan Himpunan Penyelesaian
Karena matriks telah berhasil diubah menjadi matriks identitas, nilai setiap variabel dapat langsung dibaca dari kolom terakhir matriks.
Diperoleh:

$
x_1 = -1
$

$
x_2 = 1



x_3 = -1



x_4 = -1



x_5 = 3
$

Sehingga himpunan penyelesaiannya adalah

$
(x_1,x_2,x_3,x_4,x_5)=(-1,\,1,\,-1,\,-1,\,3)
$

# Validasi Logika Menggunakan Kode Python (NumPy)

```
import numpy as np

# Matriks koefisien
A = np.array([
    [1, 4, 0, 0, 0],
    [0, 1, 4, 0, 0],
    [0, 0, 1, 1, 0],
    [0, 0, 0, 1, 4],
    [0, 0, 0, 0, 1]
], dtype=float)

# Vektor konstanta
B = np.array([
    3,
    -3,
    -2,
    11,
    3
], dtype=float)

# Menyelesaikan SPL
X = np.linalg.solve(A, B)

print("Solusi SPL:")
print(f"x1 = {X[0]}")
print(f"x2 = {X[1]}")
print(f"x3 = {X[2]}")
print(f"x4 = {X[3]}")
print(f"x5 = {X[4]}")
```

# Link collabnya :
https://colab.research.google.com/drive/1aPa7p_DU1dP17n4NIulXhvZOGAD20dKm?usp=sharing

