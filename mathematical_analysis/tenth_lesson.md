---
title: 10. Дифференцирование
description: 
published: 1
date: 2020-11-25T17:49:25.812Z
tags: 
editor: markdown
dateCreated: 2020-11-17T11:48:30.450Z
---

## Дифференцирование

## Критерий дифференцируемости

**Теорема** Функция $f(x)$ дифиренцируема в т. $x \iff \Delta f = f(x + \Delta x) - f(x) = Ax + o(\Delta x), \Delta x \to 0$; $A$ независит от $\Delta x$

Доказательство достаточности

Пусть $
\underset{\Delta x \to 0}{\lim} \frac{\Delta f}{\Delta x} = f'(x) \iff \frac{\Delta f}{\Delta x} = f'(x) + \alpha(\Delta x) \xrightarrow[\Delta x \to 0]{} 0\\
\Delta f = f'(x) \Delta x + o(\Delta x), \Delta x \to 0 \text{ т. о } A = f'(x)
$

Доказательство необходимости

Пусть $
\Delta f = A\cdot \Delta x + o(\Delta x) \quad (\alpha(\Delta x) \xrightarrow[\Delta x \to 0]{} 0) \\
(\frac{\Delta f}{\Delta x} = A + \alpha (\Delta x) \xrightarrow[\Delta x \to 0]{} f'(x) = A)
$

**Следствие** Если функция $f$ непрерывна в т. $x$, то она непрерывна в этой точке

Доказательство $\Delta f = A \Delta x + o(\Delta x) \xrightarrow[\Delta x \to 0]{} 0, \Delta f \xrightarrow[\Delta x \to 0]{} 0 \iff f$ непрерывна в т. $x$

$\forall \varepsilon > 0 \Epsilon \sigma > 0 \forall \Delta x |x| < \sigma \implies |f(x + \Delta x) - f(x)| < \varepsilon$

Пример

$f(x) = |x|, x_0 = 0 \\
\frac{f(x) - f(0)}{x - 0} = \frac{|x|}{x} \xrightarrow[x\to0]{}$ нет предела

## Свойства операций дифференцирования

$f$ и $g$ дифференцируемы в т. $x$

1. Линейность $(af(x) + bg(x))' = af'(x) + bg'(x) \quad a, b \in \R$
2. Формула Лейбница: $(f(x)g(x))' = f'(x)g(x) + f(x)g'(x)$
3. $\left(\frac{f(x)}{g(x)}\right)' = \frac{f'(x)g(x) - f(x)g'(x)}{g^2(x)}, \quad g(x) \not= 0$

---

$\Delta f = f(x + \Delta x) - f(x); \Delta g = g(x + \Delta x) - g(x)$

1. $\Delta(af + bg) = a\Delta f + b \Delta g$
2. $\Delta(fg) = f(x + \Delta x) g(x + \Delta x) - f(x) g(x) = f(x + \Delta x) g(x + \Delta x) - f(x) g(x + \Delta x) + f(x)g(x + \Delta x) - f(x) g(x) = \Delta f g(x + \Delta x) + f(x) \Delta g \\
\frac{\Delta (f g)}{\Delta x} = \frac{\Delta f}{\Delta x} g(x + \Delta x) + f(x) \frac{\Delta g}{\Delta x} \xrightarrow[\Delta x \to 0]{} f'(x) g(x) + f(x) g'(x)$
3. $\Delta\left(\frac{f}{g}\right) = \frac{f(x + \Delta x)}{g(x + \Delta x)} - \frac{f(x)}{g(x)} = \frac{f(x + \Delta x) g(x) - f(x) g(x + \Delta x)}{g(x + \Delta x)g(x)} = \frac{f(x + \Delta x) g(x) - f(x) g(x) + f(x) g(x) - f(x) g(x + \Delta x)}{g(x + \Delta x)g(x)} = \frac{\Delta f g(x) - f(x) \Delta g}{g(x + \Delta x) g(x)}, \quad \frac{\Delta\left(\frac{f}{g}\right)}{\Delta x} = \frac{\frac{\Delta f}{\Delta x} g(x) - f(x) \frac{\Delta g}{\Delta x}}{g(x + \Delta x)g(x)} \xrightarrow[\Delta x \to 0]{} \frac{f'(x)g(x) -f(x)g'(x)}{g^2(x)} {}$

## Теорема (о производной сложной функции)

$
y = y(x) \text{ дифференцируема в т. } x_0; y_0 = y(x_0) \\
z = z(y) \text{ дифференцируема в т. } y_0 \\
z = z(y(x)), z - \text{ функция } x \text{ сложная функция от переменной } x \\
z_x' (x_0) = z_y'(y(x_0))y_x'(x_0) \\
z_x'(x_0) = z_y'(y_0) y_x'(x_0)
$

Доказательство $z(y)$ дифференцируема в т. $y_0 \quad \Delta z = z_y'(y_0) \Delta y + \alpha(\Delta y) \Delta y, \alpha(\Delta y) \xrightarrow[]{} 0, \Delta y \to 0$

Пример $\alpha(0) - 0$, тогда $\alpha(\Delta y)$ непрерывна в т. $\Delta y = 0$

$\Delta y = y(x_0 + \Delta x) - y(x_0) \implies \Delta y \xrightarrow[]{} 0, \Delta x \to 0, \alpha(\Delta y) = \alpha (y_0(x_0 + \Delta y) - y(x_0)) \xrightarrow[\Delta x \to 0]{} 0$

$
\frac{\Delta z}{\Delta x} = z_y' (y_0)\frac{\Delta y}{\Delta x} + \alpha(\Delta y) \frac{\Delta y}{\Delta x} \xrightarrow[\Delta x \to 0]{} z_y'(y_0) y_x'(x_0)
$

## Производная обратной функции
$x \in (a, b); -\infin \le a < b \le +\infin$

$y(x) -$ непрерывно возрастающая (убывающая) функция

$A = \underset{x\to a+}{\lim} y(x), b = \underset{x\to b-}{\lim} y(x); (A, B) -$ множество значений функции

$\forall y \in (A, B) \exists! x \in (a, b) \implies y = y(x)$

т. о. определна функция $x = x(y)$ - обраная функция функции $y(x)$

$
\left(
\begin{array}{l}
    x(y(x)) = x, x\in(a, b) \\
    y(x(y)) = y, y \in (A, B)
\end{array}
\right)
$

**Теорема** (о производной обратной функции)

Пусть $x = x(y)$ дифференцируема в т $y_0$ и $x_y'(y_0) \not= 0$

**Утверждение** Функция $y = y(x)$ дифференцируема в т. $x_0 = x(y_0)$ и $y_x'(x_0) = \frac{1}{x_y'(y_0)} {}$

**Доказательство** $\Delta x$ - приращение аргумента в т. $x_0, \Delta y = y(x_0 + \Delta x) - y(x_0), \Delta x \to 0 \implies \Delta y \to 0$, аналогично и $\Delta y \to 0 \implies x \to 0$

$y_x'(x_0) = \frac{\Delta y}{\Delta x} = \frac{1}{\left(\frac{\Delta x}{\Delta y}\right)} \xrightarrow[\Delta y \to 0]{} \frac{1}{x_y'(y_0)} {}$

