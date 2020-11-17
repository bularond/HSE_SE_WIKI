---
title: 5. Теория чисел
description: 
published: 1
date: 2020-11-03T15:21:32.875Z
tags: 
editor: undefined
dateCreated: 2020-11-03T15:21:20.732Z
---

# Теория чисел

Лемма\
$\forall a, b \in \N (b \not= 0 \implies \exists !(q, z) \in \N^2 \quad a = bq + 2 \land 0 \le z < b)$

Существование
$$
\text{Рассмотрим } X = \{s \in \N | b \cdot s > a\} \\
x < y \land z > 0 \implies x \cdot z < y \cdot z (z, y, x \in \N) \\
b (a + 1) = b a + b > b \cdot a \ge 1 \cdot a = a \\
a + 1 \in X \quad x \not= \varnothing \\
\text{По ПНЧ, } \exists s' - min X, b \cdot s' > a\\
\text{I случай } s' = 0 \text{ тогда } 0 = b \cdot 0 > a \text{ противоречие} \\
\text{II случай } \exists q \in \N \quad s' = q + 1 \\
\text{Помним } z = a - bq \\
q < s' \implies q \not\in X \implies bq \not> a \implies \\
\implies bq \le a \implies 0 \le a - bq = z \\
\text{Допустим } z = a - bq \ge b; \text{ Тогда } a \ge b(q + 1) = bs' > a \implies a > a \text{ противоречие}
$$

Единственность
$$
\text{Допустим } a = bq_1 + z_1' \land 0 \le z_1 < b \\
a = bq_2 + z_2 \land 0 \le z_2 < b \\
\text{Хочу } q_1 = q_2 \quad \text{ пусть не так } \\
q_1 > q_2 \\
0 = a - a = b(q_1 - q_2) + (z_1 - z_2) \\
z_2 - z_1 = b(q_1 - q_2) \ge b > 0\\
b > z_2 \ge z_1 + b \\
0 > z_1 \text{ противоречие} \\
\text{Значит } q_1 = q_2 \\
\text{Тогда } z_1 = a - bq_2 = z_2 
$$

---

Теорема (о делении с остатком)
$$
\forall a, b \in \Z (b \not= 0 \implies \exists! (q, z) \in \Z^2 \quad a = bq + z \land 0 \le z < |b|)\\
\text{По лемме } \exists(q', z') \in \N^2 \\
|a| = |b| \cdot q' + z'; 0 \le z' < |b| \\
\text{Тогда } a = sign(a) \left(\frac{b}{sign(b)}q' + z'\right) = b \left(\frac{sign(a)}{sign(b)}q'\right) + z'sign(a) \\
\text{II случай } a \ge 0 \lor z' = 0 \implies sign(a) = 1 \lor z' = 0 \\
q = \frac{sighn(a)}{sign(b)}q' \quad z'sign(a) = z' \\
z = z'sign(a) = z' \\
\text{II случай } a < 0 \land z' > 0 \\
sign(a) = -1 \\
a = b\left(\frac{-q'}{signb}\right) - z' = b\left(\frac{-q'}{signb}\right) - \frac{b}{sign(b)} - z' = b\left(\frac{-1-q'}{sign(b)}\right) + |b| - z' = bq + z \\
z' < |b| \implies |b| - z' > 0 \\
-z' > 0 \implies |b| - z' < |b|\\
$$

> $$
> sign x = \begin{cases}
> 1, & x \ge 0 \\
> -1, & x < 0
> \end{cases} \\
> x = |x| \cdot sign(x) \\
> $$

Единственность
$$
\text{Допустим } a = bq_1 + z_1 \quad a= bq_2 + z_2\\
\text{Хочу }  q_1 = q_1 \\
0 = a - a = b(q_1 - q_2) + (z_1 - z_2) \\
z_2 - z_1 = b(q_1 - q_2) = b(q_1 - q_2) \implies |z_2 - z_1| = |b| (q_1 - q_2) \ge b \\
\text{Б. о. о. Тогда } z_2 - z_1 \ge |b| \\
|b| > z_2 \ge |b| + z_1 \\
0 > z_1 \text{ Противоречие}
$$

---

**Определение** Пусть $a, b, \in \Z$ и $m > 1$. Тогда $a \equiv b (mod m) \iff m|(a-b)$ ($\iff a \equiv_m b \iff a \equiv b (m)$)

**Лемма**
$a \equiv b(m) \iff a$ и $b$ дают одинаковый остаток при делении на $m$. Т. е. $a\%m = b\%m$

$$
\text{Доказательство } \implies \text{Дано } m|(a - b) \\
\text{Тогда остаток } \exists a, q_2, z_1, z_2 \\
a = mq_1 + z_1 \\
b = mq_2 + z_2 \\
0 \ge z_1, z_2 < m \\
(a - b) = m (q_1 - q_2) + (z_1 - z_2) \implies m | (z_1 - z_2) \\
\text{Б. о. о. } z_1 \ge z_2 \text{ где  } \exists k \in \N \quad z_1 = z_2 + km \\
m > z_2 + k m \ge km \\
0m > km \\
k = 0 \\
z_1 = z_2 \text{ ч.т.д. }
$$

В другую сторону
$$
\text{Дано } \exists q_1, q_2, z \\
a = mq_1 + z \\
b = mq_2 + z \\
a - b = m ( q_1 - q_2 ) \\
\text{т. е. } m|(a - b)
$$

Лемма
$$
\forall a, b, c, m > 1 \quad (1) a \equiv a (m) \\
(2) a \equiv b (m) \implies b \equiv a (m);
(3) \begin{rcases}
a \equiv b (m) \\
b \equiv c (m)
\end{rcases} \implies a \equiv c (m)
$$

$$
\text{Доказательство } (3) \\
\text{В виду предыдущей леммы } a \equiv c (m) \Longleftarrow a \% m - c \% m \Longleftarrow
\begin{cases}
a \% m = b \% m \\
b \% m = c \% m
\end{cases}
$$


Лемма 2 $\forall a, b, c, m > 1 \forall n \in \N$
$$
\text{Пусть } a \equiv c(m)
$$
