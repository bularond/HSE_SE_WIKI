---
title: 2. ФСР, ангем, теория групп
description: 
published: 1
date: 2020-12-21T01:58:36.069Z
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
a_1 b_1 (\vec e_1, \vec e_1) + a_1 b_2 (\vec a_1, \vec e_2) + \dots + a_3 b_3 (\vec e_3, \vec e_3)
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
PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSIyODFweCIgaGVpZ2h0PSIxNzFweCIgdmlld0JveD0iLTAuNSAtMC41IDI4MSAxNzEiIGNvbnRlbnQ9IiZsdDtteGZpbGUgaG9zdD0mcXVvdDtlbWJlZC5kaWFncmFtcy5uZXQmcXVvdDsgbW9kaWZpZWQ9JnF1b3Q7MjAyMC0xMi0yMFQxNzowMDo0NS4yNDRaJnF1b3Q7IGFnZW50PSZxdW90OzUuMCAoWDExKSZxdW90OyBldGFnPSZxdW90O284Y3FVWXhncXRubTg2cF94N1VzJnF1b3Q7IHZlcnNpb249JnF1b3Q7MTQuMS4xJnF1b3Q7IHR5cGU9JnF1b3Q7ZW1iZWQmcXVvdDsmZ3Q7Jmx0O2RpYWdyYW0gaWQ9JnF1b3Q7YlJ4Y0ZXXzRZRU5pTUVXQ21lVlQmcXVvdDsgbmFtZT0mcXVvdDtQYWdlLTEmcXVvdDsmZ3Q7N1ZoTmM1c3dGUHcxektRWER5RGJjWTZKa3lhWGRES1RRNXVqQmw1QVU0RThRclp4Zm4wbEk0RkFwTVFObnJwSlQwaFBuMjkzV1FrOHRNektXNDVYNlQyTGdYcWhINWNldXZiQ01KZ0hvWHlveUs2S0xOQzhDaVNjeExwVEUzZ2tMNkNEdm82dVNReEZxNk5nakFxeWFnY2psdWNRaVZZTWM4NjI3VzdQakxaWFhlRUVuTUJqaEtrYi9VNWlrZW9zWm40VHZ3T1NwR2Jsd05jdEdUYWRkYUJJY2N5MlZnamRlR2pKR1JOVktTdVhRQlY0QnBkcTNOZFhXdXVOY2NqRld3Wm9JamFZcm5WdWVsOWlaNUtWVzF5cG9wd1VVd3FVSlJ4bkhycGFBU2NaQ09EZHRvZW00V3FiRWdHUEt4eXBHYlpTRFRLV2lvektXaUNMejZRRXc2K3FGN29vaVVaWGJpNDZ2UTF3QWFVVjBybmRBcFByOHAzc29sc2xKOVVRTGJUcFhPTytiV2dMRnpxV1dwU1pHTlpLU2VxcEd6QmxRZVBaankwYXhoYnkrRkxwVWRZaWlvdUNSRzE4WG9VQTRwWkNYUUNzQkdjOStaa1lCNG9GMmJSMTNaZTBYdUdCRWJtVEdsOWtjTnFaYVR1NEZXek5JOUNqYkIwT1RJUzZCQWpNRXhET1JIc082clRmUk12MDQ5TlN5L3k5dEhRbm1nWkhvK1hDb2VYK3JKU3JMZFhxK3ZuaWYzRzRrazRnMnV3VWdyT2ZzR1NVS1d2S1dRNTdwNkcwRThLVUpMbWlXTEs0Tnl2bEswUzYvS1Z1eUVnY3EyVjZYWXl6ZFI2RDJ2eElYdVZnN2J0ZWRkR2ptWEFFcXdvQ0IzMHZuRk1GYkV3MnNwaW9ZbTVpY2pvci9IRXBRYk9PSzUyN2xFeVBSY2xoeDRjRzBNSmNwczEzUHpRWSs4cVRxa3htcG5wZDJvM1h1eUhjcW5lOTliYWVpTjkxVHcvSHB0N3FkN1ZSR3VORVIvTzcwSDNsdnAyVmdUWTgvWHdKUHJEaGRkK3VXWS9oOWQzTnhuaTdlaTYrZDU4SDZiNmo1VmcrZHVCOXkvV3hWL00vRWZPWmRzRzlHT3V5MVoxb1JQT1pmekpTL3Z3R1BNVHVpS1NjdjVPVStzUVBEanZ4b1NTaUhpYkxUMWE1R2FJcWczZUVDdGEyeDlyM0JoTTdWWmwwUHp0UDhlS3dlSzlNRHFhN3VVcE96bWUydG9JQlpmM1h5Vi9VaWZ0Ri9UdWQ5UDdvTUZMeEoyaXhzT1RpVHdZRUl5dldiOENPaUViNkhtbHA2T1MvVWY0QkNjbHE4K2U1NnQ3OHYwYzN2d0E9Jmx0Oy9kaWFncmFtJmd0OyZsdDsvbXhmaWxlJmd0OyI+PGRlZnMvPjxnPjxwYXRoIGQ9Ik0gMCAxNzAgTCAxMTAgOTAgTCAyODAgOTAgTCAxNzAgMTcwIFoiIGZpbGw9IiNmZmZmZmYiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PHBhdGggZD0iTSA5NSAxMzAgTCA5NSAxNi4zNyIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDk1IDExLjEyIEwgOTguNSAxOC4xMiBMIDk1IDE2LjM3IEwgOTEuNSAxOC4xMiBaIiBmaWxsPSIjMDAwMDAwIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxwYXRoIGQ9Ik0gMTc1IDEzMCBMIDE3NSA0Ni4zNyIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDE3NSA0MS4xMiBMIDE3OC41IDQ4LjEyIEwgMTc1IDQ2LjM3IEwgMTcxLjUgNDguMTIgWiIgZmlsbD0iIzAwMDAwMCIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cmVjdCB4PSIxNzUiIHk9IjMwIiB3aWR0aD0iOTAiIGhlaWdodD0iMjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3Qgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiA4OHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDQwcHg7IG1hcmdpbi1sZWZ0OiAxNzZweDsiPjxkaXYgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMDsgdGV4dC1hbGlnbjogY2VudGVyOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogIzAwMDAwMDsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+TSh4MCwgeTAsIHowKTwvZGl2PjwvZGl2PjwvZGl2PjwvZm9yZWlnbk9iamVjdD48dGV4dCB4PSIyMjAiIHk9IjQ0IiBmaWxsPSIjMDAwMDAwIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjEycHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPk0oeDAsIHkwLCB6MCk8L3RleHQ+PC9zd2l0Y2g+PC9nPjxyZWN0IHg9IjY1IiB5PSIwIiB3aWR0aD0iNDAiIGhlaWdodD0iMjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3Qgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiAzOHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDEwcHg7IG1hcmdpbi1sZWZ0OiA2NnB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7ICI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDEycHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiAjMDAwMDAwOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyB3b3JkLXdyYXA6IG5vcm1hbDsgIj48ZGl2Pm48L2Rpdj48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iODUiIHk9IjE0IiBmaWxsPSIjMDAwMDAwIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjEycHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPm48L3RleHQ+PC9zd2l0Y2g+PC9nPjxwYXRoIGQ9Ik0gOTUgNDAgTCAxNzUgNDAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHJlY3QgeD0iNjUiIHk9IjEzMCIgd2lkdGg9IjgwIiBoZWlnaHQ9IjIwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogNzhweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiAxNDBweDsgbWFyZ2luLWxlZnQ6IDY2cHg7Ij48ZGl2IHN0eWxlPSJib3gtc2l6aW5nOiBib3JkZXItYm94OyBmb250LXNpemU6IDA7IHRleHQtYWxpZ246IGNlbnRlcjsgIj48ZGl2IHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTJweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6ICMwMDAwMDA7IGxpbmUtaGVpZ2h0OiAxLjI7IHBvaW50ZXItZXZlbnRzOiBhbGw7IHdoaXRlLXNwYWNlOiBub3JtYWw7IHdvcmQtd3JhcDogbm9ybWFsOyAiPk4oeDEsIHkxLCB6MSk8L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iMTA1IiB5PSIxNDQiIGZpbGw9IiMwMDAwMDAiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+Tih4MSwgeTEsIHoxKTwvdGV4dD48L3N3aXRjaD48L2c+PHJlY3QgeD0iNjUiIHk9IjMwIiB3aWR0aD0iNDAiIGhlaWdodD0iMjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3Qgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiAzOHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDQwcHg7IG1hcmdpbi1sZWZ0OiA2NnB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7ICI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDEycHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiAjMDAwMDAwOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyB3b3JkLXdyYXA6IG5vcm1hbDsgIj5IPC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9Ijg1IiB5PSI0NCIgZmlsbD0iIzAwMDAwMCIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxMnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5IPC90ZXh0Pjwvc3dpdGNoPjwvZz48cGF0aCBkPSJNIDE2NSAxMjAgTCAxNzUgMTIwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMTY1IDEzMCBMIDE2NSAxMjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHBhdGggZD0iTSAxMDUgNTAgTCAxMDUgNDAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ic3Ryb2tlIi8+PHBhdGggZD0iTSAxMDUgNTAgTCA5NSA1MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDk2LjA0IDEzMiBMIDE3MC44NSA0NC44MyIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDE3NC4yNyA0MC44NSBMIDE3Mi4zNyA0OC40NCBMIDE3MC44NSA0NC44MyBMIDE2Ny4wNiA0My44OCBaIiBmaWxsPSIjMDAwMDAwIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjwvZz48c3dpdGNoPjxnIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSIvPjxhIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAsLTUpIiB4bGluazpocmVmPSJodHRwczovL3d3dy5kaWFncmFtcy5uZXQvZG9jL2ZhcS9zdmctZXhwb3J0LXRleHQtcHJvYmxlbXMiIHRhcmdldD0iX2JsYW5rIj48dGV4dCB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjEwcHgiIHg9IjUwJSIgeT0iMTAwJSI+Vmlld2VyIGRvZXMgbm90IHN1cHBvcnQgZnVsbCBTVkcgMS4xPC90ZXh0PjwvYT48L3N3aXRjaD48L3N2Zz4=
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

