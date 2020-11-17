---
title: 1. Семинар по математической индукции
description: 
published: 1
date: 2020-09-22T11:56:45.907Z
tags: 
editor: undefined
dateCreated: 2020-09-10T09:58:11.867Z
---

# Практика по математический индукции
$$
3^{2n+2} + 8n - 9 \space \vdots \space 16\\
n=1; 80\space \vdots \space 16 \space \text{- верно}\\
\text{пусть} \space 3^{2n+2} + 8n - 9 \space \vdots \space 16 \\
\text{требуется доказать} \space 3^{2n+4} + 8(n+1) - 9 =\\
= 9\cdot 3^{2n+2} + 8n + 8 - 9 =\\
= (e^{2n+2} + 8n - 9) + 8(3^{2n+2} + 1) =\\
= \underbrace{(3^{2n+2} + 8n -9)}_{\dots \atop 16} + 
\underbrace{\underbrace{8}_{\dots \atop 8} \underbrace{(3^{2n+2}+1)}_{\dots \atop 2}}_{\dots \atop 16} \quad \vdots 16
$$

---

$$
x_1, \dots, x_n; \space x_i \ge -1\\
\text{числа одного знака}\\
(1+x_1)(1+x_2)\dots(1+x_n) \ge 1+x_1+x_2+\dots+x_n \space (\star)\\
n=1 \quad (1+x_1) \ge 1+x_1 \quad \text{верно}\\
$$
пусть $(\star)$ справедливо при всех $n$
$$
1+x_{n+1} \ge 0\\
(1+x_1)\dots(1+x_n)(1+x_{n+1}) \ge (1+x_1+\dots+x_n)(1+x_{n+1}) =\\
= 1 + x_1 + \dots + x_n + x_{n+1} + \underbrace{x_{n+1}(1 + x_1 + \dots + x_n)}_{\ge0} \ge\\
\ge 1 + x_1 + \dots + x_{n+1}
$$

---

$$
1 + 2 + \dots + n = \frac{n(n+1)}{2}\\
1 + 2^2 + \dots + n^2 = \frac{n(n+1)(2n+1)}{6}\\
1^3 + 2^3 + \dots + n^3 = \left( \frac{n(n+1)}{2} \right)^2 \quad (\star)\\ 
$$
пусть для всех $n$ справедливо $(\star)$
$$
n = 1 \quad \text{верно}\\
1^3 + 2^3 + \dots + n^3 (n + 1)^3 = \left( \frac{(n + 1)(n + 2)}{2} \right) =\\
= \left( \frac{n(n+1)}{2} \right)^2 + (n + 1)^3 = (n + 1)^2\left( \frac{n^2}{4} + (n + 1)^2 \right) =\\
=(n+1)^2\frac{n^2 + 4n + 4}{4} = \left(\frac{(n+1)(n+2)}{2}\right)^2
$$

---

$$
1\cdot1! + 2\cdot2! + \dots + n\cdot n! = S_n\\
S_1 = 1\\
S_2 = 5\\
S_3 = 23\\
S_4 = 119\\
\text{предположение} \space S_n = (n+1)! - 1\\
n = 1 \space \text{верно}\\
S_{n+1} = S_n + (n+1)\cdot(n+1)! = (n+1)! - 1 + (n+1)\cdot(n+1)! =\\
=(n+1)!\cdot(n+2) - 1 = (n+2)! - 1
$$

---

$$
\frac{1}{2!} + \frac{2}{3!} + \frac{3}{4!} + \dots + \frac{n-1}{n!} = S_n\\
S_2 = \frac{1}{2}\\
S_3 = \frac{5}{6}\\
S_4 = \frac{23}{24}\\
\text{предположение} \space S_n = \frac{n! - 1}{n!}\\
=\frac{1}{2!} + \dots + \frac{n-1}{n!} + \frac{n}{(n+1)!} =\\
=\frac{n! - 1}{n!} + \frac{n}{(n+1)!} = \frac{(n+1)(n! - 1) + n}{(n+1)!} =\\
=\frac{(n+1)! - 1}{(n+1)!}
$$
