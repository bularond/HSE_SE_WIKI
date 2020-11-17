---
title: 5. Свойства пределов функций
description: 
published: 1
date: 2020-10-11T13:03:28.587Z
tags: 
editor: undefined
dateCreated: 2020-10-06T11:28:53.088Z
---

# Свойства пределов функций

> $$
> т \not= X \subset \R; f \text{ определена } X; a - \text{ предельная точка множества } X
> $$

$$
\lim_{x\to\infin} f(x) = A \\
\text{I (по Гейне) } \forall x_n \in X, x_n \longrightarrow a, x_n \pm a \implies f(x_n) \longrightarrow A; n\to\infin \\
\text{II (по Коши) } \forall \varepsilon > 0 \exists \delta > 0 \forall x \in \mathring O_\delta (a) \cap X \implies |f(x) - A| < \varepsilon
$$

## Теоремы пределов функций

**Теорема 1** Определения $\text{I}$ и $\text{II}$ эквивалентны
$$
\text{II} \implies \text{I} \quad \forall \varepsilon > 0 \exists \delta > 0 \forall x \in \mathring O_\delta (a) \cap X \implies |f(x) - A| < \varepsilon \\
\text{пусть } x_n \not= A_1, x_n \longrightarrow a (n \to \infin). \exists N \forall n \ge N \implies x_n \in \mathring O_\delta (a) \cap x \implies \\
\implies |f(x_n) - A| < \varepsilon \text{ т. е. } f(x_n) \longrightarrow \bar A, n \to \infin
$$

$$
\text{II} \implies \text{I} \quad \text{от противного. пусть определение I выполнено но II не верно} \\
\text{т. е. } \exists \varepsilon > 0 \forall S = \frac{1}{n} (n = 1, 2, \dots) \exists x_n \in \mathring O_{\delta=\frac{1}{n}} (a) \implies |f(x_n) - A| \ge \varepsilon \implies \\
\implies x_n \not= a, x_n \to a, f(x_n) \not\longrightarrow A. \text{ Противоречие}
$$

**Теорема 2** (об арифметический свойствах пределов функций)
$$
\lim_{x\to a} f(x) = A; \lim_{x\to a} g(a) = B \\
$$
Тогда: 
1. $\underset{x\to a}{\lim}(f(x) \pm g(x)) = A \pm B$
2. $\underset{x\to a}{\lim}(f(x)\cdot g(x)) = A \cdot B$
3. $\underset{x\to a}{\lim}\frac{f(x)}{g(x)} = \frac{A}{B} \space$

---

Доказательство 3
$$
\text{пусть } x_n \in x, x_n \not= a, x_n \longrightarrow a(n\to \infin) \\
f(x_n) \longrightarrow A, g(x_n) \longrightarrow B, g(x_n) \not= 0, B\not= 0 \implies \frac{f(x_n)}{g(x_n)} \longrightarrow \frac{A}{B} \\
$$

---

**Теорема 3** (о пределе зажатой фунции)
$$
f(x) \le g(x) \le k(x) \text{ Если } \lim_{x\to A}f(x) = \lim_{x\to a} h(x) = A, \text{ то } \lim_{x\to a} g(x) = A
$$
Доказательство
$$
x_n \longrightarrow a (x_n \not= a) \implies f(x_n) \le g(x_n \le h(x_n))
$$

## Различные типы пределов
Пример: 
$$
f(x) = \frac{x}{|x|} = \begin{cases}
1, & x > 0 \\
-1, & x < 0
\end{cases} \\
\lim_{x\to 0} f(x) \text{неосуществим} \\
x_n = \frac{1}{n}; f(x_n) = 1 \longrightarrow 1 \\
x_n = -\frac{1}{n} f(x_n) = -1 \longrightarrow -1 \\
\lim_{x\to 0+} f(x) = 1; \lim_{x\to 0-} f(x) = 01
$$

---

**Определение** $\underset{x\to a+}{\lim} f(x) = A$
$$
\text{I (по Гейне) } \forall x_n \in X, x_n > a, x_n \xrightarrow[x\to \infin]{} a \implies f(x_n) \longrightarrow A, n \to \infin \\
\text{II (по Коши) } \forall \varepsilon > 0 \exists \delta > 0 \forall x \in (0, a + \delta) \cap X \implies |f(x) - A| < \varepsilon \\
$$

**Определение** $\lim_{x\to a-} f(x) = A$ аналогично

## Бесконечные пределы
Пример: 
$$
f(x) = \frac{1}{x - a} \\
\lim_{x\to a} f(x) = \infin \\
\text{I (по Гейне) } \forall x_n \in X, x_n \to a, x_n \pm a \implies f(x_n) \to \infin \\
\text{II (По Коши) } \forall \varepsilon > 0 \exists \delta > 0 \forall x \in \mathring O_\delta (a) \cap x \implies |f(x)| > \varepsilon
$$

---

$$
f(x) = \frac{1}{|x-a|} \\
\lim_{x\to a} f(x) = \infin \\
\lim_{x\to a} f(x) = +\infin \text{ т.е. I } \forall x_n \in X, x_n \not= a, x_n \longrightarrow a \implies f(x_n) \xrightarrow[x\to\infin]{} +\infin \\
\forall \varepsilon > 0 \exists N \forall n \ge N \implies f(x_n) \ge \varepsilon
$$

---

$$
\begin{array}{c c}
\text{Если } \\
\lim_{x\to a} f(x) = \infin & f(x) - \text{ б.б. функция при } x\to a \\
\lim_{x\to a} f(x) = 0 & f(x) - \text{б.м. функция при} x\to a
\end{array}
$$

**Теорема 4**
$$
f(x) \not= 0; f(x) - \text{б.м. } x\to a \iff \frac{1}{f(x)} - \text{б.б. } x\to a
$$

## Предел в бесконечностях
Пример:
$$
f(x) = \arctg(|x|) \\
\lim_{x\to\infin} f(x) = \frac{\pi}{2} \\
\text{I (по Гейне) } \lim_{x\to\infin} f(x) = A \\
\forall x_n \in X, x_n \xrightarrow[x\to\infin]{} \infin \implies f(x_n) \implies A \\
\text{II (по Коши) } \forall \varepsilon > 0 \exists \delta > 0 \forall x: |x| > \delta, x \in X \implies |f(x) - A| < \varepsilon
$$

---

Пример:
$$
f(x) = \arctg(x) \\
\lim_{x\to+\infin} f(x) = \frac{\pi}{2} \\
\lim_{x\to-\infin} f(x)
\begin{array}{c c c}
\lim_{x\to+\infin} f(x) =  A & \text{I (по Гейне) } & \forall x_n \in X, x_n \longrightarrow +\infin \implies f(x_n) \longrightarrow A \\
& \text{II (по Коши)} & \forall \varepsilon > 0 \exists \delta > 0 \forall x: x > \delta \implies |f(x) - A| < \varepsilon
\end{array}
$$

---

**Теорема** (второй замечательный предел)
$$
\lim_{x\to\infin} \left(a + \frac{1}{x}\right)^x = e \\
$$
Доказательство:
$$
1) \lim_{x\to+\infin}(1 + \frac{1}{x})^x = e \\
a_n = \left(1 + \frac{1}{n + 1}\right)^n = \frac{\left(1 + \frac{1}{n+1}\right)^{n+1}}{\left(1 + \frac{1}{n+1}\right)} \longrightarrow e. n\to\infin\\
b_n = \left(1 + \frac{1}{n+1}\right)^{n+1} \longrightarrow e \\
\forall \varepsilon > 0 \exists N \forall n \ge N \\
e - \varepsilon < \left(1 + \frac{1}{n+1}\right)^n < e + \varepsilon \\
e - \varepsilon < \left(1 + \frac{1}{n+1}\right)^{n+1} < e + \varepsilon \\
$$

Рассмотрим $x > 0$
$$
x: [x] > N \implies n \le x \le n+1 \implies \frac{1}{n+1} \le \frac{1}{x} \le \frac{1}{n} \implies 1 + \frac{1}{n+1} \le 1 + \frac{1}{x} \le 1 + \frac{1}{n} \implies \\
\implies \left(1 + \frac{1}{n+1}\right)^n \le \left(1 + \frac{1}{x}\right)^x \le \left(1 + \frac{1}{n}\right)^{n+1} \implies \\
\implies e - \varepsilon < \left(1 + \frac{1}{n+1}\right)^n \le \left(1 + \frac{1}{x}\right)^x \le \left(1 + \frac{1}{n}\right)^{n+1} < e + \varepsilon \\
\lim_{x\to+\infin}(1 + \frac{1}{x})^x = e
$$
