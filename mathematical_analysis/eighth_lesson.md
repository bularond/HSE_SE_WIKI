---
title: 08. Свойства функций, непрерывных на отрезке
description: 
published: 1
date: 2020-12-23T10:02:12.664Z
tags: 
editor: undefined
dateCreated: 2020-11-03T13:13:06.678Z
---

# Свойства функций, непрерывных на отрезке

## Теорема: об обращении непрерывной функции в ноль

$f(x)$ непрерывна на отрезке $[a_1, b_1]; f(a_1) \cdot f(b_1) < 0$

Утв. $\exists c \in (a, b) \implies f(a) = 0$

Доказательство\
Пусть $f(a_1) < 0; f(b_1) > 0$\
$d_1 = \frac{a_1 + b_1}{2}$, если $f(\alpha_1) = 0$, то $c = d_1$\
если $f(d_1) \not= 0$ выберем из отрезков $[a_1, d_1], [d_1, b_1]$ тот, на концах которого $f(x)$ значения разных знаков\
это отрезок $[a_2, b_2]$\
Рассмотрим $d_2 = \frac{a_2 + b_2}{2};$ если $f(d_2) = 0$, то $c = d_2$,\
если $d_2 \not= 0$, то из отрозков $[a_2, d_2], [d_2, b_2]$ выбираем тот, на концах которого $f(x)$ принимает значения разных знаков\
это отрезок $[a_3, b_3]$\
Продолжим процесс построения отрезков \
Если $\exists n: f(dn) = 0$, что $c=dn$\
Если $f(d_n) \pm 0, n = 1, 2, \dots$\
$(a_1 \le a_2 \le \dots a_n \le \dots) \le (\dots \le b_n \le \dots \le b_2 \le b_1)$\
$\exists \underset{n\to\infin}{\lim} f(a_n) = f(\underset{n\to\infin}{\lim} a_n) \le 0$\
$\exists \underset{n\to\infin}{\lim} f(b_n) = f(\underset{n\to\infin}{\lim} b_n) \ge 0;$\
$b_n - a_n = \frac{b_1 - a_1}{2^{n-1}} \underset{n\to\infin}{\longrightarrow} 0$\
$\underset{n\to\infin}{\lim} a_n = \underset{n\to\infin} b_n = c$\
$f(c) \le 0; f(c) \ge 0 \implies f(c) = 0$

### Теорема: Коши о промежуточных значениях непрерывных функций

$f(x)$ непрерывна на $[a, b]; f(a) = A, f(b) = B$

Утверждение $\forall C$ между $A$ и $B \quad \exists c \in [a, b] \implies f(c) = C$

Доказательство:\
пусть $A > b; g(x) = f(x) - C$\
$
\left.
    \begin{array}{l}
        g(a) = A - C > 0 \\
        g(b) = B - C < 0
    \end{array}
\right\} \exists c \in (a, b) g(c)= 0$\
$f(c) - C = 0$\
$f(c) = C$

### Утверждение: Многочлен нечетной степени имеет корни

$
x^{2k+1} + a_{2k} x^{2k} + \dots + a_0 = 0 \\
f(x) = x^{2k+1} + a_{2k}x^{2k} + \dots + a_0 = x^{2k+1}(1+ \frac{a_{2k}}{x} + \dots + \frac{a_0}{x^{2k+1}}) \\
\underset{x\to+\infin}{\lim} f(x) = +\infin; \underset{x\to-\infin}{\lim} f(x) = -\infin \\
\exists \alpha, \beta \quad \alpha < \beta: f(\alpha) < 0; f(\beta) > 0 \\
\implies \exists c \in (\alpha, \beta) \implies f(c) = 0
$

## Теорема Больцано
Всякая ограниченная последовательность содержит сходящуюся подпоследовательность

$$
\gamma_n = (-1)^{n} + \frac{1}{n}; x_{2k} = 1 + \frac{1}{2k} \underset{k\to\infin}{\longrightarrow} 1
$$

### I Теорема Вейерштрасса
Функция, непрерывная на отрезке, ограничена на этом отрезке

**Пример** $f(x) = \frac{1}{x}; x \in (0; 1) \quad f$ непрерывна на $(0; 1). f$ не является ограниченной на $(0; 1)$

Доказательство:\
Пусть непрерывная функция $f(x)$ не является ограниченной на $[a, b]$\
$\forall n \in \N \exists x_n \in [a, b] \implies |f(x_n)| \ge n$\
Пусть $x_{n_k}$ - сходящаяся подпоследовательсть $x_n$\
$\underset{n_k\to\infin}{\lim} x_{n_k} = x^* \in [a, b]$\
$\underset{n_k\to\infin}{\lim} f(x_{n_k}) = f(x^*)$\
т. к. $|f(x_{n_k})| \ge n_k, |f(x_{n_k})| \underset{n_k\to\infin}{\longrightarrow} +\infin$\
противоречие
