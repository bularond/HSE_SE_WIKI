---
title: 3. Еще строки, ПМИ ПСИ и ПНЧ
description: 
published: 1
date: 2020-11-17T13:46:40.999Z
tags: 
editor: undefined
dateCreated: 2020-09-22T11:53:18.529Z
---

# Немного обобщения с прошлой лекции

$A$ - алфавит\
$S(A)$ - множество всех строк над $A$
1. $[] \in S(A)$
2. $\forall s \in S(A) \forall x \in A \quad x:s \in S(A)$

$[1,2,3] = 1:(2:(3:[]))$


$
\forall s \forall t \forall x: \\
app([], t) = t \\
app(x:s, t) = x:app(s, t)
$

**Лемма 1**
$\forall s \; app(s, [])= s$

ПИ для $S(A)$\
$\forall$ унарного предиката П над $S(A)$, если $P([]) \land \forall x \forall s (P(s) \implies P(x:s))$,
то $\forall s P(s)$

# Продолжение разговора о строках

$(n+m)+l \stackrel{?}{=} n+(m+l)$

**Лемма 2**
$$
\forall r \forall t \forall s \space
app(s, app(t, r)) = app(app(s, t), r)
$$

**Доказательство:**
$P(s) := app(s, app(t, r)) = app(app(s, t), r))$

Рассмотрим произвольные $r$ и $t$
Индукция по $S$
$$
\text{Нужно} \space \forall s P(s) \\
\underline{\text{БАЗА:}} \space \text{Хотим -} P([]) = (app([],app(t,r)))=app(app([],t),r)\\
\text{Левая часть} = app([], app(t, r)) = app(t, r) \\
\text{Правая часть} = app(app([], t), r) = app(t, r)
$$
$$
\underline{\text{ШАГ}}: \forall s \forall x (P(s) \implies P(x:s)) \\
\text{Рассмотрим произвольные } x \text{ и } s \\
\text{Хотим}: P(s) \implies P(x:s) \\
\text{Допустим, } P(s) \\
P(s) = (app(s, app(t, r))) = app(app(s, t), r) \\
\text{Хотим } P(x:s) \\
P(x:s) = (app(x:s, app(t, r))) = app(app(x:s, t), r) \\
\text{ЛЧ} = app(x:s, app(t, r)) = x:app(s, app(t, r)) \\
\xlongequal{\text{I.H.}} x:app(app(s, t), r) \xlongequal{\text{опр}} 
app(x: app(s, t), r) \\
\xlongequal{\text{опр}} app(app(x:s, t), r) = \text{ПЧ}
$$

По ПИ: $\forall s P(s)$ т.к. $r$ и $t$ произвольные, имеем $\forall r \forall t \forall s\space
app(s, app(t, r)) = app(app(s, t), r)$

---

$n+m \stackrel{?}{=} m+n$

**Утв** 
$\exist s \exist t \space app(s,t) \neq app(t,s)$

Ваще сказали это дома доказать но мне лень:)

$n+m = n+k \iff m = k$

---

**Лемма 3**

$$
\forall t \forall r \forall s \\
app(s, t) = app(s, r) \implies t = r \\
\text{Рассмотрим t,r - произвольные} \\
P(s) := (app(s, t) = app(s, r) \implies t = r)
$$
$$
\underline{\text{БАЗА}}: P([]) = (app([], t) = app([], r) \implies t = r) \\
\text{Допустим: } \underset{\xlongequal{\text{опр}} \space t}{app([], t)} = 
\underset{\xlongequal{\text{опр}} \space r}{app([], r)} \\
t = r \\
\text{база доказана}
$$
$$
\underline{\text{ШАГ}}: \forall x \forall s \\
\text{Пусть } P(s) \text{ Хотим } P(x:s) \\
P(s) = (app(s, t) = app(s, r) \implies t = r) \\
P(x:s) = (app(x:s, t) = app(x:s, r) \implies t = r) \\
\text{допустим: } \underset{\xlongequal{\text{опр}} \space x:app(s, t)}{app(x:s, t)} = 
\underset{\xlongequal{\text{опр}} \space x:app(s, r)}{app(x:s, r)} \\
app(s,t) = app(s,r) \\
\text{По предположению индукции} \\
t = r \\
\blacksquare
$$

Еще можно было вспомнить аксиому 2

**Аксиома 2**
$\forall x \forall y \forall s \forall t \quad (x:s = y:t \iff x = y \land s = t)$

$\text{По А2 } app(s, t) = app(s, r) \implies t = r$

---

$$
\forall s \forall t \forall r\\
app(t, s) = app(r, s) \implies t =r
$$
Это тоже сказали попробовать доказать дома. Типо посмотреть что это так просто не доказывается.

---

**Лемма 4** 
$$
\forall s \forall t \quad app(s, t) = [] \implies s = [] \land t = [] \\
\square \text{Рассмотрим произвольные } s \text{ и } t \\
\text{Допустим } app(s, t) = [] \\
\text{I случай: } s = [] \text{ , тогда } app([], t) \stackrel{опр}{=} t = [] \\
\text{II случай: } \exist x \exist r s = x:r\\ 
\text{Тогда } app(x:r, t) = [] \\
\text{По определению: } x:app(r, t) = [] \\
\text{По аксиоме 1} (\forall x \forall s \quad x:s \not= []) \\
\text{Противоречие } \implies s = [] \land t = [] \blacksquare
$$

# Любимая индукция теперь еще и на чиселках

ПИ для $\N$\
$\forall$ унарного придиката $P$ над $\N$, если 
$P(0) \land \forall (P(n) \implies P(n + 1))$, то $\forall n P(n)$

> Здесь и далее все числа $\in \N (0 \in \N)$

> $A \subseteq B$ $\\$
> "A - подмножество B" $\\$
> $A \subseteq B \iff \forall x (x \in A \implies x \in B)$
 
> $A \setminus B = \{x\in A | x \notin B\}$ $\\$
> "A без B" типо

> $x \subseteq \N; \varnothing$ (хз че это значит) $\\$
> $\bar{x} = \N \setminus x$ 

## ПМИ (принцип мат. индукции)

$\forall X \subseteq \N$, если $0 \in X \land \forall n(n \in X \implies (n+1) \in X)$,
то $X = \N$

## Принцип сильной (порядковой) индукции
$$
P(n) = (n \in X), x := {n \in \N | P(n)} \\ \ \\
\text{Пусть } P(0) \land \underbrace{\forall n((P(0) \land P(1) \land P(2) \land \dots \land P(n-1))}_{\text{I.H.}} \implies P(n)) \\ 
\text{тогда } \forall n P(n)
$$

## Прогрессивность

**Определение**\
Пусть $x \subseteq \N$. Тогда $x$ прогрессивно, если $\forall n ((\forall m < n (m\in X)) \implies
n \in X)$
$Prog(X)$


Пример: $Prog(\N)$

Еще пример:
$$
X_1 = {0; 2; 4; 6; \dots} \\
\forall m < 1 \quad m \in X_1 \\
1 \notin X_1 \quad \lnot Prog(X_1)
\cdot X_2 = {1; 3; 5; \dots} \\
\forall m < 0: m \in X_2 \\
0 \notin X_2 \\
\forall m < 0, m\in X_2 \iff \forall m \underbrace{(\underbrace{m < 0}_\text{ложь}
\implies m \in X_2)}_\text{истина}
$$

---

**Лемма** (еще одна блядская лемма, может хватит уже она даже никак не обозначена сколько можно то)
$$
\forall X \subseteq \N (Prog(X) \implies 0 \in X) \\
\square \text{Допустим: } Prog(x) \text{, тогда } \forall n (\forall m < n \space ( m \in X \implies n \in X))\\
\underbrace{\forall m < 0 \ m \in X}_\text{верно} \implies \underbrace{0 \in X}_\text{верно}
$$

## ПСИ (Принцип сильной индукции)
$\forall x \subseteq \N \ (Prog(X) \implies X = \N)$

## ПНЧ (принцип наименьшего числа)
Если есть какое-то число со свойством, есть и наименьшее такое число
$$
\forall X \subseteq \N (X \not = \varnothing \implies \exist n 
\underbrace{(n \in X \land \forall m (m \in X \implies n \le m ))}_{\exist min \space X})
$$

---

**Теорема**\
Следующие утверждения равносильны:
1. ПСИ
2. ПНЧ
3. ПМИ

$ПСИ \implies ПНЧ \implies ПМИ \implies ПСИ$

$(1) \implies (2)$ Дано ПСИ. Хотим: ПНЧ
$$
\forall X (x \not = 0 \implies \exist min \space X) \\
(\lnot B \implies \lnot A \equiv A \implies B) ||| \\
\forall X (\nexists min \space X \implies x = \varnothing) \\
\text{Утверждение } \nexists min \space X \iff Prog(\bar{X}) \\
\text{Дано } \nexists min \space X \\
\text{Хочу: } \forall n (\forall m < n \space m \notin \bar{x} \implies n\in\bar{X}) \\
\forall n (\forall m < n \space m \notin X \implies n \notin X) \\
\forall n (n \in X \implies \lnot \forall m < n \space m \notin X) \\
\forall n (n\in X \implies \exist m < n \space m \in X) \\
\forall n (n \in X \implies n \not min \space X) \\
\nexists min \space X \\
\forall x (\nexists min \space X \implies x \subset \varnothing) \implies \\
\implies Prog(\bar{x}) \xRightarrow[\text{ПСИ}]{} \bar{X} = \N \implies x = \varnothing
\blacksquare
$$