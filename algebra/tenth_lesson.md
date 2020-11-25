---
title: 10. Комплексные числа
description: 
published: 1
date: 2020-11-25T13:14:09.290Z
tags: 
editor: markdown
dateCreated: 2020-11-25T13:14:09.290Z
---

# Комплексные числа

$
x + 5 = 3 \quad x = -2 \\
x^2 + 1 = 0 \quad \text{- не имеет решения в вещественных числах} \implies \text{нужно расширять понятие числа}
$

**Определение** Рассмотрим множество пар вещественных чисел (точек на плоскости) с двумя операциями

1) Сложения
2) Умножения

Возмем ПДСК. Пусть координаты точки $M$ это $(a, b)$. Тогда операции определяются так:

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

$\implies \forall$ пару вещественных чисел $(a, b)$ можно представить в виде:
$(a, b) = (a, 0) \cdot (1, 0) + (b, 0) \cdot (0, 1) = (a, 0) \cdot 1 + (b, 0) \cdot i$

---

Заметим, что точки вида $(\lambda, 0)$ соответствуют точкам на мрямой (оси абсцисс)

$$
(a, b) = a \cdot 1 + b \cdot i, \quad a, b \in \R
$$

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

Re - вещественная ось

Im - мнимая ось

$(r, \varphi)$ - триганометрическая форма записи

$$
x = r \cdot \cos{\varphi} \\
y = r \cdot \sin{\varphi}
$$

$r$ - называется модулем комплексного числа (это расстояние от $z$ до 0)

$$
r = \sqrt{x^2 + y^2} = |z| \\
z = x + iy = r\cdot \cos{\varphi} + i \cdot r \cdot \sin{\varphi} = r \cdot (\cos{\varphi} + i \cdot \sin{\varphi})
$$

$x + i \cdot y$ - алгебраическая форма записи комплексного числа 

$r \cdot (\cos{\varphi} + i \cdot \sin{\varphi})$

$\varphi$ - это аргумент комплексного числа ( это угол между радиус-вектором $z$ и полярном направляющим веществеттной оси)

$$
\varphi = Arg \space z = \{arg \space z + 2 \pi k | k \in \Z\}
$$

$arg \space z$ - главное значение аргумента

$arg \space z \in [0, 2\pi)$ или $(-\pi, \pi)$
