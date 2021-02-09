---
title: 12. Теоремы дифференциального исчесления
description: 
published: 1
date: 2021-02-09T19:41:00.861Z
tags: 
editor: markdown
dateCreated: 2020-12-01T11:50:53.501Z
---

# Производная произвольного порядка

1. $(x^\lambda)^{(n)} = \alpha (\alpha - 1) \cdot \dots \cdot (\alpha - n + 1) x^{\alpha - n}; x > 0$
2. $\left(\frac{1}{x}\right)^{(n)} = \frac{(-1)^n n!}{x^{n+1}}$ 
3. $(\ln x)^{(n)} = \frac{(-1)^{n-1} (n - 1)}{x^n} {}$
4. $(\sin{x})^{(n)} = \sin{(x + n \frac{\pi}{2})}$
5. $(\cos{x})^{(n)} = \cos{(x + n \frac{\pi}{2})}$

## Формула Лейбница

$(f(x) g(x))^{(n)} = \sum_{k=0}^{n} C_n^k f^{(k)}(x)g^{(n-k)}(x) = \sum_{k=0}^{n} C_n^k g^{(k)}(x)f^{(n-k)}(x)$

**Доказательство индукцией**

$(fg)^{(n+1)} = ((fg)^{(n)})' = (\sum_{k=0}^{n} C_n^k f^{(k)} g^{(n-k)})' = \\ 
= \sum_{k=0}^n C_n^k f^{(k+1)} g^{(n - k)} + \sum_{k=0}^{n} C_n^k f^{(k)} g^{(n - k + 1)} = \\
= \sum_{m=1}^{n+1} C_n^{m-1} f^{(m)} g^{(n - m + 1)} + \sum_{m=0}^{n} C_n^m f^{(m)} g^{(n - m + 1)} = \\
= f^{(n + 1)} g^{(0)} + \sum_{m=1}^n (C_n^{m-1} + C_n^m) f^{(m)} g^{(n - m + 1)} + f^{(0)} g^{(n + 1)} = \\
= \sum_{m=0}^{n+1} C_{n + 1}^m f^{m} g^{n - m + 1} {}$

# Основные теоремы дифференциального исчисления

$x \in O_h(x_0), f(x); x_0 - \text{locmin}(\text{locmax})$ если $\exists \delta > 0 \forall x \in O_\delta (x_0) \implies (f(x) \geq f(x_0)) \text{ или, для locmax, }(f(x) \leq f(x_0))$

$x_0$ - точка $\text{locmin}$ или $\text{locmax}$, то $x_0$ точка $\text{locextr}$. 

## Теорема Ферма (необходимое условие экстремума)
Если $x_0 - \text{locextr}$ функции $f$ и $\exists f'(x_0)$, то $f'(x_0) = 0$

**Доказательство** Пусть $f'(x_0) \not= 0$, тогда $|f'(x_0)| > 0$

Пусть $x_0 - \text{locmin}$.

$f(x_0 + \Delta x) - f(x_0) = f'(x_0) \cdot \Delta x + \bar {o}(\Delta x) = f'(x_0) \cdot \Delta x + \alpha (\Delta x) \cdot \Delta x; \alpha (\Delta x) \xrightarrow[\Delta x \to 0]{} 0$

$f(x_0 + \Delta x) - f(x_0) = \Delta x [f'(x_0) + \alpha(\Delta x)]$

для $\varepsilon = |f'(x_0)| > 0 \quad\exists \delta_1 (0 < \delta_1 < \delta) \forall \Delta x: |\Delta x| < \delta_1 \implies |\alpha(\Delta x)| < |f'(x_0)| {}$

Следовательно, если $|\Delta x| < \delta_1, f'(x_0) + \alpha(\Delta x)$ имеет тот же знак, что $f'(x_0)$

Следовательно $f(x_0 + \Delta x) - f(x_0) = \Delta x [f'(x_0) + \alpha(\Delta x)]$ меняет значение в $O_{\delta_1}(x_0)$

Но $x_0 - \text{locmin} \implies f(x_0 + \Delta x) - f(x_0) \ge 0$ противоречие

## Теорема Ролля
Имеем $f(x)$

1. $f(x)$ непрерывна на отрезке $[a, b]$
2. $f(x)$ дифференцируема в интервале $(a, b)$
3. $f(a) = f(b)$

**Утверждение** $\exists c \in (a, b) \implies f'(c) = 0$

**Доказательство**

Из 2 Теоремы Вейерштрасса

$\exists x_{\min}, x_{\max} \in [a, b]$

$f(x_{\min}) = m, f(x_{\max}) = M, m \le M$

Если $m = M \implies f(x) = const, c$ - любая точка $\in(a, b)$

Если $m < M$, то хотя бы одна из точек $x_{\min}, x_{\max}$ не совпадает с концами отрезков. 

Тогда эта точка есть точка $c$, т. к. она $\in(a, b)$ и по теореме Ферма $f'(x) = 0$

## Теорема Коши
$f(x), g(x)$

1. $f$ и $g$ непрерывны на отрезке $[a, b]$
2. $f$ и $g$ дифференцируемы в интервале $(a, b)$
3. $g'(x) \not= 0, x \in a, b$

**Утверждение** $\exists c \in (a, b) \implies \frac{f(b) - f(a)}{g(b) - g(a)} = \frac{f'(c)}{g'(c)}$.

Замечание $g(b) - g(a) \not=0$ в силу теоремы Ролля

**Доказательство**

$\varphi(x) = f(x) - f(a) - \frac{f(b) - f(a)}{g(b) - g(a)}(g(x) - g(a))$

$\left.
\begin{array}{r}
\varphi(x) \text{ непрерывна на } [a, b] \\
\varphi(x) \text{ дифференцируема в } (a, b) \\
\varphi(a) = 0; \varphi(b) = 0
\end{array}
\right\}$ для $\varphi$ выполнено условие т. Ролля

$\exists c \in (a, b) \implies \varphi'(c) = 0$

$\varphi'(x) = f'(x) - \frac{f(b) - f(a)}{g(b) - g(a)} \cdot g'(x)$

$0 = \varphi'(c) = f'(c) - \frac{f(b) - f(a)}{g(b) - g(a)} g'(c)$, т. к. $g'(c) \not= 0 \implies \frac{f(b) - f(a)}{g(b) - g(a)} = \frac{f'(c)}{g'(c)} {}$

## Теорема Лагранжа (о конечном приращении)

Имеем $f(x)$
1. $f$ непрерываная на $[a, b]$
2. $f$ дифференцириуема в $(a, b)$

**Утвержение** $\exists c \in (a, b) \implies \frac{f(b) - f(a)}{b - a} = f'(c)$

**Доказательство**

Следует из теоремы Коши, если положить $g(x) = x$
