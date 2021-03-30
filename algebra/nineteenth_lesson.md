---
title: 19. Факторкольцо, многочлены, поля
description: 
published: 1
date: 2021-03-30T13:44:52.206Z
tags: 
editor: markdown
dateCreated: 2021-02-24T11:33:21.748Z
---

**Лемма** $Ker(\varphi)$, где $\varphi$ - гомоморфизм колец, всегда являетя идеалом в кольце $K_1$ ($\varphi: K_1 \to K_2$)

$\square$ Идеал:
1. Подгруппа в $(K_1, +)$
2. $\forall a \in Ker(\varphi) \forall r \in K_1: a \cdot r \in Ker(\varphi) \land r \cdot a \in Ker(\varphi)$

Любой гомоморфизм колец является гомоморфизмом их их аддитивных групп $\implies Ker(\varphi)$ является нормальной подгруппой в $(Ker_1, +)$. Пусть $a \in Ker(\varphi)$ т. е. $\varphi(a) = 0$. Берем $a \cdot r$ и рассмотрим 

$\varphi(a \cdot r) = \varphi(a) \cdot \varphi(r) = 0 \cdot \varphi(r) = 0$

И аналогично $\varphi(r \cdot a) = \varphi(r) \cdot 0 = 0 \ \blacksquare$

**Лемма** $r \cdot 0 = 0 \cdot r = 0$

$\square\ r + 0 = r \implies r (r + 0) = r \cdot r \implies r^2 + r \cdot 0 = r^2 \mid + (-r^2) \\ 
r \cdot 0 = 0$ $\blacksquare$

## Факторкольцо

Любой идеал явялется нормальной подгруппой в $(K, +) \implies$ можно рассмотреть факторгруппу $K/I$ (по сложению). Введем в этой факторгруппе умножение: $(a + I) (b + I) = a \cdot b + I$ (используется свойства идеала: $aI$ и $bI$ это элементы $I$)

> Умножение корректно, т. к. $
> \forall a', b' \in K$ таких что: $\\
> a + I = a' + I \\ 
> b + I = b' + I$ - взяли других представителей того же смежного класса$\\
> a' = a + x, x \in I \\
> b' = b + y, y \in I \\
> \rightarrow a' \cdot b' + I = (a + x) \cdot (b + y) + I = a \cdot b + \underbrace{a \cdot y}_{\in I} + \underbrace{x \cdot b}_{\in I} + I
> $
{.is-info}

**Определение** Множество $(\underbrace{K/I}_{\text{множество смежных классов по сложению}}, +, \cdot)$ называется факторкольцом кольца $K$ по идеалу $I$

---

**Пример** факторкольца: $(\Z, +, \cdot)$ - кольцо $K\\
(n\Z, +, \cdot)$ - идеал $I$ в $K$

Тогда факторкольцо $\Z/n\Z \cong \Z_n$ - кольцо вычетов по модулю $n$

**Замечание** $Im(\varphi)$, где $\varphi$ - гомоморфизм колец является подкольцом в $K_2$ ($\varphi: K_1 \to K_2$)

## Теорема о гомоморфизме колец

Пусть $K_1, K_2$ - два кольца. $\varphi: K_1 \to K_2$ - гомоморфизм. Тогда $K_1 / Ker(\varphi) \cong Im(\varphi)$

$\square Ker(\varphi)$ является идеалом (по лемме выше) $\implies K_1/Ker(\varphi)$ корректно определен

Рассмотрим отображение $\tau: K/Ker(\varphi) \to Im(\varphi), \tau(a + I) = \varphi(a)$. Из доказательства [теоремы о гомоморфизме групп](https://wiki.bularond.ru/ru/algebra/sexteenth_lesson) $\implies \tau$ корректно определено и является гомоморфизмом групп по сложению. Остается проверить, что $\tau$ сохроняет умножение:

$\tau((a + I) \cdot (b + I)) = \tau(a \cdot b + I) = \varphi(a \cdot b) = \varphi(a) \cdot \varphi(b) = \tau(a + I) * \tau(b + I) \implies \tau$ - это гомоморфизм колец. И т. к. $\tau$ являются биекцией (из теоремы о гомоморфизме групп), то это изоморфизм (между $K_1/Ker(\varphi)$ и $Im(\varphi)$) $\blacksquare$

---

Пусть $K[x]$ это кольцо многочленов с коэфициентами из кольца $K$ и от переменной $x$

*Замечание* Пусть $K$ - целостное кольцо и $g$ - многочлен из $K[x]$, со старцим коэфициентом обратимым в $K$. Тогда $\forall f \in K[x] \exists!$ пара $q(x), r(x) \in K[x]: f(x) = q(x) \cdot q(x) + r(x)$ 

$deg(r(x)) < deg(g(x))$

**Алгоритм Евклида** нахождения НОД$(a, b)$, где $a, b \in K$

> $
> a_n \cdot x^n + a_{n-1} \cdot x^{n-1} + \dots + a_1 \cdot x^1 + a_0 \cdot x^0 \\
> deg(f(x)) = n
> $

$a(x) = b(x) \cdot q_1(x) + r_1(x) \\
deg(r_1(x)) < deg(b(x)) \\
b = q_2 \cdot r_1 + r_2, deg r_2 < deg(r_1) \\
\dots \\
r_{k - 1} = q_k \cdot r_{k - 1} + r_k \quad deg(r_k) < deg(r_{k-1})
$

Последовательность степеней остатков состоит из неотрицательных чисел и строго убывает $\implies$ она должна оборваться. А это может быть только за счет обнуления остатка: $r_{k-1} = q_{k - 1} \cdot r_k$ (т. е. $r_{k + 1} = 0$)

Тогда НОД$(a, b) = r_k \implies$

**Утверждение** В кольце многочленов $K[x]$ ($k$ - целостное) $\forall a, b \in K[x] \exists \text{НОД}(a, b)$ и $\exists u(x), v(x) \in K[x] \\
\text{НОД}(a, b) = a(x) \cdot u(x) + b(x) \cdot v(x)$

**Определение** Взаимной простоты многочленов

Два элемента кольца (многочленов) $a(x)$ и $b(x)$ являеются взаимно простыми если $\exists u(x), v(x): a(x) \cdot u(x) + b(x) \cdot v(x) = 1$

**Определение** Пусть $P$ - поле. Характеристикой поля называется наименьшее $q \in \N: \underbrace{1 + 1 + \dots 1}_{q} = 0$ Если такого $q$ нет, то характеристика равно нулю

Обозначение: $char(P)$

*Примеры* 
1. $char(\R) = char(\mathbb{C}) = char(\mathbb{Q}) = 0$
2. $char(\Z_p) = p$

**Утверждение**: $char(p) = \begin{cases}
0, \\
p, p - \text{простое}
\end{cases}
$

$\square$ Пусть $p \not= 0 \implies p \ge 2 (1 \not=0)$

Если $p = m \cdot k$, где $1 \le m, k < p$

$0 = \underbrace{1 + \dots + 1}_{m \cdot k} = \underbrace{(1 + \dots + 1)}_m \cdot \underbrace{(1 + \dots + 1)}_k$ так как $p = M \cdot k$ минимально, то обе скобки $\not= 0 \implies m$ и $k$ - делители нуля - а из нет в поле по определению $\blacksquare$

**Определение** Пусть $P$ - поле. Рассмотрим множество рациональных функций (т. е. отношения двух многочленов) с коэфициентами из $P$ элементы этого множества это дроби вида: $\frac{f(x)}{g(x)} \\
f(x), g(x) \in P[x], g(x) \not= 0$

Обозначение: $P(x)$ - поле частных, где $P$ - это поле

*Замечание* $char(\Z_p(x)) = p$

**Определение** Если $F \subset P$, то говорят, что $P$ является расширением $F#

