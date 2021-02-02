---
title: 10. Комплексные числа
description: 
published: 1
date: 2021-02-02T14:45:52.611Z
tags: 
editor: markdown
dateCreated: 2020-11-25T13:14:09.290Z
---

# Комплексные числа

$
x + 5 = 3 \quad x = -2 \\
x^2 + 1 = 0 \quad \text{- не имеет решения в вещественных числах} \implies \text{нужно расширять понятие числа}
$

**Определение** Возьмем множество пар вещественных чисел (точек на плоскости) с двумя операциями

1) Сложения
2) Умножения

Возмем ПДСК. Пусть координаты точки $M$ это $(a, b)$. Тогда операции можно определить так:

Сложение
$$
(a, b) + (c, d) = (a + c, b + d)
$$

Произведение
$$
(a, b) \cdot (c, d) = (a \cdot c - b \cdot d, a \cdot d + b \cdot c) \\
a, b, c, d \in \R
$$

**Замечание** $(0, 1)^2 = (-1, 0) \iff i^2 = -1$

$$
\begin{matrix}
i = (0, 1) \\
1 = (1, 0)
\end{matrix} \quad \text{базисные векторы на плоскости}
$$


$\forall$ пару - вещественное число - $(a, b)$ можно представить в виде:
$(a, b) = (a, 0) \cdot (1, 0) + (b, 0) \cdot (0, 1) = (a, 0) \cdot 1 + (b, 0) \cdot i = a \cdot 1 + b \cdot i$ 

$$
(a, b) = a + b \cdot i, \quad a, b \in \R - Алгебраическая\ форма\ записи\ числа
$$

Точки вида $(\lambda, 0)$ соответствуют точкам на прямой (оси абсцисс)


## Алгебраические свойства

> Множество комплексных чисел: $\mathbb{C}$, его элементы: $z$

1. $\forall z_1, z_2 \in \mathbb{C}: z_1 + z_2 = z_2 + z_1$
2. $\exists 0 \in \mathbb{C}: z + 0 = z = 0 + z$
3. $\forall z \in \mathbb{C}: \exists -z: z + (-z) = (-z) + z = 0$
4. $\forall z_1, z_2, z_3 \in \mathbb{C}: z_1 + (z_2 + z_3) = (z_1 + z_2) + z_3$
5. $\forall z_1, z_2 \in \mathbb{C}: z_1 \cdot z_2 = z_2 \cdot z_1$
6. $\forall z_1, z_2, z_3 \in \mathbb{C}: z_1 \cdot (z_2 \cdot z_3) = (z_1 \cdot z_2) \cdot z_3$
7. $\exists$ нейтральный элемент: $(1, 0): \forall z \in \mathbb{C} \quad (1, 0) \cdot z = z \cdot (1, 0) = z$
8. $\forall z \in \mathbb{C}, z \not= 0 \quad \exists z^{-1} \in \mathbb{C}: z \cdot z^{-1} = z^{-1} \cdot z = 1$
9. $\forall z_1, z_2, z_3 \in \mathbb{C} \quad (z_1 + z_2) \cdot z_3 = z_1 \cdot z_3 + z_2 \cdot z_3$

---

$z = a + b \cdot i$
$Re(z) = a\ -$  Вещественная часть числа $z$
$Im(z) = b\ -$  Мнимая часть числа $z$


$(r, \varphi)\ -$ Возьмем полярные координаты вектора $(a, b)$ ($\varphi$ это угол, отложенный от оси абсцисс, $r$ $-$ длинна вектора)

$$
a = r \cdot \cos{\varphi} \\
b = r \cdot \sin{\varphi}
$$

$r$ $-$ называется модулем комплексного числа (расстояние от $z$ до 0)
$$
|z| = r = \sqrt{x^2 + y^2}
$$

$$
 \\
z = x + iy = r\cdot \cos{\varphi} + i \cdot r \cdot \sin{\varphi} = r \cdot (\cos{\varphi} + i \cdot \sin{\varphi})
$$

$z = r \cdot (\cos{\varphi} + i \cdot \sin{\varphi})\ -$ Тригонометрическая форма записи числа

$\varphi$ - это аргумент комплексного числа (это угол между радиус-вектором $z$ и полярном направляющим вещественной оси)

$$
\varphi = Arg \space z = \{arg \space z + 2 \pi k | k \in \Z\}
$$

$arg \space z$ $-$ Главное значение аргумента

$arg \space z \in [0, 2\pi)$ или $(-\pi, \pi)$
