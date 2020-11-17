---
title: 3. Бесконечно большие и малые последовательности
description: 
published: 1
date: 2020-09-22T13:13:48.342Z
tags: 
editor: undefined
dateCreated: 2020-09-22T11:24:10.762Z
---

> 22 сентября 2020
# Бесконечно малые (Б.М.) числове последовательности
$x_n$ - б. м. последовательность, если $\underset{n\to\infin}{\lim} x_n = 0$

**Утверждение 5**
1. $\{x_n\}, \{y_n\}$ - б.м. посл $\implies \{x_n \pm y_n\}$ - б. м.
1. $\{x_n\}$ - б.м. $, \{y_n\}$ - ограниченная $\implies \{x_n \cdot y_n\}$ - б. м.

**Доказательство**\
1. 
$$
\Epsilon > 0 \exist N_1 \forall n \ge N_1 \implies |x_n| < \Epsilon / 2 \\
\exist N_2 \forall n \ge N_2 \implies |y_n| < \Epsilon / 2 \\
N = max(N_1, N_2) \implies |x_n \pm y_n| \le |x_n| + |y_n| < \Epsilon / 2 + \Epsilon / 2 = \Epsilon
$$

2. 
$$
|y_n| < M (M > 0) \\
\Epsilon > 0 \exist N \forall n \ge N \implies |x_n| < \Epsilon / M \\
|x_n \cdot y_n| \le |x_n| \cdot |y_n| < \Epsilon / M \cdot M = \Epsilon
$$

**Пример**
$$
\lim_{n\to\infin} \frac{n^k}{a^n} (a > 1; k - \text{фиксированное число}) \\
\frac{n^k}{a^n} = \left(\frac{n}{(\sqrt[k]{a})^n}\right)^k; 
\sqrt[k]{a} > 1; \frac{n}{(\sqrt[k]{a})^n} \xrightarrow[n\to\infin]{} 0 \implies 
\left(\frac{n}{(\sqrt[k]{a})^n}\right)^k \xrightarrow[n\to\infin]{} 0
$$

## Арифметические операции над сходящимися последовательностями
**Утверждение 6**\
Если $\underset{n\to\infin}{\lim}x_n = a; \underset{n\to\infin}{\lim}y_n = b$, то
1. $\underset{n\to\infin}{\lim}(x_n \pm y_n) = a \pm b$
2. $\underset{n\to\infin}{\lim}(x_n \cdot y_n) = a \cdot b$
3. $\underset{n\to\infin}{\lim}(\frac{x_n}{y_n}) = \frac{a}{b}; y_n \not = 0, b \not = 0$

---

$$
\lim_{n\to\infin} x_n = a \iff \lim_{n\to\infin}(x_n - a) = 0, \text{т. е. } (x_n - a) - 
\text{б.м. последовательность} \\
x_n - a = \alpha_n; x_n = a + \alpha_n
$$

---

**Доказательство 1**
$$
\begin{rcases}
x_n = a + \alpha_n, \alpha_n - \text{б.м.} \\
y_n = b + \beta_n, \beta_n - \text{б.м.}
\end{rcases}
x_n + y_n = (a + b) + (\alpha_n + \beta_n); \text{т.е. } x_n + y_n \xrightarrow[n\to\infin]{}
a + b
$$

2. 
$$
x_n \cdot y_n = (a + \alpha_n) (b + \beta_n) = (a \cdot b) + a \beta_n + b \alpha_n + \beta_n \alpha_n , \text{ т.е. }
x_n\cdot y_n \xrightarrow[n\to\infin]{} a\cdot b
$$

3. \
a)\
Если $y_n \not = 0; b \not = 0$, то послед $\frac{1}{y_n}$ ограничена
$$
b \not = 0; \frac{|b|}{2} > 0 \exist N \forall n \ge N \implies ||b| - |y_n|| \le |b - y_n| <
\frac{|b|}{2}; ||\alpha| - |\beta|| \le |\alpha - \beta| \\
|b| - |y_n| < \frac{|b|}{2} \implies \frac{|b|}{2} < |y_n|, \frac{2}{|b|} > \frac{1}{|y_n|}\\
M = max(\frac{1}{|y_1|}, \frac{1}{|y_2|}, \dots, \frac{1}{|y_{n-1}|}, \frac{2}{|b|}) \\
\text{следовательно } \forall y_n \implies \left|\frac{1}{y_n}\right| \le M
$$

б)
$$
\frac{1}{y_n} \xrightarrow[n\to\infin]{} \frac{1}{b} \\
\left|\frac{1}{y_n} - \frac{1}{b} \right| = \frac{1}{|b||y_n|} |y_n - b| 
\xrightarrow[n\to\infin]{} 0
$$

в)
$$
\lim_{n\to\infin} \frac{x_n}{y_n} = \lim_{n\to\infin} x_n \cdot \frac{1}{y_n} =
\lim_{n\to\infin} x_n \cdot \lim_{n\to\infin} \frac{1}{y_n} = a \cdot \frac{1}{b} = \frac{a}{b}
$$

# Бесконечно большие (б.б.) последовательности 
$$
x_n = (-1)^n \cdot n; x_1 = -1, x_2 = 2, x_3 = -3, x_4 = 4, \dots
$$

**Определение**
$$
\lim_{n\to\infin} x_n = \infin (x_n \text{- б.б. последовательность}), \text{ если }
\forall \sigma > 0 \exist N \forall n \ge N \implies |x_n| > \sigma \\
\sigma > 0; O_\sigma (\infin) = \{x | |x| > \sigma \} = (-\infin; -\sigma) \cup
(\sigma; +\infin) \\
\forall \sigma > 0 \exist N \forall n \ge N \implies x_n \in O_\sigma(\infin)
$$

---

**Утверждение 7** (о связи б.б. и б.м. последовательностей)
1. $x_n$ - б.б., $x_n \not = 0 \implies \frac{1}{x_n}$ - б.м.
1. $x_n$ - б.м., $x_n \not = 0 \implies \frac{1}{x_n}$ - б.б.

---

$$
x_n = \frac{1}{n} \text{б.м.} \quad \frac{1}{x_n} = n \text{- б.б.}
$$

**Доказательство**
$$
1. \Epsilon > 0; \sigma = \frac{1}{\Epsilon} > 0 \quad \exist N \forall n \ge N \implies
|x_n| > \sigma = \frac{1}{\Epsilon} \implies \frac{1}{|x_n|} < \frac{1}{\sigma} = \Epsilon
$$
$$
2. \sigma > 0; \Epsilon = \frac{1}{\sigma} > 0 \quad \exist N \forall n \ge N \implies 
|x_n| < \Epsilon = \frac{1}{\sigma} \implies \frac{1}{|x_n|} > \frac{1}{\Epsilon} = \sigma
$$

---

Последовательность 
$x_1 < x_2 < \dots < x_n < \dots$ т.е. $x_n < x_{n+1} (n=1,2, \dots)$ - возрастет\
$x_1 \le x_2 \le \dots \le x_n \le \dots$ т.е. $x_n \le x_{n+1} (n=1, 2, \dots)$ - не убывает\
$x_1 > x_2 > \dots > x_n > \dots$ т.е. $x_n > x_{n+1} (n=1,2, \dots)$ - убывает
$x_1 \ge x_2 \ge \dots \ge x_n \ge \dots$ т.е. $x_n \ge x_{n+1} (n=1,2, \dots)$ - не возрастает

**Теорема**\
Если последовательность $\{x_n\}$ не убывает и ограничена сверху, то она сходится

**Теорема**\
Последовательность $x_n = (1 + \frac{1}{n})^n$ сходится\
Ее предел обозначается $e$; число Эйлера (Euler);\
$e \approx 2,7182818$

$$
C_n^k = \frac{n!}{k!(n-k)!} = \frac{n(n-1)(n-2)\dots(n-k+1)}{k!}\\
$$

1. Последовательность $x_n$ ограничена сверху
$$
x_n = (1 + \frac{1}{n})^n = 1 + \sum_{k=1}^{n} \frac{n(n-1)(n-2)\dots(n-k+1)}{k!} \cdot
\frac{1}{n^k} = \\
= 1 + \sum_{k=1}^{n} (1-\frac{1}{n})(1 - \frac{2}{n})\dots(1 - \frac{k-1}{n}) \frac{1}{k!} < \\
< 1 + \sum_{k=1}^{n} \frac{1}{k!} < 1 + 1 + \frac{1}{2} + \frac{1}{2^2} + \dots + 
\frac{1}{2^{k-1}} = 1 + \frac{1 - (\frac{1}{2})^k}{1 - \frac{1}{2}} < 1 + \frac{1}{1/2} = 3
$$
$$
k! = 1 \cdot 2 \cdot 3 \dots k \\
2^{k-1} = 2 \cdot 2 \dots 2 \\
2^{k-1} < k! \\
\frac{1}{2^{k-1}} > \frac{1}{k!}
$$
