# Materi 4: Konsep Dasar Teori Sistem Persamaan Linear
# D. Landasan Teoretis Sistem Persamaan Linear
Sebelum melakukan penyelesaian terhadap Sistem Persamaan Linear (SPL), penting untuk memahami konsep-konsep dasar yang menjadi fondasi dari metode penyelesaiannya. Pemahaman teori ini membantu dalam menganalisis struktur sistem, menentukan solusi, serta memilih metode yang paling sesuai untuk digunakan.

# Konsep Dasar Sistem Persamaan Linear
Sistem Persamaan Linear merupakan sekumpulan persamaan aljabar yang melibatkan beberapa variabel dengan pangkat tertinggi satu. Tujuan utama dari SPL adalah menemukan nilai variabel yang dapat memenuhi seluruh persamaan secara bersamaan.

Secara umum, bentuk persamaan linear dapat dituliskan sebagai:

$a_1x_1 + a_2x_2 + \cdots + a_nx_n = b$

adalah koefisien yang menyatakan pengali masing-masing variabel.

$x1,x2,…,xn$	​

merupakan variabel yang nilainya akan dicari.
b adalah konstanta atau nilai tetap pada ruas kanan persamaan.

# Pengelompokan Sistem Persamaan Linear
Berdasarkan jumlah variabel dan bentuk persamaannya, SPL dapat diklasifikasikan menjadi beberapa jenis, yaitu:

## 1. Sistem Homogen
Sistem disebut homogen apabila seluruh konstanta pada ruas kanan bernilai nol (b=0).

## 2. Sistem Non-Homogen
Sistem non-homogen adalah sistem yang memiliki setidaknya satu konstanta pada ruas kanan yang tidak sama dengan nol (b
=0).

## 3. Persamaan Linear dan Nonlinear
Suatu sistem dikatakan linear apabila setiap variabel berpangkat satu dan tidak terdapat perkalian antarvariabel. Sebaliknya, jika terdapat variabel berpangkat lebih dari satu atau hasil kali antarvariabel, maka sistem tersebut termasuk sistem non-linear.

# Karakteristik dan Jenis Solusi SPL
Sebuah Sistem Persamaan Linear dapat menghasilkan beberapa kemungkinan solusi, tergantung pada hubungan antar persamaannya.

## 1. Solusi Tunggal
Terjadi ketika sistem memiliki tepat satu himpunan nilai variabel yang memenuhi seluruh persamaan.

## 2. Solusi Tak Hingga
Muncul apabila terdapat lebih dari satu kombinasi nilai variabel yang memenuhi semua persamaan. Kondisi ini biasanya terjadi karena adanya ketergantungan antar persamaan.

## 3. Tidak Memiliki Solusi
Sistem tidak mempunyai solusi jika terdapat pertentangan antar persamaan sehingga tidak ada nilai variabel yang dapat memenuhi semuanya sekaligus.

# Representasi SPL dalam Bentuk Matriks
Untuk mempermudah proses perhitungan, Sistem Persamaan Linear sering dituliskan dalam bentuk matriks.

# Matriks Koefisien (A)
Matriks yang berisi seluruh koefisien variabel dari sistem persamaan.

# Vektor Variabel (X)
Vektor yang memuat variabel-variabel yang akan dicari nilainya.

# Vektor Konstanta (B)
Vektor yang berisi nilai konstanta pada ruas kanan setiap persamaan.

Dengan demikian, SPL dapat dinyatakan dalam bentuk:

AX=B

Selain itu, untuk keperluan eliminasi dan operasi baris, sering digunakan matriks augmented, yaitu penggabungan antara matriks koefisien dan vektor konstanta:

$[A∣B]$

Bentuk ini sangat membantu dalam penerapan metode Eliminasi Gauss maupun Eliminasi Gauss-Jordan.

# Penyelesaian Komputasi Menggunakan SageMath
Selain dapat diselesaikan secara manual, Sistem Persamaan Linear juga dapat dianalisis menggunakan perangkat lunak matematika seperti SageMath. Dengan bantuan SageMath, proses perhitungan menjadi lebih cepat, akurat, dan efisien, terutama untuk sistem berukuran besar.

Melalui SageMath, pengguna dapat:

Membentuk matriks dan vektor secara otomatis.
Melakukan operasi baris elementer.
Menghitung determinan matriks.
Menentukan invers matriks.
Menyelesaikan SPL menggunakan berbagai metode numerik maupun aljabar.

# SageMath Cell Interaktif
SageMath menyediakan fasilitas SageMath Cell, yaitu lingkungan komputasi daring yang memungkinkan pengguna menjalankan kode matematika tanpa perlu menginstal perangkat lunak tambahan. Fasilitas ini sangat bermanfaat untuk memverifikasi hasil perhitungan manual dan mendukung proses pembelajaran matematika komputasional.

<div id="mycell">
<script type="text/x-sage">
A = matrix(QQ, 4, 4, [1, 2, 3, 4,
                      5, 6, 7, 8,
                      9, 10, 11, 12,
                      13, 14, 15, 16])

A.rref()
</script>
</div>

<script>
sagecell.makeSagecell({
    inputLocation: '#mycell',
    autoeval: false
});
</script>