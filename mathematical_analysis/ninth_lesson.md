---
title: 9. Вторая теорема Верштрасса и дифференцирование
description: 
published: 1
date: 2020-11-17T14:36:13.837Z
tags: 
editor: markdown
dateCreated: 2020-11-10T11:26:40.705Z
---

# Вторая теорема Вершртрасса и дифференцирование

$
\varnothing \not= A \subset \R \\
M \in \R$ - это верхняя грань множества $A$, если
1. $\forall x \in A \implies x \le M$
2. $\forall \varepsilon > 0 \exists x \in A \implies M - \varepsilon < x \le M$

$M = \sup A$

---

$m \in \R$ - нижняя грань $A$, если
1. $\forall x \in A \implies x \ge m$
2. $\forall \varepsilon > 0 \exists x \in A \implies m + \varepsilon > x \ge m$

$m = \inf A$

---

**Теорема** Ограниченное сверху (снизу) множество имеет верхнюю (нижнюю) грань

## Вторая теорема Верштрасса
Функция, непрерывная на отрезке, принимает на этом отрезке этом отрезке наибольшее и наименьшее значение

$\exists x_{\max} \in [a, b], x_{\min} \in [a, b] \forall x \in [a, b] \implies f(x_{\min}) \le f(x) \le f(x_{\max})$

---

Пример $f(x) = x, x \in (0; 1)$

*Доказательство* для точек множество значений функции ограничено  (по 1ой теореме Верштрасса) пусть $M$ - верхняя граница Тр. док.: $\exists x (=x_{\max}); f(x) = M$

Пусть такой точки не существует $\implies \forall x \in [a, b] f(x) < M$

Рассмотрим $q(x) = \frac{1}{M - f(x)} \implies q(x)$ непрерывна на $[a, b] \implies g(x)$ ограничена на $[a, b]$

Но $M = \sup {y| y = f(x), x \in [a, b]}$ для $\varepsilon = \frac{1}{n} \exists x_n \in [a, b] \implies f(x_n) > M - \frac{1}{n} {}$

$\frac{1}{n} > M - f(x_n) \implies n < \frac{1}{M - f(x_n)} = g(x_n) \implies g(x_n) \xrightarrow[n \to \infin]{} +\infin$ т. е. $g(x)$ - неограничено. Противоречие

## Дифференциальное исчисления функции одного переменного

$f$ окружение $O_n (x_n) x - x_0 = \Delta x$

**Определение** Если существует $\underset{\Delta x\to0}{\lim} \frac{\Delta f}{\Delta x} = \underset{\Delta x \to0}{\lim} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \underset{x\to x_0}{\lim} \frac{f(x) - f(x_0)}{x - x_0} {}$

То функция $f$ диффиренцируема в точке $x_0$

$\underset{x\to0}{\lim} \frac{\Delta f}{\Delta x} = f'(x_0)$ - производная функции $f$ в т. $x_0$

---

1. $f(x) = C(const); \Delta f= 0. f'(x) = 0$
2. $(x^n)' = n\cdot x^{n-1}; n = 1,2,3,\dots\\
(x + \Delta)^n - x^n = x^n + C_n^1 x^{n-1} \Delta x + C_n^2 x^{n-2}(\Delta x)^2 + \dots + C_n^n (\Delta x)^n - x^n\\
\frac{(x + \Delta x)^n - x^n}{\Delta x)} = n\cdot x^{n-1} C_n^2 x^{n-2} (\Delta x) + \dots + C_n^n (\Delta x)^{n-1} \xrightarrow[\Delta x \to 0]{} n x^{n-1} {}$
3. $(\sin x)' = \cos x\\
\sin(x + \Delta x) - \sin x = 2\sin \frac{\Delta x}{2} \cos \frac{2x + \Delta}{2}\\
\frac{\sin (x + \Delta x) - \sin x}{\Delta x} = 2 \frac{\sin \frac{\Delta x}{2}}{\Delta x} \cdot \cos (\frac{2x + \Delta x}{2}) \xrightarrow[\Delta x\to0]{} \cos x$
4. $(\cos)' = -\sin x$
5. $(e^x)' = e^x; \underset{\Delta x\to 0}{\lim} \frac{e^{x+\Delta x} - e^x}{\Delta x} = \underset{\Delta x \to 0}{\lim} e^x \frac{e^{\Delta x} - 1}{\Delta x} = e^x$
6. $(\ln x)' = \frac{1}{x} \quad \underset{\Delta x \to 0}{\lim} \frac{\ln(x + \Delta x) - \ln x}{\Delta x} = \underset{\Delta x \to 0}{\lim} \frac{\ln(1 + \frac{\Delta x}{x})}{\Delta x} = \underset{\Delta x\to0}{\lim} \frac{\frac{Delta x}{x}}{\Delta x} = \frac{1}{x} {}$

### Геометрический смысл производной
$y = f(x); x_0$

$A(x_0, y_0) \quad B(x_0 + \Delta X, y_0 + \Delta y); \Delta y = f(x_0 + \Delta x) - f(x_0)\\
y - y_0 = x(x - x_0) = \tg \alpha (x - x_0)$\
пусть $B \to A$, т. е. $\Delta x \to 0$\
$\tg \alpha = \frac{\Delta y}{\Delta x}$ если функция $y = y(x)$ дифференцируема в т. $x_0$,\
то $\exists \underset{\Delta x\to0}{\lim} \frac{\Delta y}{\Delta x} = y'(x_0).$ предельные положение секущей прямой $AB$ при $B \to A$ называется касательной к графику функции в т. $A(x_0, y_0)$. Уравнение касательной $y - y_0 = y'(x_0)(x - x_0)$\
Уравнение нормали $y - y_0 = - \frac{1}{y'(x_0)}(x - x_0)$

---

$k - y_0 = k(x - x_0) = \tg \alpha (x - x_0)\\
\frac{\Delta y}{\Delta x} \to y'(x_0) \\
y - y_0 = y'(x_0)(x - x_0)$
