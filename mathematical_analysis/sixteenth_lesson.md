---
title: 16. Неопределенный интеграл
description: 
published: 1
date: 2021-01-19T11:30:06.033Z
tags: 
editor: markdown
dateCreated: 2021-01-19T11:30:06.033Z
---

## Точка перегиба (графика функции)

$f(x); x \in [x_0 - h, x_0 + h]$

**Определение** Если $f$ выпукла на левом полуотрезке ($[x_0 - h, x_0]$) и вогнута на правом полуотрезке ($[x_0, x_0 + h]$) или наоборот, то $x_0$ - точка перегиба

**Теорема** Пусть $f''(x)$ непрерывна на $[x_0 - h, x_0 + h]$. Пусть $f''(x) > 0, x \in [x_0 - h, x_0)$ (1) и $f''(x) < 0, x \in (x_0, x_0 + h)$ (2) (вторая производная меняет знак в т. $x_0$). Утверждаем, что $x_0$ - это точка перегиба.

*Доказательство* (1) $\implies f(x)$ выпуклая функци $[x_0 - h, x_0)$. $\underset{x\to x_0-}{\lim} f''(x) = f''(x_0) \ge 0$

(2) $\implies f(x)$ вогнутая функция $x_0, x_0 + h$. $\underset{x \to x_0+}{\lim} f''(x) = f''(x_0) \le 0$

## Асимптоты

1. Вертикальные асимтоты. $x = x_0$ - вертикальная асмиптота или $\underset{x \to x_0+}{\lim} f(x) = \infin$ или $\underset{x \to x_0-}{\lim} f(x) = \infin$
2. Наклонные асимптоты. $f(x), x \in (a, +\infin)$. $y = kx + b$ - наклонная асимптота функции $y = f(x)$, если $\underset{x \to +\infin}{\lim} (f(x) - (kx + b)) = 0$

**Теорема** $y = kx + b$ асимптота графика функции $y = f(x)$ при $x \to +\infin \iff\\
\iff 
\begin{cases}
\underset{x \to +\infin}{\lim} \frac{f(x)}{x} = k (\in \R) (1) \\
\underset{x \to +\infin}{\lim} (f(x) - kx) = b (\in R) (2)
\end{cases}
$

*Доказательства* 

$\implies$ Дано: $\underset{x \to +\infin}{\lim} (f(x) - (kx + b)) = 0;\\
f(x) = kx + b + \alpha(x) \\
\frac{f(x)}{x} = k + \frac{b}{x} + \frac{1}{x} \cdot \alpha(x) \xrightarrow[x \to +\infin]{} k$ (1)

(2) $
\underset{x \to +\infin}{\lim} (f(x) - kx) = \underset{x \to \infin}{\lim} (f(x) - kx - b) + \underset{x \to \infin}{\lim} b = b
$

---

$\impliedby$ (2) $f(x) - kx = b + \beta(x), \beta(x) \xrightarrow[x \to +\infin] 0 \\
f(x) - kx - b = \beta(x) \xrightarrow[x\to\infin]{} 0; \underset{x\to\infin}{\lim} (f(x) - (kx + b)) = 0$

# Неопределенный интеграл

$F(x), f(x), \forall x \in (a, b) \implies F'(x) = f(x)$

$f(x)$ - производная функции $F(x)$

$F(x)$ - первообразная для $f(x)$

$(\sin x)' = \cos x$, $\cos x$ - производная $\sin x$, $\sin x$ - первообразная $\cos x$

**Лемма** Пусть $F_1(x), F_2(x)$ - первообразные для $f(x)$, на $(a, b)$. Тогда $F_2(x) = F_1(x) + \text{const}$

*Доказательство*

$
\begin{cases}
F_1'(x) = f(x) \\
F_2'(x) = f(x)
\end{cases}
$

$F_2'(x) - F_1'(x) = (F_2(x) - F_1(x))' = 0, x \in(a, b)$

$G(x) = F_2(x) - F_1(x); G'(x) = 0$

Пусть $x_1, x_2 \in (a, b)$: $G(x_2) - G(x_1) = G'(\xi)(x_2 - x_1) = 0 \implies G(x_1) = G(x_2), G(x) = \text{const}$

$F_2(x) = f_1(x) + \text{const}$

---

**Определение** Множество всех первообразных для $f(x)$ на $(a, b)$ над неопределенным интегралом функции $f$ на $(a, b)$

Обозначение: $\int f(x) dx$. Если $F(x)$ - первообразная для $f(x)$

$\int f(x)dx = \{\int F(x) + C | C \in \R\}$. Пишут $\int f(x)dx = F(x) + C$

$\int \cos x dx = \sin x + C$. $C$ - константа интегрированиы

## Свойства неопределенных интегралов

1. Линейность
    1. $\int \alpha f(x) dx = \alpha \int f(x)dx \quad \alpha \not= 0$
    2. $\int (f(x) + g(x))dx = \int f(x)dx + \int g(x)dx$
2. Формула интегрирования по частям

$f(x), g(x)$ непрерына дифференцируемо на $(a, b)$

$f(x) \cdot g(x))' = f'(x) \cdot g(x) + f(x) \cdot g'(x) \\
\int (f(x) \cdot g(x))' dx = f(x) \cdot (x) + C \\
f(x) \cdot g'(x) = (f(x) \cdot g(x))' - f'(x) \cdot g(x) \\
\int f(x) \cdot g'(x) = \int (f(x) \cdot g(x))' dx - \int f'(x) g(x) dx = \\
= f(x) \cdot (x) + C - \int f'(x) g(x) dx = f(x) g(x) - \int f'(x) g(x) dx$

$$
\boxed{\int f(x) g'(x) dx = f(x) g(x) - \int f'(x) g(x) dx}
$$

$
\int f(x) dg(x) = f(x) g(x) - \int g(x) df(x) \\
]int fdg = fg - \int gdf
$

$
x > 0; (\ln x)' = \frac{1}{x} \quad \int \frac{1}{x} dx = \ln x + C \\
\int \underbrace{\ln x}_f \underbrace{dx}_g = x \ln x - \int x d\ln x = x \ln x - \int x \cdot \frac{1}{x} dx = x \ln x - x + C
$

3. Замена переменной в неопределенном интеграле

$
y \in (a, b), F'(y) = f(y) \\
x \in (\alpha, \beta), y = y(x); y(x) \in (a, b), y'(x)$ непрерывна

$
F(y(x)), F_x' (y(x)) = F_y'(y(x)) \cdot y_x'(x) = f(y(x)) \cdot y_x' \\
\int f(y(x)) y_x'(x) dx = F(y(x)) + C \\
\int f(y) dy = F(y) + C \\
\boxed{\int f(y)dy = \int f(y(x)) y_x'dx}
$
