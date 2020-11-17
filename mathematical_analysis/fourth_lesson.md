---
title: 4. Пределы функций
description: 
published: 1
date: 2020-10-06T21:34:17.718Z
tags: 
editor: undefined
dateCreated: 2020-09-29T11:22:06.964Z
---

# #ямыбпи205

## Возвращаемся к вопросу предудущей лекции
1) Докажем, что {x~n~} ограничена сверху
$$
C_n^k = \frac{n!}{k!(n-k)!} = \frac{n(n-1)(n-2)\dots(n - k + 1)}{k!} \\
x_n = (1+\frac{1}{n})^n = \sum_{k=0}^n C_{n}^k \frac{1}{n^k} =\\
= 1 + \sum_{k=1}^n \frac{n(n-1)(n-2)\dots(n-k+1)}{k!} \frac{1}{n^k} =\\ = 1 + \sum_{k=1}^n (1 - \frac{1}{n})(1 - \frac{2}{n})\dots(1 - \frac{k+1}{n})\frac{1}{k!} \space(*) < \\
< 1 + (\frac{1}{1!} + \frac{1}{2!} + \frac{1}{3!} + \dots + \frac{1}{n!}) < \\
< 1 + 1 + \frac{1}{2} + \frac{1}{2^2} + \dots + \frac{1}{2^{k-1}} = \\
= 1 + \frac{1-(\frac{1}{2})^k}{1-\frac{1}{2}} < 1 + \frac{1}{\frac{1}{2}} = 3 \implies \\
\implies \forall x \space x_n \le 3
$$
2) Докажем, что {x~n~} возрастает

$$
x_n < x_{n+1} \quad ? \\
x_{n+1} = \left(1 + \frac{1}{n+1}\right)^{n+1} = \\
= 1 + \sum_{k=1}{n} \frac{(n+1)(n+1-1)(n+1-2)\dots(n+1-(k-1))}{k!} \cdot \frac{1}{(n+1)^k} + 
\frac{1}{(n+1)^{n+1}} = \\
= 1 + \sum_{k=1}^n \left(1 - \frac{1}{n+1}\right)\left(1 - \frac{2}{n+1}\right)\dots
\left(1 - \frac{k-1}{n+1}\right) \frac{1}{k!} + \frac{1}{(n+1)^{n+1}} (**) \\
\begin{cases}
1 - \frac{1}{n+1} > 1 - \frac{1}{n} \\
1 - \frac{2}{n+1} > 1 - \frac{2}{n} \\
\dots
\end{cases} \implies 
\text{Сумма } (**) > \text{Сумма } (*) \\
x_{n+1} > x_n
$$
$$
(1+x)^{n+1} = \sum_{k=0}^{n+1} C_{n+1}^k \cdot x^k = 1 + \sum_{k=1}^n C_{n+1}^k x^k +
C_{n+1}^{k+1} x^{n+1}
$$

## Предел функции
$$
f(x) = \frac{x^2 - 1}{x - 1} = \begin{cases}
x + 1, & x\not= 1 \\
\text{не определена} & x=1
\end{cases} \\
\lim_{x\to1} f(x) = 2
$$
$$
\varnothing \not= X \subset \R, a \in \R \\
$$
$a$ - предел точки последовательности $X$, если $\exists$ последовательность $x_n \in X (x_n + a)$ такая, что $x_n \xrightarrow[n\to\infin]{} a$

Пример $X = (0, 1)$
1) $a\in(0,1) \quad x_n = a \frac{a}{n+1} \implies a$ а предельная точка $X$
2) $a=0; x_n = \frac{1}{n+1}; \frac{1}{2}, \frac{1}{3}, \dots \to a$ - предельная точка (предельная точка может не принадлежать множеству)

$$
\exists \text{ Определение } \lim_{x\to a} f(x) = A (\text{определение по Гейне}) \\
0 \not= X \subset \R; f \text{ определена на } X, 0 - \text{ определяется } X \\
\lim_{x\to a} f(x) = A, \text{если для всякой последовательности } x_n \to 0, x_n \in X, x_n \not= a \not= f(x_n)\xrightarrow[n\to\infin]{} A
$$
$$
f(x) = \begin{cases}
1, & x \not=0 \\
5, & x = 0
\end{cases} \\
\lim_{x\to\infin} f(x) = 1
$$

$$
f(x) = sin\frac{1}{x}; x\not=0 \\
x_n = \frac{1}{2\pi n} \to 0 \\
f(x_n) = 0 \to 0 \\
x_n = \frac{1}{\frac{\pi}{2} + 2\pi n} \to 0 \\
f(x+1) = 1 \to 1 \\
1 \not= 0 \\
\lim_{x\to0} \sin\frac{1}{x} \text{ не существует} \\
\frac{1}{x_n} = \frac{1}{\left(\frac{1}{2\pi n}\right)} = 2\pi n
$$
![screenshot_2020-09-29_plot_sin(1_x)_from_-0_4_to_0_4_-_wolfram_alpha(1).png](/screenshot_2020-09-29_plot_sin(1_x)_from_-0_4_to_0_4_-_wolfram_alpha(1).png)

---
$$
\sigma > 0; O_\sigma (a) = \{x | abs(x-a) < \sigma\} \\
O_\sigma(a) = \{x | 0 < abs(x - a) < \sigma\} = (a - S, a) \cup (a, a + \sigma) \\
\text{II } \lim_{x\to a} f(x) = A \text{ по Коши} \\
\varnothing \not= X \subset \R, f \text{ определена } X, a \text{ - предельная точка множетсва } X \\
\lim_{x\to a}(x) = A \text{ если } \forall \Epsilon > 0 \exists \sigma > 0 \forall x
\in O_\sigma (a) \cap X \implies |f(x) - A| < \epsilon
$$
