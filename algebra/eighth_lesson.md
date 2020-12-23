---
title: 08. Структуры общего решения СЛАУ
description: 
published: 1
date: 2020-12-23T16:43:45.921Z
tags: 
editor: markdown
dateCreated: 2020-11-11T11:21:40.140Z
---

# Структура общего решения СЛАУ

## Теорема (о структуре общего решения однородной СЛАУ)
Пусть $\Phi_1, \dots, \Phi_k$ - ФСР однородной СЛАУ $Ax=0$. Тогда любое решение этой СЛАУ можно представить в виде:

$x = c_1 \Phi_1 + \dots + c_k \Phi_k$, где $c_1, \dots, c_k$ - некоторые постоянные

Пусть 
$$
x^0 = \begin{pmatrix}
    x_1^0 \\
    \dots \\
    x_n^0
\end{pmatrix}
$$
произвольное решение однородной СЛАУ. Предположим

$$
\begin{cases}
    a_{11}x_1 + \dots a_{1r}x_r = -a_{1r+1}x_{r+1} - \dots - a_{1n}x_n \\
    \dots \\
    a_{r1}x_1 + \dots a_{rr}x_r = -a_{rr+1}x_{r+1} - \dots - a_{rn}x_n \\
\end{cases} (1)
$$

Решим эту СЛАУ относительно неизвестных $x_1, \dots, x_r$ (например по формулам Крамера)

$$
\begin{cases}
    x_1 = \alpha_{1r+1} x_{r+1} + \dots + \alpha_{1n} x_n \\
    \dots \\
    x_r = \alpha_{rr+1} x_{r+1} + \dots + \alpha_{rn} x_n \\
\end{cases} (2)
$$

Составим новую матрицу $D$:

$$
D = \begin{pmatrix}
    x_{1}^0 & \varphi_{11} & \dots & \varphi_{k1} \\
    \dots & \dots & & \dots \\
    x_r^0 & \varphi_{1r} & \dots & \varphi_{kr} \\
    x_{r+1}^0 & \varphi_{1r+1} & \dots & \varphi_{kr+1} \\
    \dots & \dots & & \dots \\
    x_n^0 & \varphi_{1n} & \dots & \varphi{kn}
\end{pmatrix}
$$

$\varphi_{ij}$ - координаты столбцов, образующих ФСР

1. $Rg D \ge k$, т. к. $\Phi_1, \dots, \Phi_k$ - л.н.з. (по определению ФСР), а по теореме о ранге матрицы $Rg D =$ максимальному числу л.н.з. столбцов
2. Покажем, что $Rg D \le k$. Столбцы $x^0, \Phi_1, \dots, \Phi_k$ - решения СЛАУ $Ax = 0 \implies$ из (2) получим, что:

$$
\begin{array}{l}
x_1^0 = \alpha_{1r+1}x_{r+1}^{0} + \dots + \alpha_{1n}x_n^0 \\
\varphi_{11}^0 = \alpha_{1r+1}\phi_{1r+1} + \dots + \alpha_{1n}\varphi_{1n} \\
\dots \\
\varphi_k1^0 = \alpha_{1r+1}\phi_{kr+1} + \dots + \alpha_{1n}\varphi_{kn} \\
\end{array}
$$

т. е. линейная строка $d_1$ матрицы является линейной комбинацией строк 

$$
d_{r+1}, \dots, d_n: \\
d_1 = \alpha_{1r+1}d_{r+1} + \dots + \alpha_{1n}d_n
$$

Аналогично с отстальными строками вплоть до $r$-ой:

$$
\dots d_r = \alpha_{rr+1}d_{r+1} + \dots + \alpha_{rn}d_n
$$

Сделаем элементарные преобразования:
$$
d_1 - \alpha_{1r+1}d_{r+1} - \dots - \alpha_{1n}d_n \to d_1 \\
\dots \\
d_r - \alpha_{rr+1}d_{r+1} - \dots - \alpha_{rn}d_n \to d_r
$$

Получаем матрицу $D_1$, у которой первые $r$ строк нулевые:
$$
D \sim D_1 = \begin{pmatrix}
0 & \dots & \dots & 0 \\
\dots \\
0 & \dots & \dots & 0 \\
x_{r+1}^0 & \varphi_{1r+1} & \dots & \varphi_{kr+1} \\
\dots \\
x_n^0 & \varphi_{1n} & \dots & \varphi_{kn}
\end{pmatrix}
$$

$Rg D_1 \le n - r = k$ При элементарных преобразованиях ранг не меняется $\implies RgD \le k$. Таким образом $RgD = k$. Заметим, что столбцы $\Phi_1, \dots, \Phi_k$ являются базисными (они л. н. з. и их $k = RgD$) $\implies$ по теормеме о базисном миноре столбец $x^0$ - их линейная комбинаций. Т. е. $\exists$ числа $c_1, \dots, c_k$:

$$
x^0 = c_1 \Phi_1 + \dots + c_k \Phi_k
$$

## Неоднородные СЛАУ
Рассмотрим СЛАУ $Ax = b$ (СЛАУ $Ax = 0$ называют однородный, соответствующей $Ax = b$)

### Теорема (о структуре общего решения неоднородной СЛАУ)
Пусть известно частное решение этой слау $\tilde{x}$ СЛАУ (неоднород). Тогда любое решение этой СЛАУ может быть представлено в виде:

$$
x = \tilde{x} + c_1 \Phi_1 + \dots + c_k \Phi_k
$$

где $c_1, \dots, c_k$ - некоторые постоянные, а $\Phi_1, \dots, \Phi_k$ - ФСР соответствующей однородной системы $Ax=0$

**Замечание** $X_{\text{общее неоднородной}} = X_{\text{частное неоднородной}} + X_{\text{общее однородной}}$

$\square$ Пусть $x^0$ - произвольное решение СЛАУ $Ax = b \implies$ по свойствам решений $x^0 - \tilde{x}$ - решение СЛАУ $Ax = 0$. К $x^0 - \tilde{x}$ применим теормему о структуре общего решения однородной СЛАУ:

$$
x^0 - \tilde{x} = c_1 \Phi_1 + \dots + c_k \Phi_k \implies \\
x^0 = \tilde{x} + c_1 \Phi_1 + \dots + c_k \Phi_k
$$

**Пример**
$$
\begin{cases}
x_1 + 2x_2 + 3x_3 - x_4 & = & -1 \\
-x_1 - 3x_2 + 5x+4 & = & 8 \\
2x_1 + 3x_2 + 9x_3 + 2x_4 & = & 5
\end{cases} \\
(A|b) = \left(\begin{array}{c c c c|c}
    1 & 2 & 3 & -1 & -1 \\
    -1 & -3 & 0 & 5 & 8 \\
    2 & 3 & 9 & 2 & 5
\end{array}\right) \sim
\left(
    \begin{array}{c c c c|c}
        1 & 2 & 3 & -1 & -1 \\
        0 & -1 & 3 & 4 & 7 \\
        0 & 0 & 0 & 0 & 0
    \end{array}
\right) \sim
\left(
    \begin{array}{c c c c|c}
        1 & 0 & 9 & 7 & 13 \\
        0 & 1 & -3 & -4 & -7
    \end{array}
\right)
$$

$x_1, x_2$ - базисные (главные)\
$x_3, x_4$ - свободные

$$
\begin{cases}
x_1 & = & -9x_3 - 7x_4 + 13 \\
x_2 & = & 3x_3 + 4x_4 - 7
\end{cases} \\
X = \begin{pmatrix}
    x_1 \\ x_2 \\ x_3 \\ x_4
\end{pmatrix} = \begin{pmatrix}
    -9x_3 - 7x_4 + 13 \\
    3x_3 + 4x_4 - 7 \\
    x_3 \\
    x_4
\end{pmatrix} = \underbrace{x_3 \begin{pmatrix}
    -9 \\ 3 \\ 1 \\ 0
\end{pmatrix} + x_4 \begin{pmatrix}
    -7 \\ 4 \\ 0 \\ 1
\end{pmatrix}}_{\text{общее решение однородной}} + \underbrace{\begin{pmatrix}
    13 \\ -7 \\ 0 \\ 0
\end{pmatrix}}_{\tilde{x}\text{ часть}}
$$

ФСР однородной:
$$
\Phi_1 = \begin{pmatrix}
    -9 \\ 3 \\ 1 \\ 0
\end{pmatrix}, \Phi_2 = \begin{pmatrix}
    -7 \\ 4 \\ 0 \\ 1
\end{pmatrix}
$$
