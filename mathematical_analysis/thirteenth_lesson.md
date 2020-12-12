---
title: 13. Правила Лопиталя.
description: 
published: 1
date: 2020-12-12T12:45:33.904Z
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

**Дополнение**
$f(x), g(x)$
1. $f, g$ непрерывны на $[a;+\infty)$, $a>0$
2. $f', g'$ существуют на $(a;+\infty)$
3. $g'(x)\not = 0$, $x\in(a;+\infty)$
4. $\underset{x\to+\infty}{\lim} f(x) = \underset{x\to+\infty}{\lim} g(x) = 0$

Если $\underset{x\to+\infty}{\lim} \frac{f'(x)}{g'(x)} = A$, то $\underset{x\to+\infty}{\lim} \frac{f(x)}{g(x)} = A$ ($A$ - число или $\pm\infty$)

**Доказательство**

$y = \frac{1}{x}$, $y\in(0;\frac{1}{a})$
$\underset{x\to+\infty}{\lim} f(x) = \underset{y\to+0}{\lim} f(\frac{1}{y}) = 0$
Аналогично $\underset{y\to+0}{\lim} g(\frac{1}{y}) = 0$

$f(\frac{1}{y}), g(\frac{1}{y})$ дифференцируемы, когда $y\in (0;\frac{1}{a})$
$\big(g(\frac{1}{y})\big)'_y = g'_y(\frac{1}{y})\cdot (-\frac{1}{y^2})$
$\begin{cases}
g'_y(\frac{1}{y}) \not =0 \\
(-\frac{1}{y^2}) \not =0
\end{cases} \Rightarrow
g'_y(\frac{1}{y})\cdot (-\frac{1}{y^2}) \not=0
$

$\underset{x\to+\infty}{\lim} \frac{f(x)}{g(x)} = \underset{y\to+0}{\lim} \frac{f(\frac{1}{y})}{g(\frac{1}{y})} = \underset{y\to+0}{\lim} \frac{f'_x(\frac{1}{y})\cdot(-\frac{1}{y^2})} {g'_x(\frac{1}{y})\cdot(-\frac{1}{y^2})} = \underset{y\to+0}{\lim} \frac{f'_x(\frac{1}{y})} {g'_x(\frac{1}{y})} = \underset{x\to+\infty}{\lim} \frac{f'_x(x)}{g'_x(x)} \Rightarrow$

$\underset{x\to+\infty}{\lim} \frac{f(x)}{g(x)} = \underset{x\to+\infty}{\lim} \frac{f'_x(x)}{g'_x(x)}\thinspace$


<div class="sorry" style="
   padding: 30px 0;
  	width:100%;
    display:flex;
    justify-content:space-evenly;
    align-items:center;
    font-size:2em;">
  <img src="https://cdn.betterttv.net/emote/5fb274372d853564472d95e6/3x">
  <div style="text-align:center;">Может быть допишу до конца</div>
  <img src="https://cdn.betterttv.net/emote/5fb274372d853564472d95e6/3x">
</div>
<br>