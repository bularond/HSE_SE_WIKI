---
title: 11. Теорема Эйлера
description: 
published: 1
date: 2020-12-02T18:31:45.127Z
tags: 
editor: markdown
dateCreated: 2020-12-02T11:22:07.605Z
---

# Умножение комплексных чисел

$
z = x + iy \\
|z| = \sqrt{x^2 + y^2} \\
z = |z| (\cos{\varphi} + i\sin{\varphi}) \\
\varphi = \text{Arg} z = \{\text{arg} z + 2\pi k | k \in \Z\} \\
\text{arg} \in [0, 2\pi)
$

**Утверждение** $z_1 \cdot z_2 = r_1 \cdot r_2 (\cos(\varphi_1 + \varphi_2) + i \sin(\varphi_1 + \varphi_2))$

т. е. при умножении комплексных чисел их модули умножеются, а аргументы складываются

$\square z_1 \cdot z_2 = r_1(\cos\varphi_1 + i\sin\varphi_1) \cdot r_2 \cdot (\cos\varphi_2 + i\sin\varphi_2) = \\
= r_1 \cdot r_2 \cdot ((\cos\varphi_1 \cdot \cos\varphi_2 + (i)^2 \sin\varphi_1 \cdot\sin\varphi_2) + i(\cos\varphi_1 \cdot \sin\varphi_2 + \cos\varphi_2 \cdot \varphi_1)) = \\
= r_1 \cdot r_2 (\cos(\varphi_1 + \varphi_2) + i \cdot \sin(\varphi_ 1 + \varphi_2)) \blacksquare$

**Определение** Комплексно сопряженным к числу $z$ называется число $\bar{z}$

$\bar{z} = a - bi$, если $z = a + bi$

Комплексно сопряженное - это отраженное относительно вещественной оси

---

$$
z \cdot \bar{z} = (a + bi) \cdot (a - bi) = a^2 - (bi)^2 = a^2 + b^2 = |z|^2
$$

# Деление комплексных чисел

Если $z = a + bi$, то $a = \text{Re}(z), b = {Im}(z)$

1)
$$
\frac{z_1}{z_2} = \frac{z_1 \cdot \bar{z_2}}{z_2\cdot \bar{z_2}} = \frac{z_1 \cdot \bar{z_2}}{|z_2|^2}
$$

т. е. свели деление к умножению на $\frac{\bar{z_2}}{|z_2|^2} {}$

2)
$$
\frac{z_1}{z_2} = \frac{r_1}{r_2} (\cos(\varphi_1 - \varphi_2) + i\sin(\varphi_1 - \varphi_2))
$$

**Утверждение** Формула Эйлера

$e^{i\varphi} = \cos \varphi + i\sin\varphi$

т. е. $\text{Re}(e^{i\varphi}) = \cos\varphi\\
\text{Im}(e^{i\phi}) = \sin\varphi$

**Следствие** 

$$
\begin{array}{r l}
&e^{-i\varphi} = \cos\varphi - i\sin\varphi \\
\pm & \\
&e^{i\varphi} = \cos\varphi + i \sin\varphi
\end{array} \implies \\
\implies \cos\varphi - \frac{e^{i\varphi} + e^{-i\varphi}}{z}, \sin\varphi = \frac{e^{i\varphi} - e^{-i\varphi}}{zi}
$$

**Утверждение** (формула Муавра)

$$
z^n = r^n (\cos(n\varphi) + i\sin(n\varphi)), n \in \N \\
z = r \cdot (\cos\varphi + i\sin\varphi)
$$

$square$ Применим принцип мат. индукции

База: $n = 2$ доказано ранее

Предположим, что формула верна для всех $n \ge k$. Докажем, что из этого следует, что они верны и для $n = k + 1$

$z^{k+1} = z^k \cdot z = r^k(\cos(k\varphi) + i\sin(k\varphi)) \cdot r \cdot (\cos\varphi + i\sin\varphi) =\\ 
= r^{k+1}(\cos((k+1)\varphi) + i\sin((k+1) \varphi)) \implies$ это верно $\forall n \in \N$

**Замечание** Из формулы Эйлера следует возможность экспоненциальной формы записи комплексного числа

$$
z = r\cdot \underbrace{(\cos\varphi + i \sin\varphi)}_{e^{i\varphi}} = r \cdot e^{i\varphi}
$$

**Замечание**

$$
e^{i\pi} = \cos\pi + i\sin\pi = -1 \\
e^{i\pi} + 1 = 0
$$

# Извлечение комплексных корней

Пусть дано комплексное числа $w = \rho (\cos\psi + i \sin\psi)$ и число $n \in \N$ нужно найти $\sqrt[n]{w}$

То есть нужно найти все $z: w$. Пусть $z = r(\cos\varphi + i\sin\varphi)$

По формуле Мудавра:

$
z^n = r^n (\cos(n\varphi) + i\sin(n\varphi)) \\
\rho (\cos\psi + i\sin\psi) \\
\begin{cases}
\rho = r^n \\
\psi + 2\pi k = n \varphi, k \in \Z
\end{cases} \implies \\
\begin{cases}
r = \sqrt[n]{\rho} \quad \text{арифметический корень из } \rho > 0 \\
\varphi = \frac{\psi + 2\pi k}{n}, k \in \Z
\end{cases}
$

Достаточно рассмотреть только $k = 0, 1, 2, \dots, n-1$. Их ровно $n$ шутк $\implies$

$$
\sqrt[n]{w} = \{z = \sqrt[n]{\rho} \cdot (\cos(\frac{\psi + 2\pi k}{n}) + i\sin(\frac{\psi + 2\pi k}{n})) | k = \overline{0,n-1}\}
$$

**Пример** $\sqrt[6]{1} - ?$

$
1 = w = 1(\cos0 + i\sin0), \rho - 1, \psi = 0 \\
n = 6 \\
\sqrt[6]{1} = \{1(\cos(\frac{0 + 2\pi k}{6}) + i \sin(\frac{0 + 2\pi k}{6}))\ | k=\overline{0,5}\} = \\
= \{\cos\frac{\pi k}{3} + i\sin{\pi k}{3} | k = \overline{0,5}\}
$

# Основная теорема алгебры

Для любого многочлена

$$
a_n z^n + a_{n-1}z^{n-1} + \dots + a_1 z + a_0 = 0 \\
a_i \in \mathbb{C}, a_n \not=0
$$

$\exists$ корень $z_0 \in \mathbb{C} {}$

**Следствие** У мношочлена $P_n(z)$ степени $n, n \in \N$ есть ровно $n$ корней (с учетом кратности)

**Теорема Безу** Остаток от деления многочлена $f(x)$ на $x-c$ равен $f(c)$

$\square$ Разделим $f(x)$ с остатком на $x-c$:

$f(x) = (x - c) \cdot Q(x) + R(x)$, где $\text{deg} R(x) < \text{deg}(x - c) = 1 \implies R(x) = k$ - константа

Подставим $x = c$:

$f(c) = 0 \cdot Q(c) + k \implies k = f(c) \blacksquare$

Находим корень $z_0$ и делим на $z - z_0$. По теореме бузу остаток равен нулю $\implies$ получается многочлен

$$
P_n(z) = (z - z_0) \cdot \widetilde{P}_{n-1} (z)
$$

I. Комплексный многочлен степени $n$ всегда расладывается в произведение:

$$
P_n(z) = a_n(z - z_1) \cdot \dots \cdot (z - z_n) = a_n (z - z_1)^{\alpha_1} \cdot \dots \cdot (z - z_k)^{\alpha_k} \\
\alpha_1 + \dots + \alpha_k = n
$$

**Определение** Разложение многочлена на множетели $f(x) = g(x) \cdot h(x)$ называют нетривиальной, если 

$$
\text{deg}(g(x)) < \text{deg}(f) \\
\text{deg}(h(x)) < \text{deg}(f)
$$

**Определение** Многочлен называется приводимим, если существует его нетрифиальные разложение $f = g\cdot h$ и неприводимым в противном случае

**Замечание** Неприводимыми над $\mathbb{C}$ являются толко многочлены 1-ой степени: $(z - z_i)$
