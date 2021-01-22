---
title: 4. Индукции и начала теории чисел
description: 
published: 1
date: 2020-11-17T13:46:18.928Z
tags: 
editor: undefined
dateCreated: 2020-09-29T20:25:01.381Z
---

# Индукции и начало теории чисел

ПМИ (Принцип математической индукции):
$$
\forall X \subseteq \N, \\
\text{если } 0 \in X \land \forall n (n \in X \implies n + 1 \in X), \text{то } X = \N
$$

ПСИ (Принцип сильной индукции):
$$
\forall X \subseteq \N, \\
Prog(X) \implies X = \N
$$

ПНЧ (Принцип наименьшего числа):
$$
\forall X \subseteq \N, \\
X \not= \varnothing \implies \exists \min X
$$

> $$
> Prog(X) := \forall n (\forall m < n \space m \in X \implies n \in X)
> $$

---

I. Утверждение (1) ПСИ (2) ПНЧ (3) ПМИ равносильны
$$
(1) \implies 2 \\
\text{Доказательство} \\
\text{Дано: } \forall x \subseteq \N (Prog(X) \implies X = \N) \\
\text{Хотим: } \forall x \subseteq \N (x \not= \varnothing \implies \exists \min X)\\
$$
$$
\text{Рассмотрим } X \text{ такой, что } \nexists \min X \text{ Тогда } Prog(\overline{X}) \\
Действительно, \\
Prog(\overline{X}) \iff \forall n (\forall m < n \space m \in \overline{X} \implies n \in \overline{X}) \\
Prog(\overline{X}) \iff \forall n (\forall m < n \space m \not\in x, \implies n \not\in X) \\
Prog(\overline{X}) \iff \forall n (n \not= \min X) \iff \nexists \min X
$$
$$
(\forall m < n \space m \not\in X \quad n \in X) \implies n = \min X \\
\text{т.к. } \min \text{ нет, то } \forall m < n \space m \not\in X \implies n \not\in X \\
$$

По ПСИ, из $Prog(\overline{X})$ следует $\overline{X} = \N$, тогда $X=\varnothing$

---

$$
(2) \implies (3) \\
\text{Дано } \forall X \subseteq \N (X \not= \varnothing \implies \exists \min X) \\
\text{Хотим } \forall X \subseteq \N (0 \in X \land \forall n (n \in X \implies n + 1 \in X)
\implies X = \N) \\
\text{Допустим } 0 \in X \text{ и } \forall n (n \in X \implies n + 1 \in X) \\
\text{Хочу: } X = N \\
\text{Рассмотрим } \overline{X} \text{ Допустим существует } n = \min X \\
\begin{array}{c|c}
\text{I случай:} & \text{II случай:}\\
0 \in \overline{X} & \exists m \quad n = m + 1\\
0 \not\in X & m+1 \not\in X \\
\perp & \text{т. к. } m+1 = \min \overline{X} \text{, то} \\
& m \not\in \overline{X}, \text{т. к. } m < m + 1 \\
& m \in X \text{ тогда } m + 1 \in X
& \perp
\end{array}\\
$$
Значит, $\nexists \min \overline{X}$, тогда по ПНЧ, $\overline{X} = \varnothing$, т. е. $X = \N$

---

$$
(3) \implies (1) \\
\text{Дано: } \forall x \subseteq \N, \text{ если } 0 \in X \land \forall n 
(n \in X \implies n + 1 \in X), \text{ то } X = \N \\
\text{Хотим: } \forall X \subseteq \N, Prog(X) \implies X = \N \\
\text{Допустим: } Prog(X), \text{т. е. } \forall n(\forall m < n\space m\in X\implies n\in X)\\
(!) \text{Рассмотрим } Y = \{n \in N | \forall m < n \space m \in X\} \\
\text{Утверждение 1: } 0 \in Y \\
\underbrace{\forall m < 0 \space m \in X}_{\text{истина}} \iff \forall m 
(\underbrace{\overbrace{m < 0}^{\text{ложь}} \implies m \in X}_{\text{истина}}) \\
\text{Утверждение 2: } \forall n (n \in Y \implies n + 1 \in Y) \\
\text{допустим, что } n \in Y, \text{ т.е. } \forall m < n \quad m \in X \\
\text{т. к. } Prog(X), \text{ то } n \in X \\
\text{хочу: } n + 1 \in Y, \text{т. е. } \forall m < n + 1 \quad m \in X \\
\text{допустим } m < n + 1 \\
\begin{array}{c|c}
\text{I случай } & \text{II случай } \\
m < n & m = n \\
m \in X & n \in X \implies m \in X
\end{array} \\
\text{Применим ПМИ к } Y \text{ тогда получим } Y = \N \\
\text{Утверждение: } X = \N \\
\text{Рассмотрим } n \in \N \\
\begin{rcases}
n + 1 \in Y \\
n < n + 1
\end{rcases}\implies n \in X \\
X = Y = \N
$$
> Дашков сказал: Получили одинаковый вывод разными способами, значит спосовбы эквивалентны

## Основы теории чисел
Рассматриваем $\Z$ (целые числа)

"$a$ делит $b$" ($\iff$ $b$ делится на $a$)

Определение 
$$
\boxed{a|b \iff \exists k \quad b = a \cdot k}
$$

Примеры: 
- $2|6$, т. к. $6 = 2 \cdot 3$
- $2|2$, т. к. $2 = 2 \cdot 1$
- $-2|6$, т. к. $6 = (-2) \cdot (-3)$
- $2020|0$, т. к. $0 = 2020 \cdot 0$
- $\boxed{0|0}$, т. к. $0 = 0 \cdot 2019$
- $1|2020$, т. к. $1 = 1 \cdot 2020$

Утверждение 1
$$
\forall a (1 | a \land a | 0) \\
a = 1 \cdot a \quad 0 = a \cdot 0
$$

Утверждение 2
$$
a|b \land b|c \implies a|c
$$

Утверждение 3
$$
a|b \land b|a \implies a = \pm b
$$

Утверждение 4
$$
a|b \land a|c \implies a|(b+c) \land a|(b-c)
$$

Утверждение 5
$$
a|(b+c) \land a|b \implies a|c \\
a|(b-c) \land a|b \implies a|c
$$

### Теорема (деление с остатком)
Лемма
$$
\forall a,b \in \N \text{ если } b \not=0 \quad \exists!(q,z) \in \N^2 \\
a = bq + r \land 0 \le r < b
$$

