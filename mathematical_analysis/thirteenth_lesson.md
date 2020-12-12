---
title: 13. Правила Лопиталя.
description: 
published: 1
date: 2020-12-12T12:13:38.435Z
tags: 
editor: markdown
dateCreated: 2020-12-12T12:13:38.435Z
---

# Первое правило Лопиталя (Неопределенность вида $\frac{0}{0}\thinspace$)

Имеем:
$f(x), g(x)$
1. $f,g$ непрерывны на $x\in (a;b]$
2. $f,g$ дифференцируемы на $(a;b)$
3. $g'(x) \not = 0$, $x\in(a;b)$ 
4. $\underset{x\to a+}{\lim}f(x) = \underset{x\to a+}{\lim} g(x) = 0$

Если $\underset{x\to a+}{\lim} \frac{f'(x)}{g'(x)} = A$, то $\underset{x\to a+}{\lim} \frac{f(x)}{g(x)} = A$ ($A$ - число или $\pm\infty$)

**Доказательство**
Положим, что $f(a) = g(a) = 0$
Тогда $f(x), g(x)$ непрерывны на $[a;b]$
Выполняются условия теоремы Коши.

$\frac{f(x)}{g(x)} = \frac{f(x)-f(a)}{f(x)-g(a)} = \frac{f'(\phi(x))}{g'(\phi(x))} \Rightarrow \underset{x\to a+}{\lim} \frac{f'(\phi(x))}{g'(\phi(x))} = A = \underset{x\to a+}{\lim} \frac{f(x)}{g(x)} \thinspace$.

**Замечание**
1. Аналогичное утверждение справедливо для $x\in[b,a)$, $b<a$
То есть для $\underset{x\to a-}{\lim}\thinspace$
2. Аналогичное утверждение справедливо для $\underset{x\to a}{\lim}\thinspace$



<br><br><br><br><br>