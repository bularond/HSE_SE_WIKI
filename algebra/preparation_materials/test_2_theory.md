---
title: 2. ФСР, ангем, теория групп
description: 
published: 1
date: 2020-12-24T17:07:18.404Z
tags: 
editor: markdown
dateCreated: 2020-12-20T17:15:28.983Z
---


# Определения о доказательства
## 1. Теорема о структуре общего решения неоднородной системы линейных алгебраических уравнений

Пусть $Ax = b$ - совместная СЛАУ

$\tilde x$ - частное решение $Ax = b$

$\Phi_1, \dots, \Phi_k$ - ФСР соответствующей однородной системы $Ax = 0$

Тогда общее решение $Ax = b$ равно:

$$
x = \tilde x + \sum_{i=0}^k \alpha_i \Phi_i \\
\alpha_i \in \R
$$

**Доказательство**

Пусть $x_0$ - произвольное решение СЛАУ $Ax = b$

По свойствам решений $x_0 - \tilde x$ - решение $Ax = 0$. Применим теорему о структуре общего решения однородной СЛАУ:

$$
x_0 - \tilde x = \sum_{i=1}^k \alpha_i \Phi_i \implies x_0 = \tilde x + \sum_{i=1}^k \alpha_i \Phi_i
$$

## 2. Формула скалярного произведения векторов в $\R^3$

Пусть

$$
\vec a = a_1 \vec e_1 + a_2 \vec e_2 + a_3 \vec e_3 \\
\vec b = b_1 \vec e_1 + b_2 \vec e_2 + b_3 \vec e_3
$$

Тогда

$$
(\vec a, \vec b) = \begin{pmatrix}
    a_1 & a_2 & a_3
\end{pmatrix} \cdot \begin{pmatrix}
    (e_1, e_1) & (e_1, e_2) & (e_1, e_3) \\
    (e_2, e_1) & (e_2, e_2) & (e_2, e_3) \\
    (e_3, e_1) & (e_3, e_2) & (e_3, e_3) \\
\end{pmatrix} \cdot \begin{pmatrix}
    b_1 \\ b_2 \\ b_3
\end{pmatrix}
$$

**Доказательство**

$(\vec a, \vec b) = (a_1 \vec e_1 + a_2 \vec e_2 + a_3 \vec e_3, b_1 \vec e_1 + b_2 \vec e_2 + b_3 \vec e_3)$

По линейности скалярного произведения:

$
(a_1 \vec e_1, b_1 \vec e_1 + b_2 \vec e_2 + b_3 \vec e_3) + (a_2 \vec e_2, b_1 \vec e_1 + b_2 \vec e_2 + b_3 \vec e_3) + (a_3 \vec e_3, b_1 \vec e_1 + b_2 \vec e_2 + b_3 \vec e_3) = \\
= (a_1 \vec e_1, b_1 \vec e_1) + (a_1 \vec e_1, b_2 \vec e_2) + (a_1 \vec e_1, b_3 \vec e_3) + \\
{+} (a_2 \vec e_2, b_1 \vec e_1) + (a_2 \vec e_2, b_2 \vec e_2) + (a_2 \vec e_2, b_3 \vec e_3) + \\
{+} (a_3 \vec e_3, b_1 \vec e_1) + (a_3 \vec e_3, b_2 \vec e_2) + (a_3 \vec e_3, b_3 \vec e_3)
$

Вынесем скаляры за скобки

$
a_1 b_1 (\vec e_1, \vec e_1) + a_1 b_2 (\vec e_1, \vec e_2) + \dots + a_3 b_3 (\vec e_3, \vec e_3)
$

Группируя слагаемые получим умножение следующих матриц по определению:

$$
\begin{pmatrix}
    a_1 & a_2 & a_3
\end{pmatrix} \cdot \begin{pmatrix}
    (e_1, e_1) & (e_1, e_2) & (e_1, e_3) \\
    (e_2, e_1) & (e_2, e_2) & (e_2, e_3) \\
    (e_3, e_1) & (e_3, e_2) & (e_3, e_3) \\
\end{pmatrix} \cdot \begin{pmatrix}
    b_1 \\ b_2 \\ b_3
\end{pmatrix}

$$

## 3. Формула векторного произведения в правом ОНБ $\R^3$
Пусть $i, j, k$ - правый ортонормированный базис

$$
\vec a = a_x \vec i + a_y \vec j + a_z \vec k \\
\vec b = b_x \vec i + b_y \vec j + b_z \vec k
$$

Тогда

$$
\vec a \times \vec b = \begin{vmatrix}
    \vec i & \vec j & \vec k \\
    a_x & a_y & a_z \\
    b_x & b_y & b_z
\end{vmatrix}
$$

**Доказательство**

$
\vec a \times \vec b = (a_x \vec i + a_y \vec j + a_z \vec k) \times (b_x \vec i + b_y \vec j + b_z \vec k) = \\
= (a_x \cdot b_x) i \times i + (a_x \cdot b_y) i \times j + (a_x \cdot b_z) i \times k + \\
{+} (a_y \cdot b_x) j \times i + (a_y \cdot b_y) j \times j + (a_y \cdot b_z) j \times k + \\
{+} (a_z \cdot b_x) k \times i + (a_z \cdot b_y) k \times j + (a_z \cdot b_z) k \times k
$

Воспользуемся свойствами $a \times a = 0$ и $(i, j, k)$ - правый ОНБ

$
(a_x \cdot b_y) i \times j + (a_x \cdot b_z) i \times k + (a_y \cdot b_x) j \times i + (a_y \cdot b_z) j \times k + (a_z \cdot b_x) k \times i + (a_z \cdot b_y) k \times j = \\
= (a_x \cdot b_y) k + (a_x \cdot b_z) j - (a_y \cdot b_x) k + (a_y \cdot b_z) i - (a_z \cdot b_x) j - (a_z \cdot b_y) i = \\
= (a_y b_z - a_z b_y) i + (a_x b_y - a_z b_x) j + (a_x b_y - a_y b_x) k = \\
= \begin{vmatrix}
    \vec i & \vec j & \vec k \\
    a_x & a_y & a_z \\
    b_x & b_y & b_z
\end{vmatrix}
$

## 4. Всякое линейное уравнение на координаты точки задает плоскость. Всякая плоскость задается линейным уравнением

**Доказательство 2**:

Пусть задана плоскость $P$ и $M_0(x_0, y_0, z_0) \in P$. $\quad \vec n \bot P, \vec n(A, B, C)$

Тогда

$M(x, y, z) \in P \iff (\vec n, \overrightarrow{M_0M}) = 0 \iff A(x - x_0) + B(y - y_0) + C(z - z_0) = 0 \\
A_x - A_{x_0} + B_y - B_{y_0} + C_z - C_{z_0} = 0 \\
A_x + B_y + C_z - (A_{x_0} + B_{y_0} + C_{z_0}) = 0 \\
A_x + B_y + C_z + D = 0
$

Соответственно плоскость задана множеством точек, ей принадлежащих

**Доказательсво 1**:

Пусть $Ax + By + Cz + D = 0, A^2 + B^2 + C^2 > 0, M(x, y, z)$ удовлетворяет этому уравнению

Пусть $M_0(x_0, y_0, z_0)$ также удовлетворяет уравнению:

$Ax + By + Cz - (Ax_0 + By_0 + Cz_0) = A(x - x_0) + B(y - y_0) + C(z - z_0) = 0 \iff \\
\iff (\vec n, \overrightarrow{M_0M}) = 0 \iff$ по определению $Ax + By + Cz + D = 0$ задает плоскость

## 5. Формула вычисления расстояния от точки до плоскости

Пусть $P: Ax + By + Cz + D = 0$

$M(x_0, y_0, z_0)$ - данная точка

Тогда

$$
\rho(P, M) = \frac{|Ax_0+ By_0 + Cz_o + D|}{\sqrt{A^2 + B^2 + C^2}}
$$

**Доказательство**:

```diagram
PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSIyODFweCIgaGVpZ2h0PSIxNzFweCIgdmlld0JveD0iLTAuNSAtMC41IDI4MSAxNzEiIGNvbnRlbnQ9IiZsdDtteGZpbGUgaG9zdD0mcXVvdDtlbWJlZC5kaWFncmFtcy5uZXQmcXVvdDsgbW9kaWZpZWQ9JnF1b3Q7MjAyMC0xMi0yMVQxNDoyNDozMi43MTBaJnF1b3Q7IGFnZW50PSZxdW90OzUuMCAoWDExKSZxdW90OyBldGFnPSZxdW90O2ZvRWs1Yl9RU3d6Vkp3bmdqMmpyJnF1b3Q7IHZlcnNpb249JnF1b3Q7MTQuMS4xJnF1b3Q7IHR5cGU9JnF1b3Q7ZW1iZWQmcXVvdDsmZ3Q7Jmx0O2RpYWdyYW0gaWQ9JnF1b3Q7YlJ4Y0ZXXzRZRU5pTUVXQ21lVlQmcXVvdDsgbmFtZT0mcXVvdDtQYWdlLTEmcXVvdDsmZ3Q7N1ZqTFR1TXdGUDJhU013R05YRmJZQW1GZ1EwakpCWXpMSzNra2xqanhKWGp0aWxmUDNaem5aY0RwZE5VVTlGWnhUNSszbk51anAxNFpKWVc5NUxPazBjUkFmZUNVVlI0NU5ZTEFuL3FCL3Boa0hXSlhKSnBDY1NTUmRpcEJwN1pHeUE0UW5UQklzaGJIWlVRWExGNUd3eEZsa0dvV2hpVlVxemEzVjRGYjY4NnB6RTR3SE5JdVl2K1pKRktNSXJKcU1ZZmdNV0pYZGtmWVV0S2JXY0U4b1JHWXRXQXlKMUhabElJVlpiU1lnYmNrR2Q1S2NkOWY2ZTEycGlFVEgxbUFBcXhwSHlCc2VHKzFOb0dxN2M0TjBVOUtlVWN1SWdsVFQxeU13ZkpVbEFndTIxUGRjUE5LbUVLbnVjME5ET3NkRFpvTEZFcDF6VmZGMTlaQVZaZlU4K3hxSVVtTjI0c0dONFNwSUtpQVdGczl5RDB1bkt0dTJDcjFxUWNnb2sybmlMdnExcTI0Qkt4cENHWnhTaG1TbHhOWFpPcEM4aG5QN2RrTzdlUVJkY21IM1V0NURUUFdkam01MTBLSUdwbHFFdEFJOEJKVDN3V2s4Q3BZc3QyWHZjRmpTczhDYVozVXZGTExFOXJPMjJIdDF3c1pBZzRxcG1IV3lZaVhRRVVsVEVvWjZLTkJsWFluNUpsL1BWbHFkSjhYMW02RTQzOWc4bHk1Y2p5ZUZibzFXWm1kWHkramI0NVdta25VRzExY2lYRmI1Z0pMb3cxWlNLRGpkTnczb0VvWjNGbUpOWXFic3pLK0FyVExuK05EU21MSXJOTXI0dEpzY2dpTUpzZnlLc2Nya2V1VjEzMTVFd3dnRlg1dnNPK0YweTVJVFppUzEyTVRUR3ptSjZ1QVg5ZFNjaWs0MG9YcmlUalEwbXkyL0dCQkRZNDEySEw5UzhrWTFONU1aWHppYTNlRnMzRzIvVTIzc3AzdmZXMkhvbmZkVThQeDZZKzYzZVZVVnJqSkFmenU4Qjk1WDZjRlQ0YUhqN2YvQzlzZU4yM2E5SmplSDEzc3lIZXJwNkw3OFBwTU4xM3RCekt4M2E4YjdrKzltNzhSMkkrNHk2NVYwTmR0cm9URFdnKzB4TVQ1ZTl2d052VUhWQ1VpejFGcVU1OGY3Y1RId3FtcW1HNi9OSW8xME5NWmVzZG9hUzE3YkhOZTRQRmpqVk51cCtkeDNoeHVOdzNUWGFXdTc1S25sOU1tcm5sYjhtcy8zbnlEL1BFL2FMK0tFOTZmM1NjMURlRVA4eUpjVGlKZGJYK00xeDJyLyt2azdzLyZsdDsvZGlhZ3JhbSZndDsmbHQ7L214ZmlsZSZndDsiPjxkZWZzLz48Zz48cGF0aCBkPSJNIDAgMTcwIEwgMTEwIDkwIEwgMjgwIDkwIEwgMTcwIDE3MCBaIiBmaWxsPSIjZmZmZmZmIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxwYXRoIGQ9Ik0gOTUgMTMwIEwgOTUgMTYuMzciIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHBhdGggZD0iTSA5NSAxMS4xMiBMIDk4LjUgMTguMTIgTCA5NSAxNi4zNyBMIDkxLjUgMTguMTIgWiIgZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cGF0aCBkPSJNIDE3NSAxMzAgTCAxNzUgNDYuMzciIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHBhdGggZD0iTSAxNzUgNDEuMTIgTCAxNzguNSA0OC4xMiBMIDE3NSA0Ni4zNyBMIDE3MS41IDQ4LjEyIFoiIGZpbGw9IiMwMDAwMDAiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PHJlY3QgeD0iMTc1IiB5PSIzMCIgd2lkdGg9IjkwIiBoZWlnaHQ9IjIwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogODhweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiA0MHB4OyBtYXJnaW4tbGVmdDogMTc2cHg7Ij48ZGl2IHN0eWxlPSJib3gtc2l6aW5nOiBib3JkZXItYm94OyBmb250LXNpemU6IDA7IHRleHQtYWxpZ246IGNlbnRlcjsgIj48ZGl2IHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTJweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6ICMwMDAwMDA7IGxpbmUtaGVpZ2h0OiAxLjI7IHBvaW50ZXItZXZlbnRzOiBhbGw7IHdoaXRlLXNwYWNlOiBub3JtYWw7IHdvcmQtd3JhcDogbm9ybWFsOyAiPk0oeDAsIHkwLCB6MCk8L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iMjIwIiB5PSI0NCIgZmlsbD0iIzAwMDAwMCIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxMnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5NKHgwLCB5MCwgejApPC90ZXh0Pjwvc3dpdGNoPjwvZz48cmVjdCB4PSI2NSIgeT0iMCIgd2lkdGg9IjQwIiBoZWlnaHQ9IjIwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMzhweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiAxMHB4OyBtYXJnaW4tbGVmdDogNjZweDsiPjxkaXYgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMDsgdGV4dC1hbGlnbjogY2VudGVyOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogIzAwMDAwMDsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+PGRpdj5uPC9kaXY+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9Ijg1IiB5PSIxNCIgZmlsbD0iIzAwMDAwMCIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxMnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5uPC90ZXh0Pjwvc3dpdGNoPjwvZz48cGF0aCBkPSJNIDk1IDQwIEwgMTc1IDQwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxyZWN0IHg9IjY1IiB5PSIxMzAiIHdpZHRoPSI4MCIgaGVpZ2h0PSIyMCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJub25lIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTAuNSAtMC41KSI+PHN3aXRjaD48Zm9yZWlnbk9iamVjdCBzdHlsZT0ib3ZlcmZsb3c6IHZpc2libGU7IHRleHQtYWxpZ246IGxlZnQ7IiBwb2ludGVyLWV2ZW50cz0ibm9uZSIgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ij48ZGl2IHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hodG1sIiBzdHlsZT0iZGlzcGxheTogZmxleDsgYWxpZ24taXRlbXM6IHVuc2FmZSBjZW50ZXI7IGp1c3RpZnktY29udGVudDogdW5zYWZlIGNlbnRlcjsgd2lkdGg6IDc4cHg7IGhlaWdodDogMXB4OyBwYWRkaW5nLXRvcDogMTQwcHg7IG1hcmdpbi1sZWZ0OiA2NnB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7ICI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDEycHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiAjMDAwMDAwOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyB3b3JkLXdyYXA6IG5vcm1hbDsgIj5OKHgxLCB5MSwgejEpPC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjEwNSIgeT0iMTQ0IiBmaWxsPSIjMDAwMDAwIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjEycHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPk4oeDEsIHkxLCB6MSk8L3RleHQ+PC9zd2l0Y2g+PC9nPjxyZWN0IHg9IjY1IiB5PSIzMCIgd2lkdGg9IjQwIiBoZWlnaHQ9IjIwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMzhweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiA0MHB4OyBtYXJnaW4tbGVmdDogNjZweDsiPjxkaXYgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMDsgdGV4dC1hbGlnbjogY2VudGVyOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogIzAwMDAwMDsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+SDwvZGl2PjwvZGl2PjwvZGl2PjwvZm9yZWlnbk9iamVjdD48dGV4dCB4PSI4NSIgeT0iNDQiIGZpbGw9IiMwMDAwMDAiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+SDwvdGV4dD48L3N3aXRjaD48L2c+PHBhdGggZD0iTSAxNjUgMTIwIEwgMTc1IDEyMCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDE2NSAxMzAgTCAxNjUgMTIwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMTA1IDUwIEwgMTA1IDQwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMTA1IDUwIEwgOTUgNTAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHBhdGggZD0iTSA5NiAxMzAgTCAxNzAuOCA0NC43OSIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDE3NC4yNiA0MC44NCBMIDE3Mi4yOCA0OC40MSBMIDE3MC44IDQ0Ljc5IEwgMTY3LjAxIDQzLjc5IFoiIGZpbGw9IiMwMDAwMDAiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PC9nPjxzd2l0Y2g+PGcgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ii8+PGEgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMCwtNSkiIHhsaW5rOmhyZWY9Imh0dHBzOi8vd3d3LmRpYWdyYW1zLm5ldC9kb2MvZmFxL3N2Zy1leHBvcnQtdGV4dC1wcm9ibGVtcyIgdGFyZ2V0PSJfYmxhbmsiPjx0ZXh0IHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtc2l6ZT0iMTBweCIgeD0iNTAlIiB5PSIxMDAlIj5WaWV3ZXIgZG9lcyBub3Qgc3VwcG9ydCBmdWxsIFNWRyAxLjE8L3RleHQ+PC9hPjwvc3dpdGNoPjwvc3ZnPg==
```


$\rho(P, M) = HM = |\text{пр}_{\vec n} \overrightarrow{NM}| = |\overrightarrow{NM}| \cos \varphi = \frac{|(\overrightarrow{NM}, \vec n)|}{|\vec n|} {}$

> $(\overrightarrow{NM}, \vec n) = |\overrightarrow{NM}| |\vec n| \cos \varphi = |\vec n| |\text{пр}_{\vec n} \overrightarrow{NM}|$

$\rho(P, M) = \frac{|(\overrightarrow{NM}, \vec n)|}{|\vec n|} = \frac{|Ax_0 + By_0 + Cz_0 - (Ax_1 + By_1 + cz_1)|}{\sqrt{A^2 + B^2 + C^2}} = \frac{|Ax_0 + By_0 + Cz_0 + D|}{\sqrt{A^2 + B^2 + C^2}}$

[Видосик с доказательством](https://youtu.be/tSjRBZh9q8c)

## 6. Формула Муавра

$$
z^n = r^n(\cos n \varphi + i \sin n \varphi)
$$

**Вывод формулы**:

Пусть $z = r (\cos \varphi + i\sin \varphi)$

База индукции
$
z^2 = z \cdot z = r \cdot r (\cos \varphi + i \sin \varphi)^2 \\
\cos^2 \varphi - \sin^2 \varphi + 2 i \cos \varphi \sin \varphi = \cos 2 \varphi + i \sin 2 \varphi 
$

Предположение

$
z^n = r^n (\cos n \varphi + i \sin n \varphi)
$

Шаг

$
z^{n+1} = z^n \cdot z = r^n (\cos n \varphi + i \sin n \varphi) \cdot r (\cos \varphi + i \sin \varphi) = \\
= r^{n + 1} (\cos n \varphi \cos \varphi + i \cos n \varphi \sin \varphi + i \cos \varphi \sin n \varphi - \sin \varphi \sin n \varphi) = \\
= r^{n + 1} (\cos((n + 1) \varphi) + i \sin((n + 1) \varphi))
$

