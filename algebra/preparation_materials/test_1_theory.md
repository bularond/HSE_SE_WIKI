---
title: 1. Контрольная работа. Теоретическая часть
description: 
published: 1
date: 2020-11-17T13:49:10.046Z
tags: 
editor: undefined
dateCreated: 2020-10-14T17:21:40.677Z
---

[Список вопросов с доказательством для подготовки к теоретической части контрольной работы](/вопросы_к_кр1_с_доказательством_2020_v1.pdf)

# Определения и доказательства
## 1. Что происходит с произведением матриц при транспонировании? Ответ обосновать.
$$
(A\cdot B)^T = B^T \cdot A^T
$$

Доказательство:
$$
\square \ [(A\cdot B)^T]_{ij} = [A\cdot B]_{ji} = \sum_{r=1}^{n} [A]_{jr} \cdot [B]_{ri} = \\
= \sum_{r=1}^{n} [A^T]_{rj} \cdot [B^T]_{ir} = [B^T \cdot A^T]_{ij} \ \blacksquare
$$

## 2. Сформулировать и доказать критерий существования обратной матрицы. Свойства определителя предполагаются известными.

$$
\det A \not = 0 \iff \exists A^{-1}
$$

**Доказательство**

$
\text{Докажем} \ \exists A^{-1} \implies detA \not= 0 \\
\text{По определению } A \cdot A^{-1} = E \text{, тогда} \ \det(A\cdot A^{-1}) = \det E = 1 = \det A \cdot \det A^{-1} \\
\text{Получаем противоречие при } \det A = 0
$

Докажем $\det A \not= 0 \implies \exists A^{-1} \space$
$$
\text{Рассмотрим матрицу } B \text{ такую, что} \\
B = \frac{1}{\det A} \widetilde{A}; \widetilde{A} = 
\begin{pmatrix}
A_{11} & A_{12} & \dots & A_{1n} \\
A_{21} & A_{22} & \dots & A_{2n} \\
\dots & \dots & \ddots & \dots \\
A_{n1} & A_{n2} & \dots & A_{nn}
\end{pmatrix}^T \\

[A \cdot B]_{ij} = \sum_{r=1}^n [A]_{ir} \cdot [B]_{rj} = \frac{1}{\det A} \left[\sum_{r=1}^n a_{ir} A_{jr} \right]_{ij} =
\begin{cases}
1 & i = j & (\text{8 свойство}) \\
0 & i \not= j & (\text{9 свойство})
\end{cases} = [E]_{ij}
$$

## 3. Какие три условия достаточно наложить на функцию от столбцов матрицы, чтобы она обязательно была детерминантом? Ответ обоснуйте для матриц второго порядка.
Функция должна быть полилинейна (линейна по строкам), кососиметрична (менять знак, при перестановки строк) и от $E$ равняться еденице -- тогда она является определителем

$$
f\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix} = f\left(\binom{a_{11}}{a_{21}}, \binom{a_{12}}{a_{22}}\right) = f\left(a_{11} \binom{1}{0} + a_{21} \binom{0}{1}, \binom{a_{12}}{a_{22}}\right) \overset{\text{полилинейность}}{=} \\

= a_{11} f\left(\binom{1}{0}, \binom{a_{12}}{a_{22}}\right) + a_{21} f\left(\binom{0}{1}, \binom{a_{12}}{a_{22}}\right) = \\

= a_{11} a_{12} f \begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix} + 

a_{11} a_{22} f \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} +

a_{12} a_{21} f \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} +

a_{21} a_{22} f \begin{pmatrix}
0 & 0 \\
1 & 1
\end{pmatrix} \overset{\text{кососимметричность}}{=} \\
= a_{11} a_{22} f \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} -

a_{12} a_{21} f \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} =

f(E_n) \det A = \det A
$$

## 4. Сформулировать и доказать утверждение о том, что кососимметричность для линейной функции эквивалентна обнулению на паре совпадающих элементов.

$$
\begin{array}{r l}
\text{Дано: } & \det(a, a) = 0 \\
\text{Доказать: } & \det(v, u) = -\det(u, v)
\end{array} \\
0 = \det(v + u, v + u) = \det(v, u) + \det(v, v) + \det(u, u) + \det(u, v) = \det(v, u) + \det(u, v) \\
\det(v, u) + \det(u, v) = 0 \\
\det(v, u) = -\det(u, v)
$$

---

$$
\begin{array}{r l}
\text{Дано: } & \det(v, u) = -\det(u, v) \\
\text{Доказать: } & \det(a, a) = 0
\end{array} \\
\det(a, a) = -\det(a, a) \implies \det(a, a) = 0
$$

## 5. Чему равен определитель произведения двух квадратных матриц? Ответ обосновать.

Возьмем $f(B) = \det(A \cdot B)$. Докажем, что функция $f$ - кососимметрична и полилинейна

1. Пусть в $B$ равны столбцы $i$ и $j$, тогда в $A \cdot B$ столбцы тоже одинаковы $\implies \det(A \cdot B) = 0 \implies f(B) = 0 \implies f$ -- кососимметрична
2. Пусть $i$ столбец в матрице $B$ имеет вид $\lambda b' + \mu b''$, тогда в матрице $A \cdot B$ столбец $i$ будет иметь вид $\lambda A b' + \mu A b''$ выполняется свойство полиинейности для определителся $\implies$ выполняется свойство полилинйности

Так как $f$ полилинйна и кососимметрична $\implies f(B) = f(E_n) \cdot \det B$. Тогда $\det(A \cdot B) = f(b) = f(E_n) \det B = \det(A \cdot E_n) \det B = \det A \cdot \det B$ ч. т. д.

## 6. Выписать формулы Крамера для квадратной матрицы произвольного порядка и доказать их.

Формулы Крамера для квадратной матрицы имеют вид:
$$
x_1 A_1 + x_2 A_2 + \dots + x_n A_n = b \\
x_i = \frac{\Delta_i}{\det A}; \Delta_i = \det(A_1, A_2, \dots, A_{i-1}, b, A_{i+1}, \dots, A_n)\\
$$

Доказательство:
$$
\square \ \Delta_i = \det(A_1, A_2, \dots, A_{i-1}, b, A_{i+1}, \dots, A_n) \overset{Расписываем \ b}{=} \\
= \det(A_1, A_2, \dots, A_{i-1}, \sum_{j=1}^{n} x_j \cdot A_j, A_{i+1}, \dots, A_n) \overset{Полилинейность}{=} \\
= \sum_{j=1}^n x_j \det(A_1, A_2, \dots, A_{i-1}, A_j, A_{i+1}, \dots, A_n) \overset{\text{При} \ j \neq i \ \text{слагаемое преарвщается в ноль}}{=} \\
= x_i \det(A_1, A_2, \dots, A_{i-1}, A_i, A_{i+1}, \dots, A_n) = x_i \det A \ \blacksquare
$$

## 7. Сформулировать и доказать критерий линейной зависимости.
$a_1, a_2, \dots, a_s$ - л. з. $\iff$ хотя бы одна из $a_1, a_2, \dots, a_s$ линейно выразится через другие

Необходимость:
$$
\text{Дано: } a_1, a_2, \dots, a_s - \text{л. з.} \\
\text{Доказать: найдется одна, выражаемая через другие линейно} \\
\square \ \exists \alpha_1, \alpha_2, \dots, \alpha_s : \alpha_1 a_1 + \alpha_2 a_2 + \dots + \alpha_s 
a_s = 0 (\text{по определению л. з.}) \\
a_1 = -\frac{\alpha_2}{\alpha_1}a_2 - \frac{\alpha_3}{\alpha_1}a_3 - \dots - \frac{\alpha_s}{\alpha_1}a_s \ \blacksquare
$$

Достаточность:
$$
\text{Дано: найдется одна, выражаемая через другие линейно} \\
\text{Доказать: } a_1, a_2, \dots, a_s - \text{л. з.} \\
\square \ a_1 = \beta_2 a_2 + \beta_3 a_3 + \dots + \beta_s a_s \\
a_1 - \beta_2 a_2 - \beta_3 a_3 - \dots - \beta_s a_s = 0 \ \blacksquare
$$

## 8. Как связан ранг транспонированной матрицы с рангом исходной матрицы? Ответ обосновать.

Ранги этих матриц равны
$$
Rg A = Rg A^{T}
$$

Доказательство:
$$
\square \ \text{Пусть } Rg A = r \implies \exists M_{i_1, \dots, i_r}^{j_1, \dots, j_r} \\
\text{Тогда в } A^T \text{ есть минор } N_{j_1, \dots, j_r}^{i_1, \dots, i_r} \text{ получившийся из } M \text{ операцией транспонирования и } \\
N \not= 0 \text{ по свойству определителя (1)} \implies Rg A^T \ge r = Rg A \\
Rg A \le Rg A^T \le Rg (A^T)^T = Rg A \implies Rg A = Rg A^T \ \blacksquare
$$

## 9. Сформулировать и доказать следствие теоремы о базисном миноре для квадратных матриц (критерий невы-рожденности).

**Следствие 1** Ранг матрицы = максимальному числу ее линейно независимых строк (столбцов)

$\square$ Пусть $Rg A = r$ и количество л. н. с. $= k$

1. Так как есть r л. н. строк (т. к. $Rg A = r$ - базисные строки) по теореме о базисном миноре $\implies k \ge r$ (по определению $k$) 
2. Вычеркнем из $A$ все строки, кроме $k$, получим матрицу $A'$ размером $k \cdot k$.
$Rg A' = k$ (т. к. если бы было $Rg A' < k$, то только часть строк была бы базисной и какая-то строка была бы линейной комбинацией остальных (по теореме о базисном миноре) $\implies$ по критерию линейной зависимости строки были бы линйено зависимы --- противоречие)
Базисный минор $A'$ имеет порядок $k$ и является не равным нулю минором порядка $k$ исходной матрицы $\implies$ по определению ранга $r \ge k$

1 и 2 $\implies r = k \ \blacksquare$

**Следствие 2** 
Следующие 3 утверждения равносильны (для кв. матрицы $n \cdot n$):
1. $\det A \not= 0$
2. $Rg A = n$
3. Все строки л. н. з.

$\square$ Докажем (1) $\implies$ (2)
$\det A \not= 0 \implies$ найдется минор порядка $n \implies Rg A = n$

Докажем (2) $\implies$ (3)
$Rg A = n \implies$ все строки являются базисными $\implies$ (по т. о Базисном миноре) все строки л. н. з.

Докажем (3) $\implies$ (1)
Пусть $\det A = 0 \implies Rg A < n \implies$ (по т. о Базисном миноре) одна из строк является л. к. остальных $\implies$ по критерию л. з. строки являются л. з. --- противоречие $\blacksquare$ 