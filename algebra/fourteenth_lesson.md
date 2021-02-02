---
title: 14. Примеры групп, смежные классы
description: 
published: 1
date: 2021-02-02T21:32:09.499Z
tags: 
editor: markdown
dateCreated: 2021-01-13T11:29:50.918Z
---

$\langle g \rangle$ - циклическая группа порожденная $g$, $\langle g \rangle = \{ g^n \} {}$

**Утверждение** Пусть $G$ - группа и $g \in G$. 
Тогда $|\langle g \rangle| = ord(g)$ ($|G|$ - число элементов в $G$) 

$\square$ Заметим, что если нашлись $k,s \in \N:\ g^k = g^s \implies g^{k - s} = e$ (домножим на $g^{-s}$) $\implies$ $ord(g) \le k - s$ 

Если $g$ имеет бесконечный порядок, то все элементы $g^n, n \in \Z$ различны $\implies \langle g \rangle$ содержит бесконечно много элементов $\implies$ в бесконечном случае доказано

Если же $ord(g) = m$, то из минимальности $m \in \N \implies e = g^0, g = g^1, \dots, g^{m - 1}$ попарно различны. Покажем, что $\langle g \rangle = \{e, g, g^1, \dots, g^{m - 1}\}$ то есть других элементов нет

$\forall n \in \Z \quad n = m \cdot q + r$, где $0 \le r < m \\
\implies g^n = g^{m \cdot q + r} = (g^m)^q \cdot g^r = e^q \cdot g^r = g^r$, где $0 \le r < m \\
\implies \langle g \rangle = \{e, g, \dots, g^{m - 1}\}$ и $|\langle g \rangle| = m = ord(g)\ \blacksquare$

---

**Определение** Ядром гомоморфизма $f$ ($f: G \to F$) называется множество элементов группы $G$, которые переходят в $e_F$ (нейтральный элемент во второй группе)

$$
Ker(f) = \{g \in G | f(g) = e_F\}
$$

**Замечание** $Ker(f)$ всегда $\not= \varnothing$ т.к. по свойсву гомоморфизма $f(e_G) = e_F$. То есть $e_G \in Ker(f)$ всегда

**Утверждение** Пусть $f: G \to F$ - гомоморфизм

$f$ - инъективен $\iff Ker(f) = \{e_G\} {}$

$\square$ Необходимость ($\implies$)

Дано: $\forall x_1 \not= x_2: f(x_1) \not= f(x_2) \implies f(e_G) = e_F$ (и для $x \in G$ и $x \not= e_G$, $f(x) \not= f(e_G) = e_F$)

Достаточность ($\Longleftarrow$):

Дано $Ker(f) = e_G$

Предположим, что $\exists x_1 \not= x_2: f(x_1) = f(x_2)$. 

Тогда $f(x_1 \cdot x_2^{-1}) = e_F = f(x_1) \cdot (f(x_2))^{-1} = f(x_1) \cdot f(x_2^{-1}) \implies \\
\implies x_1 \cdot x_2^{-1} = e_G \iff x_1 = x_2$ противоречие $\implies f$ - мономорфизм $\blacksquare$

**Определение** Таблица Кэли это матрица

$$
\begin{array}{c|c c c c c}
\text{1-й / 2-й} & g_1 & g_2 & \dots & g_n & \dots \\
\hline
g_1 & g_1 \cdot g_1 & g_1 \cdot g_2 & \dots & g_1 \cdot g_n & \dots \\
g_2 & g_2 \cdot g_1 & g_2 \cdot g_2 & \dots & g_2 \cdot g_n & \dots \\
\dots & \dots & \dots & \dots & \dots & \dots \\
g_m & g_m \cdot g_1 & g_m \cdot g_2 & \dots & g_m \cdot g_m & \dots \\
\dots & \dots & \dots & \dots & \dots & \dots \\
\end{array}
$$

**Замечание** Группа $G$ - абелева $\iff$ таблица Кэли - симметрическая матрица

**Замечание** В каждой строке (столбце) таблицы Кэли стоят различные элементы

т. к. $\underbrace{g_i \cdot g_j}_{\text{элементы таблицы Кэлли}} = g_k \cdot g_j \iff g_i = g_k \iff i = k$

Примеры групп:

1. $Dn$ - группа диэдра - группа симметрий правильного $n$-угольника. Там есть $n$ вращений и $n$ симметрий

$Dn = \{r, s | r^n = 1, s^2 = 1, s^{-1} r s = r^{-1}\}$

Утв. Группа подстановок к $D_3 \cong S_3$

$
\varphi_0 \sim id, \varphi_{4\pi} \sim (1 \space 2 \space3), \varphi_{4 \pi / 3} \sim (1 \space 3 \space 2)
$ - повороты

$
\psi_1 \sim (2 \space 3), \psi_2 \sim (1 \space 3), \psi_3 \sim (1 \space 2)
$ - симметрии


Если выписать таблицы Кэлли - они совпадут

2. $A_n \subset S_n$. Название: $A_n$ знакопеременная группа. Все четные подстановки длины $n$ (с операцией композиции)

3. $Q_8 = \{\pm 1, \pm i, \pm j, \pm k | (-1)^2 - 1, i^2 = j^2 = k^2 = -1 = ijk\} {}$

$$
% Сгенерировано кодом: https://gist.github.com/iliakonnov/608432e0a96799b7b8012b7c0223f8c5
% Я же не псих переписывать/считать всё самому. Можно легко где-то ошибиться...
\begin{array}{r | r r r r r r r r}
& 1 & -1 & i & - i & j & - j & k & - k\\
\hline
1 & 1 & -1 & i & - i & j & - j & k & - k\\
-1 & -1 & 1 & - i & i & - j & j & - k & k\\
i & i & - i & -1 & 1 & k & - k & - j & j\\
- i & - i & i & 1 & -1 & - k & k & j & - j\\
j & j & - j & - k & k & -1 & 1 & i & - i\\
- j & - j & j & k & - k & 1 & -1 & - i & i\\
k & k & - k & j & - j & - i & i & -1 & 1\\
- k & - k & k & - j & j & i & - i & 1 & -1
\end{array}
$$

---

*Пример* $GL_n(\R) \to \R^* (\det A)$

т.е. $f(A) = \det A$ - это гомоморфизм

$Ker(f) = \{A | \det A = 1\} = SL_n(\R)$

**Утверждение** $\forall$ подгруппа в $(\Z, +)$ имеет вид $k \Z$, для некоторых $k \in N \cup \{0\}$ (числа, кратные $k$, т. е. при $k = 3, -6, -3, 0, 3, 6, 9, \dots$)

$\square k \Z$ очевидно является подргуппой. Докажем, что других нет. Если $H = \{0\}$, то положим $k = 0$. Иначе: $k = \min(H \cap \N)$. Тогда $k \Z \subseteq H$

Если $a \in H$ и $a = qk + r$ поделили $a$ с остатком на $k$)

$0 \le r < k$ и $\implies r = a - q \cdot k \in H \implies r = 0$ и $H = k \Z \blacksquare$

**Определение** Пусть $G$ - группа и $H$ - ее подгруппа. Пусть фиксирован $g \in G$. Левым смежным классам элемента $g$ по подгруппе $H$ называется множество $gH = \{g \cdot h | h \in H\}$ (а правый симметричным класс: $Hg = \{h \cdot g | h \in H\}$)

**Лемма 1** $\forall g_1, g_2 \in G$ либо $g_1 H = g_2 H$ либо $g_1 H \cap g_2 H = \varnothing$

$\square$ Если $g_1 H \cap g_2 H \not= \varnothing$, то $g_1 \cdot h_1 = g_2 \cdot h_2 \implies \\
\implies \exists h_1, h_2 \in H: g_1 = g_2 \cdot h_2 \cdot h_1^{-1} \implies 
\implies g_1 H = g_2 \cdot h_2 \cdot h_1^{-1} H \subseteq g_2 H$ - это лежит в $H$. И аналогично есть обратное включение $\implies g_1 H = g_1 H \blacksquare$
