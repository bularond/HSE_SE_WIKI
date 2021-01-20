---
title: 13. Правила Лопиталя и ряд Тейлора
description: 
published: 1
date: 2021-01-20T17:29:36.288Z
tags: 
editor: markdown
dateCreated: 2020-12-12T12:13:38.435Z
---

# Правило Лопиталя

## Первое правило Лопиталя (неопределенность вида 0/0)
**Теорема** $f(x), g(x)$
1. $f, g$ непрерыны на $x \in [a, b]$
2. $f, g$ дифференцируемы в $(a, b)$
3. $\underset{x\to a+}{\lim} f(x) = \underset{x\to a+}{\lim} g(x) = 0$

Если 

$$
\lim_{x\to0+} \frac{f'(x)}{g'(x)} = A
$$

то 

$$
\lim_{x\to0+} \frac{f(x)}{g(x)} = A
$$

**Доказательство** положим $f(a) = g(a) = 0$; $f(x), g(x)$ непрерывны на $[a, b]$

$$
\frac{f(x)}{g(a)} = \frac{f(x) - f(a)}{g(x) - g(a)} = \frac{f'(\xi(x))}{g'(\xi(x))} = A \implies \lim_{x\to b+} \frac{f(x)}{g(x)} = A
$$

Замечания

1. Аналогичное утверждение справедливо для $x \in [b, a), b < a$, то есть для $\underset{x \to b-}{\lim}\thinspace$
2. Аналогичное утверждение справедливо для $\underset{x\to a}{\lim}\thinspace$

$$
\lim_{x\to0} \frac{\tg x - x}{x^3} = \lim_{x\to0} \frac{\frac{1}{\cos^2 x} - 1}{3x^2} = \lim_{x\to0} \frac{1 - \cos^2x}{cos^2x - 3x^2} = \lim_{x\to0} \frac{1 - \cos^2 x}{3x^2} = \lim_{x\to0} \frac{2\sin x \cos x}{6x} = \frac{1}{3}
$$

**Дополнение** $f(x), g(x)$

1. $f, g$ непрерывны на $[a, +\infin), a > 0$
2. $f', g'$ существует на $(a, +\infin)$
3. $g'(x) \not= 0, x \in (a, +\infin)$
4. $\underset{x\to+\infin}{\lim} \frac{f'(x)}{g'(x)} = A$, то $\underset{x\to+\infin}{\lim} \frac{f(x)}{g(x)} = A$

Если
$$
\lim_{x\to\infin+} \frac{f'(x)}{g'(x)} = A
$$

то

$$
\lim_{x\to+\infin} \frac{f(x)}{g(x)} = A
$$

**Доказательство** $y = \frac{1}{x}; y \in (0, \frac{1}{x}) \quad \underset{x\to+\infin}{\lim} f(x) = \underset{y\to0+}{\lim} f\left(\frac{1}{y}\right)$, аналогично $\underset{y\to0+}{\lim} g\left(\frac{1}{y}\right) = 0$

$f\left(\frac{1}{y}\right); g\left(\frac{1}{y}\right)$ дифференцируемо $y \in (0, \frac{1}{a})$

$$
\left(g\left(\frac{1}{y}\right)\right)'_y = \left(g'_x\left(\frac{1}{y}\right)\right) \cdot \left(-\frac{1}{y^2}\right) \not= 0 \\
\lim_{x\to+a} \frac{f(x)}{g(x)} = \lim_{y\to0+} \frac{f(1/y)}{g(1/y)} = \lim_{y\to0+} = \lim_{y\to0+} \frac{f'_x(1/y)(-1/y^2)}{g'_x(1/y)(-1/y^2)} = \lim_{x\to+\infin} \frac{f'(x)}{g'(x)}
$$

## Второе правило Лопиталя (неопределенность вида $\infin/\infin$)

$f(x), g(x)$
1. $f, g$ непрерывны на $(a, b]$
2. $f, g$ дифференциальны на $(a, b)$
3. $g'(x) \not=0, x \in (a, b)$
4. $\underset{x\to a+}{\lim} f(x) = \pm\infin; \underset{a+} g(x) = \pm\infin$

Если
$$
\lim_{x\to a+} \frac{f'(x)}{g'(x)} = A
$$
то
$$
\lim_{x\to a+} \frac{f(x)}{g(x)} = A
$$

## Многочлен Тейлора

$f(x); x = a$ пусть $f(a), f'(a), \dots, f^{(n)}(a)$ определено

**Определение**
$$
T_n(a) = f(a) + \frac{f'(a)}{1!} (x - a) + \frac{f''(a)}{2!} (x - a)^2 + \dots + \frac{f^{(n)}(a)}{n!} (x - a)^n
$$

Многочлен Тейлора функции $f$ в точки $a$ порядка $n$

**Утверждение**
$$
T_n(a) = f(a), T_n'(a) = f'(a), \dots, T_n^{(n)}(a) = f^{(n)}(a)
$$

**Доказательство** $0 \le m \le n \quad T_n^{(m)}(a) = f^{(m)}(a)$

$k < m \quad \left(\frac{f^{(m)}(a)}{k!}(x - a)^k\right)'_m \equiv 0$

$k = m \quad \left(\frac{f^{(n)}(a)}{k!} (x - a)^k\right)'_m = f^{(m)}(a)$

$k > m \quad \left(\frac{f^{(m)}(a)}{k!}(x - a)^m\right)'_m = \frac{f^{(m)}(a)}{k!} k (k-1)\dots(k - m + 1)(x-a) = 0$ при $x = a$

---

$R_n(x) = f(x) - T_n(x)$ - остаточный член порядка $n$

$\boxed{R_n(a) = R'_n(a) = \dots = R_n^{(n)}(a) = 0}$

$f(x) = T_n(x) + R_n(x)$

**Теорема** $f(x)$ имеют в т. $a$ производную порядка $k$, тогда

$$
f(x) = f(a) + \frac{f'(a)}{1!} (x - a) + \dots + \frac{f^{n}(a)}{n!}(x - a)^n + o((x - a )^n)
$$
(Локальная формула Тейлора)

**Доказательство** применим правило Лопиталя $(n - 1)$ раз

$\underset{x \to a}{\lim} \frac{R_n(x)}{(x - a)^n} = \underset{x \to a}{\lim} \frac{R'_n(x)}{n(x - a)^{n-1}} = \dots = \underset{x \to a}{\lim} \frac{R^{n-1}}{n(x-a)} {}$

## Асимптотика представления основных элементарных функций

> Всюду $\boxed{x \to 0} {}$

1. $f(x) = e^x, f^{(k)}(x) = e^x; f^{(k)}(0) = 1, k = 0, 1, 2, \dots \\
e^x = 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots + \frac{x^n}{n!} + o(x^n)$

2. $f(x) = \ln(1 + x); f(0) = 0, (\ln(1 + x))^{(k)} = \frac{(-1)^{k-1}(k - 1)!}{(1 + x)^n}; f^{(k)}(0) = (-1)^{k-1} (k-1)!, k=1,2,\dots\\
\frac{f^{(n)}(0)}{k!} = \frac{(-1)^{k-1}!}{k!} = \frac{(-1)^{k-1}}{k} \\
\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \dots + (-1)^{n-1} \frac{x^n}{n} o(x^n)$

3. $f(x) = (1 + x)^\alpha; f(0) = 1, ((1 + x)^\alpha)^{(n)} = \alpha (\alpha - 1)\dots(\alpha - k + 1)(1 + x)^{\alpha - k} \\
f^{(n)}(0) = \alpha(\alpha - 1) \dots (\alpha - k + 1), k = 1,2,\dots \\
(1 + x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha - 1)}{2!} x^2 + \frac{\alpha (\alpha - 1)(\alpha - 2)}{3!} x^3 + \dots + \frac{\alpha(\alpha - 1)\dots(\alpha - n + 1)}{n!} x^n + o(x^n)$
