---
title: 7. Функции, непрерывные в точке и точки разрыва
description: 
published: 1
date: 2020-10-27T11:31:26.664Z
tags: 
editor: undefined
dateCreated: 2020-10-27T11:31:16.404Z
---

# Функции непрерывные в точке

$$
\lim_{x\to a} f(x) = f(a)
$$

### Свойство 3 (Арифметичесике свойва)
$f, g$ - непрерывны в точке $a$

Утверждение $f(x) \pm g(x); f(x) \cdot g(x), \frac{f(x)}{g(x)} (g(a) \not= 0)$

Доказательство:

Из теормемы сохранения знака непрерывной функции

$$
\lim_{x\to a}\frac{f(x)}{g(x)} = \frac{\underset{x\to a}{\lim} f(x)}{\underset{x\to a}{\lim} g(a)} = \frac{f(a)}{g(a)}
$$

### Свойство 4 (Теорема о непрерывности сложной функции)

$$
y = f(x) \quad \text{опр } O_{h_1}(a); \text{неопр. в т. } a; b = f(a) \\
z = g(y) \quad \text{опр } O_{h_2}(b); \text{неопр. в т. } b; \\
\text{если } x \in O_{h_1}(a), f(x) \in O_{h_2} (b) \\
\text{Утв. } z= g (f(x)) \text{ неопределена в т. } a
$$

$$
\text{Доказательство}: \\
\forall \varepsilon > 0 \exists \delta - \delta_y > 0 \forall y \in O_{\delta_g} \implies g(y) \in O_\varepsilon (g(b)) \space (|g(y) - g(b)| < \varepsilon) \\
\text{для } \delta_g > 0 \exists \delta = \delta_f > 0 \forall x \in O_{\delta_f}(f) \implies f(x) \in O_{\delta_g} (b) \\
\forall \varepsilon > 0 \exists \delta = \delta_f > 0 \forall x \to O_{\delta_f}(a) \implies g(f(x)) \in O_\varepsilon (g(b)) = O_\varepsilon (g(f(x))) \\
\text{т. е. } g(f(x)) \text{ не определена в т. } a
$$

---

## Точки разрыва

$$
f(x) - \text{ либо разрывка в т. } a, \text{ либо не определена в т. } a
$$

**Определение** т. $a$ - точка разрыва $1^{го}$ рода функции $f$, если
$$
\exists \lim_{x\to a+} f(x): \exists \lim_{x\to a-} f(x) (\text{конечные пределы!}) \\
$$
Если $\underset{x\to a+}{\lim} f(x) \underset{x\to a-}{\lim} f(x)$, то $a$ - точка устранимого разрыва. 

Точка разрыва, которая не является точками разрыва $1^{го}$ рода, называются точками разрыва $2^{го}$ рода

---

**Пример 1**
$$
f(x) = \frac{\sin(x)}{x}; a = 0
$$

Точка разрыва $1^{го}$ рода устранима

**Пример 2**
$$
f(x) = \arctg \frac{1}{x}; a = 0 \quad \lim{x\to0+} f(x) = \frac{\pi}{2}; \lim_{x\to0-} f(x) = -\frac{\pi}{2}
$$

Разрыв $1^{го}$ рода

**Пример 3**
$$
f(x) = e^{\frac{1}{x}}; \lim_{x\to0+}f(x) = +\infin; \lim_{x\to0-} f(x) = 0
$$

Разрыв $2^{го}$ рода

**Пример 4**
$$
f(x) = \sin \frac{1}{x}; a = 0 \text{ Не существует } \lim_{x\to0+}f(x), \lim_{x\to0-}f(x)
$$

Разрыв $2^{го}$ рода
