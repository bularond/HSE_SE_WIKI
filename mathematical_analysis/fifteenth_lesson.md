---
title: 15. Исследование функций
description: 
published: 1
date: 2021-02-12T20:50:45.109Z
tags: 
editor: markdown
dateCreated: 2021-01-12T11:26:13.507Z
---

# Исследование функций

**Теорема 1** $f(x)$ дифференцируема $x \in (a, b)$, тогда

1. $f(x)$ не убывает $\iff f'(x) \ge 0, x \in (a, b)$
2. $f(x)$ не возрастает $\iff f'(x) \le 0, x \in (a, b)$

**Доказательство**

1. $\implies f(x)$ не убывает; $x_1 \in (a, b)$

если $x_2 > x_1 \quad f(x_2) - f(x_1) \ge 0$

если $x _2 < x_1 \quad \frac{f(x_2) - f(x_1) \ge 0}{ x_2 - x_1 < 0} \ge 0$

$\underset{x_2 \to x_1}{\lim} \frac{f(x_2) - f(x_1)}{x_2 - x_1} = f'(x_1) \ge 0$

$\impliedby$ пусть $f'(x) \ge 0 \quad x_1 < x_1$ по теореме лагранжа $f(x_2) - f(x_1) = f'(\xi)(x_2 - x_1); x_1 < \xi < x_2$

---

**Теорема 2** $f(x)$ дифференцируема в $(a, b)$

Утвержение:

1. Если $f'(x) > 0$, то $f(x)$ возрастает (строго)
2. Если $f'(x) < 0$, то $f(x)$ убывает

Достаточные условия монотонности функции

**Доказательсво**

1. $x_1 < x_2; f(x_2) - f(x_1) = f'(\xi)(x_2 - x_1) > 0; f(x_2) - f(x_1) > 0$

*Замечание* $f(x) = x^3$, функция возрастает $f'(0) = 0$

---

$f(x), x \in O_\sigma (x_0) \quad x_0$ - строкий локальный минимум если

$\exists \sigma > 0 \forall x \in O_\sigma (x_0) \implies f(x) > f(x_0)$

$x_0$ - строгий локальный максимум, если

$\forall \sigma > 0 \forall x \in O_\sigma (x_0) \implies f(x) < f(x_0)$

---

**Теорема 3** $f(x)$ дифференцируема на $(a, b), x_0 \in (a, b)$, если $\exists \sigma > 0$

1. $\left.\begin{matrix}
f'(x) < 0, x \in (x_0 - \sigma, x_0) \\
f'(x) > 0, x \in (x_0, x_0 + \sigma)
\end{matrix}\right\} \implies x_0$ - locmin

1. $\left.\begin{matrix}
f'(x) > 0, x \in (x_0 - \sigma, x_0) \\
f'(x) < 0, x \in (x_0, x_0 + \sigma)
\end{matrix}\right\} \implies x_0$ - locmax

**Доказательтво**
1. Если $x \in (x_0 - \sigma, x_0) \implies f(x) - f(x_0) = f'(\xi)(x - x_0) > 0, f(x) > f(x_0)$

Если $x \in (x_0, x + \sigma) \implies f(x) - f(x_0) = f'(\xi) (x - x_0) > 0, f(x) > f(x_0)$

---

**Теорема 4** (Достаточное условие экстремума)

Пусть $f'(x_0) = 0$; пусть существует $f''(x_0)'$

1. если $f''(x_0) > 0$, то $x_0$ - locmin
2. если $f''(x_0) < 0$, то $x_0$ - locmax

**Доказательство**

$f(x) = f(x_0) + f'(x_0) (x - x_0) + \frac{f''(x_0)}{2}(x - x_0)^2 + o((x - x_0)^2) = \\
= f(x_0) + \frac{f''(x_0)'}{2} (x - x_0)^2 + d(x - x_0) (x - x_0)^2 = \\
= f(x_0) + (x - x_0)^2 \left(\frac{f''(x_0)}{2} + \alpha(x - x_0)\right)$

пусть $f''(x_0) > 0$, \xi = \frac{f''(x_0)}{2} > 0 \exists \sigma > 0 \forall x \in O_\sigma (x_0) \implies |\alpha(x - x_0)| < \frac{f''(x_0)}{2}$

т. е. $\left[\frac{f''(x_0)}{2} + \alpha(x - x_0)\right] > 0$

$f(x) = f(x_0) + (x - x_0)^2 \left[\frac{f''(x_0)}{2} + \alpha(x - x_0)\right] > f(x_0) \quad f(x) > f(x_0)$

## Выпуклые и вогнутные функции

**Определение** Непрерывная на $[a, b]$ функции $f(x)$ выпуклая на $[a, b]$ (строго выпукла), если

$\forall x_1, x_2 \in [a, b] \implies f\left(\frac{x_1 + x_2}{2}\right) \ge \frac{f(x_1) + f(x_2)}{2} \left(f\left(\frac{x_1 + x_2}{2}\right) < \frac{f(x_1) + f(x_2)}{2}\right)$

Функция $f(x)$ вогнуто (строго вогнуто), если $-f(x)$ выпукла (строго выпукла)

---

**Теорема 5** Пусть $f'(x)$ и $f''(x)$ определена на $[a, b]$. ($f'(x), f''(x)$ определена $[a, b] \subset (\alpha, \beta)$)

**Утверждение** Если $f''(x) \ge 0$ на $[a, b]$, то $f(x)$ выпукла,

если $f''(x) \le 0$ на $[a, b]$, то $f(x)$ вогнута

**Доказательство** $a \le x_1 < x_2 \le b$

$$
\begin{array}{r r l}
& f(x_2) = & f(x_0) + f'(x_0) h + \frac{f''(\xi_2)}{2} h^2 \\
+ \\
& f(x_1) = & f(x_0) + f'(x_0) (-h) + \frac{f''(\xi_1)}{2} h^2 \\
\hline \\
& f(x_1) + f(x_2) = & f(x_0) + h^2 \left(\frac{f''(\xi_1)}{2} + \frac{f''(\xi_2)}{2}\right) \ge 2f(x_0)
\end{array}
$$

*Замечание* Если в условии теоремы $f''(x) > 0$, то $f(x)$ - строго выпукло
