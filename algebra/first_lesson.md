---
title: 01. Введение в алгебру
description: 
published: 1
date: 2020-11-17T22:31:43.668Z
tags: 
editor: undefined
dateCreated: 2020-09-09T20:10:29.435Z
---

# Введение в Алгебру
> Чернышев Всеволод Леонидович
>
> 9 сентября 2020 

## Матрицы и системы линейных алгебраических уравнений (СЛАУ)
> Учебник (необязатльеный): Кострикин - Введение в алгебру

Опр. Матрицей размера $(m\cdot n)$ называется упорядоченная прямоугольная таблица, содержащая $m$ строк и $n$ столбцов.
$$
A=\begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots  \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{pmatrix}
$$

$a_{ij}$ - элемент матрицы , стоящий в i-ой строке и j-м столбце
$$
[A]_{ij} = a_{ij}
$$
m и n - размеры матрицы

Частные случаи:
1. $m = n$ - квадратная матрица
2. $n = 1$ - m-мерный (вектор) столбец
3. $m = 1$ - n-мерная строка
4. Все $A_{ij} = 0$ - нулевая матрица
5. Единичная матрица
$$
E_n = \begin{pmatrix}
1 & \dots & \dots &\dots & 0 \\
\vdots & \ddots & & & \vdots \\
\vdots & & 1 & & \vdots \\
\vdots & & & \ddots & \vdots \\
0 & \dots & \dots &\dots & 1 \\
\end{pmatrix}
$$
$$
a_{ij} = \begin{cases}
1, &i=j \\
0, &i\not=j
\end{cases}
 = \delta_j^i - \text{символ Кронекера}
$$

**Опр.** Матрицы называют равными, если они одного размера (порядка) и равны их элементы,
стоящие на одинаковый местах

## Операции с матрицами
**Опр.** Суммой матриц А и B типа m*n называют матрицу С того же типа с элементами
$$
[C]_{ij} = [A]_{ij} + [B]_{ij}
$$

Опр. Матрица С называется произведением числа $\alpha$ на матрицу A, если матрицы A и C одинакового размера и $C_{ij} = \alpha \cdot a_{ij}$

**Опр.** Транспонированием матрицы  называется операция, переводящая строки в столбцы (с сохранением порядка следования)
$$
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}^T =
\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}
[A]_{ij} = [A^T]_{ji}
$$


**Определения**

$A^T= A$ - Симметричная
$$
\begin{pmatrix}
0 & 5 & 4 \\
5 & 0 & 3 \\
4 & 3 & 0
\end{pmatrix}
$$

$A^T = -A$ - Кососиметричная
$$
\begin{pmatrix}
0 & 5 & -4 \\
-5 & 0 & 3 \\
4 & 3 & 0
\end{pmatrix}
$$

## Произведения матриц
Произведение матриц $A_{n\cdot p}$ и $B_{p\cdot k}$

$$
c_{ij} = \sum_{l=1}^p a_{il}b_{lj} =\\
= a_{i1}b_{1j} + a_{i2}b_{2j} + \dots + a_{ip}b_{pj}\\
\forall i = 1\dots n, \forall j=1\dots k
$$

Пример
$$
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix} \cdot
\begin{pmatrix}
1 \\
-2
\end{pmatrix} =
\begin{pmatrix}
1 \cdot 1 + 2 \cdot (-2) \\
3\cdot 1 + 4 \cdot (-2)
\end{pmatrix} =
\begin{pmatrix}
-3 \\
-5
\end{pmatrix}
$$

## Теорема (Св-ва транспонирования)
1. $(A^T)^T=A$
2. $(A+B)^T = A^T \cdot B^T$
3. $(\alpha A)^T = \alpha A^T; \alpha \isin R$
4. $(A \cdot B)^T = B^T \cdot A^T$
5. Умножение матриц ассоциативно
$$
\forall A,B,C \text{ - матрицы соответсвующих типов} \\
A \cdot(B \cdot C) = (A \cdot B) \cdot C
$$
6. $\exist$ нейтральный элемент по умножению  матриц. Это квадратная единичная матрица
$$
A\cdot E_n = E_n \cdot A = A
$$
7. Дистрибутивность:
$$
A\cdot(B + C) = A \cdot B + A \cdot C \\
(A + B) \cdot C = A \cdot C + B \cdot C
$$
8. Умножение матриц не является коммутативной операцией, т.е. не зависит от порядка множителей

Пример
$$
A = \begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix},
B = \begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix} \\
A \cdot B = \begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix} = A\\
B \cdot A = \begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix} = B \\
A\cdot B \not= B\cdot A
$$


