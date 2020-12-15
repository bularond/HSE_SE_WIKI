---
title: 14. Продолжаем формулу Тейлора
description: 
published: 1
date: 2020-12-15T11:21:08.447Z
tags: 
editor: markdown
dateCreated: 2020-12-15T11:19:51.368Z
---

# Продолжаем тему прошлой лекции

4. $f(x) = \sin x; f^{(k)}(x) = \sin(x + k \frac{\pi}{2}); f^{(k)}(0) = \sin(k\frac{\pi}{2}) = \begin{cases}
    (-1)^m, k = 2m + 1, m=0,1,\dots \\
    0, k = 2m, m=0,1,\dots
\end{cases} \\
\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} + \dots + (-1)^n\frac{x^{2n+1}}{(2n+1)!} + o(x^{2n+1}), x\to 0$

5. $f(x) = \cos x; f^{(k)}(x) = \cos(x + k\frac{\pi}{2}); f^{(k)}(0) = \cos(k\frac{\pi}{2}) = \begin{cases}
    (-1)^m, k = 2m, m = 0, 1, \dots \\
    0, k = 2m + 1, m = 0, 1, \dots
\end{cases} \\
\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots + (-1)^n \frac{x^{2n}}{(2n)!} + o(x^{2n}), x \to 0$

## Формула Тейлора с остаточным членом в форме Лагранжа

Если определены $f(a), f'(a), \dots, f^{(n)}(a)$

$
T_n(x) = f(a) + \frac{f'(a)}{1!}(x - a) + \dots + \frac{f^{(k)}(a)}{n!}(x - a)^n \\
R_n(x) = f(x) - T_n(x), \\
R_n(a) = R_n'(a) = \dots = R_n^{(n)}(a) = 0
$

**Теорема** пусть $f(x)$ имеет производную порядка $(n + 1)$ в $O_n(a)$, тогда $\forall x \in O_n(a) (x \not= a)$ - между $a$ и $x$ найдется такая точка $\xi$, что 

$$
f(x) = f(a) + \frac{f'(a)}{1!}(x - a) + \dots + \frac{f^{(n)}(a)}{n!}(x - a)^n + \underbrace{\frac{f^{(n + 1)}(\xi)}{(n+1)!}(x - a)^{n+1}}_{\text{Остаточныйй член в форме Лагранжа}}
$$

**Доказательство** пусть $g(x) = (x - a)^{n + 1}, g(a) = g'(a) = \dots = g^{(n)}(a) = 0 {}$

если $x \not= a; g^{(n)}(x) \not= 0, 0 \le k \le n$

$\frac{R_n(x)}{(x - a)^{n+1}} = \frac{R_n(x)}{g(x)} = \frac{R_n(x) - R_n(a)}{R(x) - g(a)} = \frac{R'_n(\xi_1) - R'_n(a)}{g'(\xi_1) - g'(a)} = \frac{R''_n(\xi_2)}{g''(\xi_2)} = \dots = \frac{R^{(n)}}{g^{(n)}(\xi_n)} = \\
= \frac{R^{(n+1)(\xi_{n+1})}}{(\xi_{n+1})} = \frac{R_n^{(n+1)}(\xi)}{g^{(n + 1)}(\xi)} = \frac{f^{(n + 1)}(\xi)}{(n + 1)!} {}$

Обозначим $\xi = \xi_{n + 1} {}$

$R_n(x) = \frac{f^{(n+1)}(\xi)}{(n + 1)!}(x - a)^{n + 1} {}$

# Примеры решения задач

$$
\underset{x\to0}{\lim} \frac{\sin^3 3x}{\sqrt{1 + \sin^2 2x} - \sqrt{1 + \sin^2 x}} = \underset{x\to0}{\lim} \frac{9x^2}{1 + \frac{1}{2}\sin^2 2x - 1 - \frac{1}{2} \sin^2 x + o(x^2)} = \\
\underset{x\to0}{\lim} \frac{9x^2}{\frac{1}{2}(2x + o(x))^2 - \frac{1}{2}(x + o(x))^2} = \underset{x\to0}{\lim} \frac{9x^2}{\frac{3}{2}x^2 + o(x^2)} = 6
$$

$$
\lim_{x\to1/2}(\frac{\pi}{\cos x} - 2x \tg x) = \left\{\begin{matrix}
    y = x - \frac{\pi}{2} \\
    x = y + \frac{\pi}{2}
\end{matrix}\right\} = \lim_{y\to0} (-\frac{\pi}{\sin y} + 2(y + \frac{\pi}{2})\frac{\cos y}{\sin y}) = \\
= \lim_{y \to 0}\frac{2 y \cos y}{\sin y} = 2
$$

$$
\lim_{x\to\infin} x^2 \ln \cos \frac{\pi}{x} = \begin{Bmatrix}
    y = \frac{1}{x} \\
    x = \frac{1}{y}
\end{Bmatrix} = \lim_{y\to0} \frac{1}{y^2} \ln \cos \pi y = \\
= \lim_{y\to0} \frac{1}{y^2} \ln \left(1 - \frac{\pi^2y^2}{2} + o(y^2)\right) = \lim_{y\to0} \frac{1}{y^2} \left[-\frac{\pi^2 y^2}{2} + o(y^2) + o(-\frac{\pi^2 y^2}{2}) o(y^2)\right] = \lim_{y \to 0} \frac{1}{y^2} (-\frac{\pi y^2}{2} + o(y^2)) = -\frac{\pi^2}{2}
$$

$
f(x) = \frac{1}{2x + 3} 
$ с остаточным членом вида $o(x^3), \quad o((x + 5)^3)$

$$
\frac{1}{3} \cdot \frac{1}{1 + \frac{2}{3}x} = \frac{1}{3} \left(1 + \frac{2}{3}x\right)^{-1} = \frac{1}{3} (1 - \frac{2}{3}x + \frac{4}{3} x^2 - \frac{8}{27} x^3 + o(x^3))
$$

$$
\frac{1}{1 - q} = 1 + q + q^2 + q^3 + o(q^3); q = -\frac{2}{3}x \\
(1 + \frac{2}{3} x)^{-1} = 1 + (-1) \frac{2}{3} x + \frac{(-1)(-1 - 1)}{2!} \frac{4x^2}{9} + \frac{(-1)(-1 - 1)(-1-2)}{3!} \frac{8}{27}x^3 + o(x^3)
$$

---

$$
f(x) = \ln \frac{x - 5}{x - 4} \\
\text{с остаточным членом } o(x^2) \\
\ln(1 + x) = x - \frac{x^2}{2} + o(x^2) \\
\ln(x - 5) - \ln(x - 4) \\
\ln\frac{5 - x}{4 - x} = \ln (5 - x) - \ln(4 - x) = \ln \frac{5}{4} + \ln (1 - \frac{x}{5}) - \ln(1 - \frac{x}{4}) = \\
= \ln{5}{4} - \frac{x}{5} - \frac{x^2}{2 \cdot 25} + o(x^n) - (- \frac{x}{4} - \frac{x^2}{2\cdot 16} + o(x^3)) = \\
= \ln \frac{5}{4} + \frac{1}{20} x + \frac{9}{800} x^2 + o(x^2)
$$

