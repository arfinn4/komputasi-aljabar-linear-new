# Tugas Eliminasi Gauss
# 1. sistem persamaan linear

$\begin{aligned}
x_1 + x_2 + x_3 + x_4 + x_5 &= 15 \\
2x_1 + x_2 + x_3 + x_4 + x_5 &= 16 \\
x_1 + 2x_2 + x_3 + x_4 + x_5 &= 17 \\
x_1 + x_2 + 2x_3 + x_4 + x_5 &= 18 \\
x_1 + x_2 + x_3 + 2x_4 + x_5 &= 19
\end{aligned}$

# 2.Matriks Augmented
$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
2&1&1&1&1&16\\
1&2&1&1&1&17\\
1&1&2&1&1&18\\
1&1&1&2&1&19
\end{array}
\right]$

# Eliminasi Gauss (OBE)
## Langkah pertama
$R_2 \rightarrow R_2 - 2R_1$ \\
$R_3 \rightarrow R_3 - R_1$ \\
$R_4 \rightarrow R_4 - R_1$ \\
$R_5 \rightarrow R_5 - R_1$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&-1&-1&-1&-1&-14\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah kedua

$R_2 \rightarrow -R_2$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah ketiga

$R_3 \rightarrow R_3 - R_2$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&-1&-1&-1&-12\\
0&0&1&0&0&3\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah keempat

$R_3 \rightarrow -R_3$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&1&1&1&12\\
0&0&1&0&0&3\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah kelima

$R_4 \rightarrow R_4 - R_3$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&1&1&1&12\\
0&0&0&-1&-1&-9\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah keenam

$R_4 \rightarrow -R_4$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&1&1&1&12\\
0&0&0&1&1&9\\
0&0&0&1&0&4
\end{array}
\right]$

## Langkah ketujuh

$R_5 \rightarrow R_5 - R_4$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&1&1&1&12\\
0&0&0&1&1&9\\
0&0&0&0&-1&-5
\end{array}
\right]$

## Langkah kedelapan

$R_5 \rightarrow -R_5$

$\left[
\begin{array}{ccccc|c}
1&1&1&1&1&15\\
0&1&1&1&1&14\\
0&0&1&1&1&12\\
0&0&0&1&1&9\\
0&0&0&0&1&5
\end{array}
\right]$

$(x_1,x_2,x_3,x_4,x_5) = (1,2,3,4,5)$

# Sagecell
![alt text](image.png)