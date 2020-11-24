---
title: Дифференцирование функции заданой параметрически, заданой неявно
description: 
published: 1
date: 2020-11-24T11:25:38.671Z
tags: 
editor: markdown
dateCreated: 2020-11-24T11:25:38.671Z
---

# Техника дифференцирования

## Функции заданные параметрически

$t \in [a, b]; \begin{cases}
    x = x(t) \\
    y = y(t)
\end{cases} \\
x_t',y_t',x_t' = 0 \quad x(t)$ возрвстает (убывает)

$x(a) = A; x(b) = B$

На $[A, B]$ определена $t=t(x)$ - обратная функция

$y = y(t(x)), y_x' = y_t' \cdot t_x' = y_t'\cdot \frac{1}{x_t'} = \frac{y_t'}{x_t'}$

$t_0; x_0 = x(t_0) \quad y_x'(x_0) = \frac{y_t'(t_0)}{x_t'(t_0)}$

**Пример** Циклоид

$R$ - радиус окружности

$\begin{cases}
    x = Rt - R\cdot \sin{t} \\
    y = R - R \cdot cos{t}
\end{cases}$

$
y_x' = \frac{y_t'}{x_t'} = \frac{R \cdot \sin{t}}{R \cdot (1 - cos{t})} = \frac{\sin{t}}{1 - \cos{t}}
$

## Функции, заданные неявно

$F(x, y) = 0; y = y(x); y_x' = ? \\
F(x, y(x)) = 0 \\
(F(x, y(x)))_x' = 0 \implies y_x'$

**Пример**

$
x^3 + y^3 - 10xy = 0 \\
y = y(x) \quad 3x^2 + 3y^2 y_x' - 10y - 10xy_x' = 0 \\
3x^2 - 10y + y_x'(3y^2 - 10x) = 0 \quad y_x' = \frac{10 y - 3x^2}{3y^2 - 10x}
$

**Пример** Эллипс

$|F_1F_2| = 2c \quad 2a > 2c \quad |MF_1| |MF_2| = 2a$

$a^2 - c^2 = b^2$

$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$

$y - y_0 = y_x'(x_0)(x - x_0) \\
\frac{x}{a^2} + \frac{y \cdot y_x'}{b^2} = 0; y_x' (x_0) = \frac{b^2}{a^2} \frac{x_0}{y_0}; y-y_0 = -\frac{b^2}{a^2} \frac{x_0}{y_0} (x - x_0) \\
a^2 y_0 y - a^2 y_0^2 = -b^2x_0 x + b^2x_0^2; a^2y_0 y + b^2x_x = b^2x_0^2 + \frac{a^2y_0^2}{a^2b^2} \\
\frac{y_0 y}{b^2} + \frac{x_0x}{a^2} = \frac{x_0^2}{a^2} + \frac{}{}$

## Дифференциал функции (1й дифференциал)
$f$ диф в т. $x$ 

$f(x + \Delta x) = f(x) + f'(x) \cdot \Delta x + 0(\Delta x), \Delta x \to 0 \\
f(x + \delta x) \approx f(x) + f'(x) \Delta x \\
\Delta x = dx \quad \Delta f \approx f'(x) dx$

**Определение** $df = f'(x) dx$ - зависит от $x$ и $dx$

**Пример**

$\sqrt{0.9} \approx ? \quad f(x) = \sqrt{x} \\
x_0 = 1 \quad dx = \Delta x = 0.9 - 1 = -0.1 \\
f'(x) = \frac{1}{2\sqrt{x}}; f'(x_0) = \frac{1}{2} \\
\sqrt{0.9} \approx f(1) + \frac{1}{2} dx = 1 + \frac{1}{2} (-0.1) = 0.95$

---

$x$ - независимая переменная. $df = f'(x)dx$

Пусть $x = x(t) \quad f(x(t)): df = f_t'(x(t)) \cdot dt = f_x' \cdot x_t' \cdot dt = f_x' \cdot x$

Вид 1го дифференциала функции не зависит от того, зависима ии независима переменная $x$. Инвариантность формы 1го дифференциала

---

$y = y(x); y_x' \quad dy = y_x' \cdot dx \quad y_x' = \frac{dy}{dx} \\
y(x(t)); \frac{dy}{dx} = \frac{dy}{dx} \cdot \frac{dx}{dt} \\
y = y(x); x = x(y); \frac{dy}{dx} = \frac{1}{\frac{dx}{dy}} \\
x = x(t) \\
y = y(t) \quad \frac{d_y}{dx} = \frac{dy}{dt}/\frac{dx}{dt}$
