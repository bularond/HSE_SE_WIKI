---
title: 6. Второй замечательный предел и непрерывные функции
description: 
published: 1
date: 2020-10-13T11:26:09.490Z
tags: 
editor: undefined
dateCreated: 2020-10-13T11:25:58.835Z
---

# Второй замечательный предел и непрерывные функции
## Второй замечательный предел

$$
\lim_{x\to\infin} \left(1 + \frac{1}{x}\right)^x = e \\
$$

---

$$
\left(1 + \frac{1}{x}\right)^x; x = -1 - y; \left(1 + \frac{1}{x}\right)^x = \left(1 + \frac{1}{y+1}\right)^{-1-y} \\ 
= \left(\frac{y}{y+1}\right)^{-1-y} = \left(1 + \frac{1}{y}\right)^y\left(1 + \frac{1}{y}\right) \\
1_n \longrightarrow \infin (n\to\infin); y_n = (-x_n - 1) \xrightarrow[x\to\infin]{} +\infin \implies \left(1 + \frac{1}{y_n}\right)^{y_n} \xrightarrow[n\to\infin]{} e \\
\text{т.е. } \left(1 + \frac{1}{y_n}\right) \xrightarrow{n\to\infin} 1, \lim_{n\to\infin} \left(1 + \frac{1}{x_n}\right)^x{n} = \lim_{n\to\infin} \left(1 + \frac{1}{y_n}\right)^{y_n} = e
$$

---

$$
\text{Теорема } y = f(x) \text{ определена } \mathring{O}_{\delta_1}(a); \lim_{x\to a} f(x) = b \\
z = g(y) \text{ определена } \mathring{O}_{\delta_2} (l); \lim_{y\to l} g(y) = A \\
\text{Если } \forall x \in \mathring{O}_{\delta_1}(a) \implies f(x) \in \mathring{O}_{\delta_1} b (f(x) \not= b) \\
\text{тогда } \lim_{x\to a} g(f(x)) = \lim_{y\to b} g(y) = A
$$

Доказательсво

$$
y(f(x)) \text{ опр } \mathring{O}_{\sigma_1} (a), \text{ пусть } x_n \in \mathring{O}_{\sigma_1}(a), x_n \longrightarrow a (n\to\infin) \\
y_n = f(x_n); f(x_n) \not= b; \lim_{n\to\infin} g (y_n) = A \\
\text{т.е }  \lim_{n\to\infin} g(f(x_n)) = \lim_{n\to\infin} g(y_n) = A
$$

Следствие

$$
\text{пусть } \alpha(x) \text{ б.м. } x \to a; \alpha(x) \not= 0, \text{ тогда } \lim_{x\to a}(1 + \alpha(x)) ^{\frac{1}{\alpha(a)}} = e \\
\text{Док. } \lim_{y\to\infin} \left(1 + \frac{1}{y}\right)^y = e; y = \frac{1}{\alpha(x)} \quad x\longrightarrow a \implies \frac{1}{\alpha(a)} \to \infin \\
e = \lim_{y\to\infin} \left(1 + \frac{1}{y}\right)^y = \lim_{x\to a} (1 + \alpha(x))^{\frac{1}{\alpha(x)}} \\
\boxed{\lim_{x\to0} (1 + x)^{\frac{1}{x}} = e}
$$

## Непрерывные функции

$$
f \text{ определена в } O_k(h); h > 0 \\
\text{Опр: } f \text{ непрер. в т. } a, \text{ если } \lim_{x\to a} f(x) = f(a) \\
\text{I (по Гейне) } f \text{ непрервывна в т. } a, \text{ если } \forall x_n \in O_h(a), x_n \xrightarrow[n\to\infin]{} a \implies f(x_n) \xrightarrow[n\to\infin]{} f(a) \\
\text{II (по Коши) } \forall \varepsilon > 0 \exists \delta > 0 \forall x \in O_\delta (a) \implies |f(x) - f(a)| < \varepsilon \\
f(x) \in O_\varepsilon (f(a)) \\
$$

---

$$
x - a = \Delta x \text{ приращение аргумента } \\
f(x \pm \Delta x) - f(a) = \Delta f \text{ приращение функции (отвечаюее приращение } \Delta x) \\
f \text{ неопр в т. } a \iff \lim_{\Delta x \to 0} \Delta f = 0 \\
\forall \varepsilon > 0 \exists \delta > 0 \forall \Delta x: |\Delta x| < \delta \implies |\Delta f(x)| < \varepsilon
$$

---

Пусть функция $f$ определена в $[a, a+h), h>0$. $f$ непрерывна в т. $a$ справа, если $\underset{x\to a+}{\lim} f(x) = f(a)$

$f$ определа $x \in (-a-h; a]$. $f$ неопределена в т. $a$ слева, если $\underset{x\to a-}{\lim} f(x) = f(a)$

Пример: $f(x) = [x]$ целая часть $x =$ наибольшее целое число, не превосходящее $x$

если $a \notin \Z; f(x)$ непрерывна в $a$

если $a \in \Z; f(x)$ непрерывна справа в т. $a$

## Свойства функций непрерывных в точке
$f$ определена $O_h (a), h > a$

1. (Локальня ограниченная) если $f$ непрервына в точке $a$, то $Пf$ ограничена в каждой окрестности точки $a

$$
\text{Доказательство } \varepsilon = 1 \exists \delta > 0 \forall x \in O_\delta(a) \implies |f(x) - f(a)| < 1 \\
f(a) - 1 < f(x) < f(a) + 1 \\
C = max(|f(a) - 1|, |f(a) + 1|) \\
\text{тогда } \forall x \in O_\delta(a) \implies |f(x)| \le C
$$

2. Теорема о сохранении знака

Если $f$ непрерывна в т. $a$ то $f(a) > 0$, то $\exists$ окрестность в т. $a$, в которой функций положительна

$$
\text{Док. } f(a) > 0; \varepsilon = \frac{f(a)}{2} > 0 \exists \delta > 0 \forall x \in O_\delta (a) \implies |f(x) - f(2)| < \frac{f(a)}{2} \\
0 < \frac{f(a)}{2} < f(x) < \frac{3}{2} f(a) \\
\text{пример } f(x) = \begin{cases}
1, & x = 0 \\
-1, & x \not= 0
\end{cases} \\
$$
