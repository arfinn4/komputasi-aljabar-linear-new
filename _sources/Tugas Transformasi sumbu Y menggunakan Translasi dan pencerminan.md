# Tugas Transformasi sumbu Y menggunakan Translasi dan pencerminan 
# representase data
Titik objek disimpan dalam bentuk koordinat:

$
(x, y)
$

Contoh:

$
A(1,1),\; B(3,1),\; C(3,3),\; D(1,3)
$

Keempat titik tersebut membentuk sebuah persegi.

# Translasi (Pergeseran)
Rumus translasi yang digunakan adalah:

$
(x, y) \rightarrow (x + dx,\; y)
$

Pada program digunakan:

```
dx = 1
```

Artinya, pada setiap langkah objek bergeser 1 satuan ke kanan.

Keterangan:
 Nilai x berubah \rightarrow objek bergerak secara horizontal.
 Nilai y tetap \rightarrow tidak ada perubahan vertikal.


# Translasi dalam Bentuk Matriks
Dalam koordinat homogen, translasi dapat dituliskan sebagai:

$
T=
\begin{bmatrix}
1 & 0 & 1\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
$

Dengan titik:

$
P=
\begin{bmatrix}
x\\
y\\
1
\end{bmatrix}
$

Maka hasil transformasinya adalah:

$
P' = T \cdot P
$

Sehingga diperoleh:

$
(x,y)\rightarrow(x+1,y)
$

Rumus yang digunakan pada program berasal dari bentuk matriks tersebut.

# Refleksi terhadap Sumbu Y
Rumus refleksi terhadap sumbu $Y$ adalah:

$
(x,y)\rightarrow(-x,y)
$

Artinya:
Koordinat x dibalik $(kanan \leftrightarrow kiri).$
Koordinat y tetap.

Contoh:

$
(4,2)\rightarrow(-4,2)
$

# Refleksi dalam Bentuk Matriks
Matriks refleksi terhadap sumbu $Y$:

$
R=
\begin{bmatrix}
-1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
$

Transformasinya:

$
P' = R \cdot P
$

Hasilnya:

$
(x,y)\rightarrow(-x,y)
$

# Transformasi Gabungan
Urutan transformasi yang digunakan pada program adalah:
- Translasi
- Refleksi

Sehingga:

$
P' = R \cdot T \cdot P
$

Artinya:
- Titik digeser terlebih dahulu.
- Setelah itu hasilnya dicerminkan terhadap sumbu Y

# Proses Animasi (Loop)
Pada setiap langkah animasi:

- Objek ditranslasi (bergeser ke kanan).
- Hasil translasi direfleksikan terhadap sumbu Y
- Objek dan bayangannya ditampilkan.
- Proses diulang untuk frame berikutnya.

Dengan pengulangan ini terbentuk animasi pergerakan objek.

# Mengapa Objek dan Bayangan Selalu Sejajar?
Hubungan antara titik objek dan bayangannya adalah:

$
x_{\text{bayangan}} = -x_{\text{objek}}
$

$
y_{\text{bayangan}} = y_{\text{objek}}
$

Akibatnya:

- Jarak objek dan bayangan terhadap sumbu y selalu sama.
- Posisinya berada pada sisi yang berlawanan.
- Objek dan bayangan tampak sejajar.

# Sistem Animasi
Program menggunakan:

```
matplotlib.animation.FuncAnimation
```

Fungsi ini digunakan untuk:

- Menjalankan frame secara berulang.
- Memperbarui tampilan pada setiap langkah animasi.
- Menampilkan pergerakan objek secara dinamis.

# Visualisasi
Pada setiap frame ditampilkan:

- Objek (warna biru).
- Bayangan hasil refleksi (warna merah).
- Grid koordinat.
- Sumbu x dan y
- Label titik-titik objek.

# Alur Program

$\begin{center}
\begin{tabular}{c}
Objek Awal \\
\downarrow \\
Translasi \\
\downarrow \\
Refleksi \\
\downarrow \\
Tampilkan \\
\downarrow \\
Ulangi
\end{tabular}
\end{center}
$

# Kesimpulan
Program ini menggunakan dua jenis transformasi geometri, yaitu translasi dan refleksi terhadap sumbu $Y$. Kedua transformasi dapat dinyatakan dalam bentuk matriks homogen maupun menggunakan rumus langsung pada kode program. Hasil animasi memperlihatkan hubungan yang jelas antara objek dan bayangannya setelah mengalami translasi dan pencerminan.

# Ilustrasi Sederhana
Bayangkan seseorang berdiri di depan cermin:

$\begin{itemize}
    \item Orang tersebut bergerak ke kanan.
    \item Bayangannya tampak bergerak ke kiri.
    \item Keduanya tetap sejajar terhadap cermin.
\end{itemize}$

Konsep inilah yang ditunjukkan oleh animasi transformasi translasi dan refleksi pada program.

# Verifikasi Menggunakan Script Python (NumPy)

```
import matplotlib.pyplot as plt
import matplotlib.animation as animation
from IPython.display import HTML
import numpy as np

# ======================
# 1. TITIK AWAL
# ======================
points = [(1,1), (3,1), (3,3), (1,3)]
labels = ['A','B','C','D']

# ======================
# 2. FUNGSI TRANSFORMASI
# ======================

# Translasi: geser ke kanan
def translasi(p, dx):
    return [(x + dx, y) for x, y in p]

# Refleksi terhadap sumbu Y
def refleksi_y(p):
    return [(-x, y) for x, y in p]

# ======================
# 3. MENYIMPAN STEP ANIMASI
# ======================
steps_obj = []
steps_cermin = []

current = points.copy()

for i in range(6):
    # geser objek
    current = translasi(current, 1)

    # simpan objek
    steps_obj.append(current.copy())

    # buat bayangan dari posisi terbaru
    steps_cermin.append(refleksi_y(current))

# ======================
# 4. SETUP PLOT
# ======================
fig, ax = plt.subplots()

def update(frame):
    ax.clear()

    # batas tampilan
    ax.set_xlim(-10, 10)
    ax.set_ylim(-2, 10)

    # grid
    ax.set_xticks(np.arange(-10, 11, 1))
    ax.set_yticks(np.arange(-2, 11, 1))
    ax.set_aspect('equal')
    ax.grid(True)

    # sumbu
    ax.axhline(0)
    ax.axvline(0)

    # ambil data
    obj = steps_obj[frame]
    cermin = steps_cermin[frame]

    # tutup bentuk
    obj_closed = obj + [obj[0]]
    cermin_closed = cermin + [cermin[0]]

    # plot objek (biru)
    x1 = [p[0] for p in obj_closed]
    y1 = [p[1] for p in obj_closed]
    ax.plot(x1, y1, 'bo-', label='Objek')

    # plot bayangan (merah)
    x2 = [p[0] for p in cermin_closed]
    y2 = [p[1] for p in cermin_closed]
    ax.plot(x2, y2, 'ro--', label='Cermin')

    # label objek
    for i, (x, y) in enumerate(obj):
        ax.text(x, y, f"{labels[i]}({x},{y})", color='blue')

    # label bayangan
    for i, (x, y) in enumerate(cermin):
        ax.text(x, y, f"{labels[i]}'({x},{y})", color='red')

    ax.set_title(f"Step {frame+1}: Translasi & Refleksi")
    ax.legend()

# ======================
# 5. ANIMASI
# ======================
ani = animation.FuncAnimation(
    fig,
    update,
    frames=len(steps_obj),
    interval=1000,
    repeat=False
)

# ======================
# 6. TAMPILKAN
# ======================
plt.close()
HTML(ani.to_jshtml())
```

# Link Google Colab
https://colab.research.google.com/drive/1dRwF6nSH7jDuIoh8o0kYZhc1WGK162Dy?usp=sharing
