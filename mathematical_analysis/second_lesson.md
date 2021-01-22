---
title: 02. Числовые последовательности
description: 
published: 1
date: 2021-01-14T10:21:08.124Z
tags: 
editor: undefined
dateCreated: 2020-09-15T12:07:27.085Z
---

> 15 сентября 2020


# Числовые последовательности
Если каждому натуральному числу поставлено в соответствие вещественное число $x_n$, 
то заданна числовая последовательность

Способы задания:
1. С помощью формулы; $x_n = n^2 + 1$; $x_1 = 2, x_2 = 5, x_3 = 10, \dots$
2. С помощью рекуррентной формулы (рекуррентного соотношения); 
$$
\text{Последовательность Фибоначчи} \\
x_1=1, x_2 = 1; x_n = x_{n-1} + x_{n-2}, n \ge 3 \\
x_3 = 2, x_4 = 3, x_5 = 5, \dots 
$$
3. Описание членов последовательности.
$x_n$ - $n$-ое простое число
$$
x_1 = 2, x_2 = 3, x_3 = 5, x_4 = 7, x_5 = 11, \dots
$$

## Пределы числовой последовательности
$$
x_n = \frac{1}{n}; x_2 = \frac{1}{2}, x_3 = \frac{1}{3}, \dots \\
\lim_{n\to \infin} x_n = 0
$$

**Опр.** $\underset{n\to\infin}{\lim} x_n = a \quad (x_n \xrightarrow[n\to\infin]{} a)$ если для всякого $\varepsilon > 0$, начиная с некоторого номера N (зависимого от $\varepsilon$) все члены последовательности удовлетворяют: $|x_n - a| < \varepsilon$

$$
\forall \varepsilon > 0 \exist N = N(\varepsilon) \space \forall n \ge N \implies |x_n - a| < \varepsilon
$$

> $\forall x$ - для всех x, для любого x; $\forall$ - квантор общности (All)
> 
> $\exist x$ - найдется x, существует x; $\exist$ - квантор существования (Exist)
> 
> $A \implies B$ - из утверждения A следует B; если А, то B ($\implies$ импликация)
> 
> $A \iff B$ - утверждение А равносильно утверждению В ($\iff$ эквивалентность)
{.is-info}

---

$$
x_n = \frac{1}{n}; \varepsilon = \frac{1}{1000}; |x_n - 0| < \frac{1}{1000}; N = 1000; N = 1001 \\
\varepsilon > 0 \quad |x_n - 0| < \varepsilon \quad N = \left[\frac{1}{\varepsilon}\right] + 1
$$

---

$a$ - вещественное число, $\varepsilon > 0$
$O_\varepsilon (a)$ - $\varepsilon$ окрестность точки $a$

$$
O_\varepsilon (a) = \{x \in \R | a - \varepsilon < x < a + \varepsilon \} \quad |x - a| < \varepsilon
$$

![ma15.09.20_01.png](/ma15.09.20_01.png)

$$
\lim_{n\to\infin} x_n = a \iff \forall \varepsilon > 0 \exist N \forall n \ge N \implies x_n \in O_\varepsilon (a)
$$

**Утв 1** $\underset{n\to\infin}{\lim} x_n = a \iff$ вне всякой окрестности точки а имеется конечное множество членов последовательности

$(\implies)$ Дано $\lim_{n\to\infin} x_n = a$
Рассмотрим $O_\varepsilon (a); \exist N \forall n \ge N \implies x_n \in O_\varepsilon (a)$
только лишь $x_1, x_2, \dots, x_{N-1}$ могуть попасть $O_\varepsilon(a)$

$(\impliedby)$ пусть $\varepsilon > 0$. Рассмотрим $O_\varepsilon(a)$; пусть $x_{n1}, x_{n2}, \dots, x_{nk}$ не принадлежат $O_\varepsilon(a)$
$N = max(n{1}, \dots, n_k) + 1$ таким образом $\forall n \ge N \implies x_n \in O_\varepsilon(a)$ т. е.
$\underset{n\to\infin}{\lim} x_n = a$

> Пример $1, \frac12, 1, \frac14, \dots, 1, \frac1n, 1 , \dots$
> У данной последовательности нет предела
> 
> ![ma15.09.20_02.png](/ma15.09.20_02.png)
> 
---

**Утв 2** (о единственности предела)
Сходящаяся последовательность имеет единственный предел.

**Доказательство** (от противного)
пусть $\underset{n\to\infin}{\lim} x_n = a_1; \underset{n\to\infin}{\lim} x_n = a_2, a_1 < a_2$

$$
\varepsilon = \frac{a_2 - a_1}{3} > 0
$$

![ma15.09.20_03.png](/ma15.09.20_03.png)

$$
\exist N_1 \forall n \ge N_1 \implies x_n \in O_\varepsilon (a_1) \\
\exist N_2 \forall n \ge N_2 \implies x_n \in O_\varepsilon (a_2)
$$

Пусть $N=max(N_1, N_2)$; если $n \ge N$, то $x_n \in O_\varepsilon (a1), x_n \in O_\varepsilon (a_2)$

противоречие, т.к. $O_\varepsilon (a1) \cap O_\varepsilon (a_2) = \varnothing$

---

Последовательность $\{x_n\}$ ограничена, если $\exist M, m$ такие, что $m \le x_n \le M$ для всех $n$
$M$ ограничивает $\{x_n\}$ сверху, а $m$ снизу

**Утв 3** 
Сходящаяся последовательность ограничена

**Доказательство** $\underset{n\to\infin}{\lim} x_n = a;$ 
для $\Epsilon = 1 \quad \exist N \forall n \ge N \implies |x_n - a| < 1$
т.е. $x_n < a + 1$
$M = max(a+1, |x_1|, |x_2|, \dots, |x_{N-1}|)$
тогда $\forall n \implies x_n \le M$

Для $m$ аналогично

---

**Утв 4** (теорема о зажатой последовательности)
$$
\lim_{n\to\infin} x_n = \lim_{n\to\infin} z_n = a \\
\{y_n\}: x_n \le y_n \le z_n \space (n=1, 2, \dots) \\
\text{Утв. } \lim_{n\to\infin} y_n = a
$$

![photo_2020-09-15_15-05-05.jpg](/photo_2020-09-15_15-05-05.jpg)

**Доказательство** 
$$
\varepsilon > 0 \quad \exist N_1 \forall n \ge N_1 \implies x_n \in O_\varepsilon(a) \\
\exist N_2 \forall n\ge N_2 \implies z_n \in O_\varepsilon(a) \\
N = max(N_1, N_2) \quad \forall n \ge N \implies x_n, z_n \in O_\varepsilon(a) \implies \\
\implies y_n \in O_\varepsilon(a) \\
$$
> 
> Пример
> $$
> a > 1 \\
> \lim_{n\to\infin} \frac{n}{a^n} = 0 \\
> a = 1 + \beta; \beta > 0 \\
> 0 < \frac{n}{a^n} = \frac{n}{(1 + \beta)^n} = \frac{n}{1 + bn + \frac{n(n-1)}{2}\beta^2 +\dots} 
> \le \frac{n}{\frac{n(n-1)}{2}\beta^2} = \frac{2}{\beta^2 (n - 1)} \xrightarrow[n\to\infin]{} 0
> $$
> 
> $$
> \begin{gathered}
>   x_n = 0 \\
>   y_n = \frac{n}{a^n} \\
>   z_n = \frac{2}{\beta^2 (n - 1)}
> \end{gathered}
> $$

## Бесконечно малые (б.м.) последовательности
**Опр** $\{x_n\}$ б.м. последовательность, если $\underset{n\to\infin}{\lim} x_n = 0$

Пример $\underset{n\to\infin}{\lim} x_n = a \iff \underset{n\to\infin}{\lim}(x_n - a) = 0$, т.е. $(x_n - a)$ - б.м. последовательность

**Утв 5** (св-ва б.м. последовательности)
1. $\{x_n\}, \{y_n\}$ - б.м. $\implies$ $x_n \pm y_n$ - б.м. последовательность
2. $\{x_n\}$ - б.м. $\{y_n\}$ - ограниченная последовательность $\implies x_n \cdot y_n$ - б.м. последовательность
