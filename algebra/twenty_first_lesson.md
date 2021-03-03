---
title: 21. Линейные пространтсва, базисы, подпространтсвап
description: 
published: 1
date: 2021-03-03T11:31:31.462Z
tags: 
editor: markdown
dateCreated: 2021-03-03T11:30:51.619Z
---

## Линейные (векторные) пространства

**Замечание** Элементы линейного пространства называются векторами

*Примеры*:

0. $V_3$ - геометрические векторы
1. $F^n$, где $F$ - поле

$F^n = \{(x_1, \dots, x_n)^T | x_i \in F\}$, чаще всего $R^n$ операции заданны покомпонентно

$
x = \begin{pmatrix}
x_1 \\
\dots \\
x_n
\end{pmatrix}, 
y = \begin{pmatrix}
y_1 \\
\dots \\
y_n
\end{pmatrix} \implies 
x + y = \begin{pmatrix}
x_1 + y_1 \\
\dots \\
x_n + y_n
\end{pmatrix}
$

$F^n$ - арифметическое пространство "размерности" $n$

2. $F^\infin = \{(x_1, \dots, x_n, \dots) | x_i \in F, i \in \N\}$ - пространство числовых последовательностей
3. Пусть $C[a, b]$ - множество функций непрерывных на отрезке $[a, b]$

Операции: $\forall x \in [a, b]: (f + g)(x) = g(x) + f(x)$

$\forall x \in [a, b], \lambda \in \R: (\lambda f)(x) = \lambda f(x)$

4. Пусть $A \cdot x = 0$ - однородная СЛАУ. $L$ - множее решений. Тогда $\forall x, y \in L: x + y \in L$ и $\lambda x \in L \implies x + y \in L$ и $\lambda x \in L \implies L$ - линейное пространство

## Базис и размерность линейного пространтсва

**Определение** Базисом линейного пространства $V$ называется упорядочнный набор векторов $b_1, \dots, b_n$ такой, что:

1. $b_1, \dots, b_n$ - линейно-независимыми
2. Любой вектор из $V$ представляется в виде линейной комбинации $b_1, \dots, b_n$ т. е.: $\forall x \in V: x = x_1 b_1 + \dots + x_n b_n$. При этом $x_1, \dots, x_n$ называется координатами вектора $x$ в базисе $b_1, \dots, b_n$

**Утверждение** Если $b_1, \dots, b_n$ - базис, то $\forall x \in V$ представляется в вида линейной коминации базисных векторов есдинственным образом (т. е. координаты вектора в базисе определены однозначно)

$\square$ Пусть $x = x_1 b_1 + \dots + x_n b_n = x_1' b_1 + \dots x_n' b_n \implies (x_1 - x_1')b_1 + \dots + (x_n - x_n')b_n = 0$

Векторы $b_1, \dots, b_n$ л. н. з. по определениею базиса и $\implies \begin{cases}
x_1 - x_1' = 0 \\
\dots \\
x_n - x_n' = 0
\end{cases}$ т. е. разложение единственно

**Замечание** При сложении векторов из координаты складываются, а при умножении на число - умножеются на число ($\lambda x = \lambda(x_1 b_1 + \dots + x_n b_n) = (\lambda x_1) b_1 + \dots + (\lambda x_n) b_n$)

**Определение** максимальное количество л. н. з. векторов в данном линейном пространстве $V$ называется размерностью этого линейного пространства

*Обозначение*: $\text{dim}(V)$

1. $dim(V_3) = 3$
2. $dim(\R^n) = n$

**Замечание** рассмотрим линейное пространство $V$ и фиксируем в нем базис $b_1, \dots, b_n$. Тогда линейное пространство $V$ изоморфно арифметическому линейному пространосву $F^n$ (если линейное проство над полем $F$)

$
x \xrightarrow{\varphi} 
\begin{pmatrix}
x_1 \\
\dots \\
x_n
\end{pmatrix}
$ - это изомомрфизм. Оно взаимно однородное и сохраняет сложение и умножение на число.

## Перехов к новому базису

Пусть $L$ -- $n$-мерное линейное пространство $\mathcal{A} = \{a_1, \dots, a_n\}$ и $\mathcal{B} = \mathcal{B} = \{b_1, \dots, b_n\}$ - два базиса в $L$.

Разложим векторы 2-го базиса $\mathcal{B}$ по базису $\mathcal{A}$:

$
\begin{cases}
b_1 = t_{11} a_1 + t_{21} a_2 + \dots + t_{n1} a_n \\
\dots \\
b_n = t_{1n} a_1 + t_{2n} a_2 + \dots + t_{nn} a_n
\end{cases} (1)
$

**Определение** Матрицей перехода от базиса $\mathcal{A}$ к базису $\mathcal{B}$ называется матрица:

$
T_{\mathcal{A} \xrightarrow{} \mathcal{B}} = \begin{pmatrix}
t_{11} & \dots & t_{1n} \\
\dots & & \dots \\
t_{n1} & & t_{nn}
\end{pmatrix}
$

$
(1) \iff (b_1, \dots, b_n)_{1 \times n} = (a_1, \dots, a_n) \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \iff \\
\iff b = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}}
$ - матричная форма записи определения матрицы перехода

**Замечание** В любом базисе данного линейного пространства всегда одинаковое количество векторов и оно $= dim(V)$ - размерности пространства

**Замечание** Матрица перехода всегда невыраждена т. к. векторы $b_i$ - л. н. з. (по определению базиса) $\implies$ столбцы матрицы перехода тоже линейно независимы (т. к. есть изоморфизм с $F^n$) т. е. столбцы координат $b_1, \dots, b_n$ имеют ранг $n \implies \det(T_{\mathcal{A} \xrightarrow{} \mathcal{B}}) \not= 0$

**Утверждение** Пусть $x \in L$, $\mathcal{A}$ и $\mathcal{B}$ - базисы в $L$.

$
x^a = \begin{pmatrix}
\end{pmatrix}
x_1^a \\
\dots \\
x_n^a
$ - столбец координат вектора $x$ в базисе $\mathcal{A}$

$
x^b = \begin{pmatrix}
\end{pmatrix}
x_1^b \\
\dots \\
x_n^b
$ - столбец координат вектора $x$ в базисе $\mathcal{B}$

Тогда $x_b = T_{\mathcal{A} \xrightarrow{} \mathcal{B}}^{-1} x^a \iff x' = T^{-1} x$

$\square$ Докажем, что $x^a = T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \cdot x^b$ (из невырожденности). Матрицы перехода будет следовать нужная формула

$
x = a \cdot x^a = (a_1, \dots, a_n) \cdot \begin{pmatrix}
x_1^a \\
\dots \\
x_n^a
\end{pmatrix} = x_1^a \cdot a_1 + \dots + x_n^a \cdot a_n = b\cdot x^b \\
b = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \xrightarrow{} a \cdot x^a = b  \cdot x^b \\
a \cdot x^a = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \cdot x^b
$ т. к. разложение по столбцу единственно 

$x_b = T_{\mathcal{A} \xrightarrow{} \mathcal{B}}^{-1} x^a \iff x' = T^{-1} x \blacksquare$

**Замечание** $T_{\mathcal{B} \xrightarrow{} \mathcal{A}} = T_{\mathcal{A} \xrightarrow{} \mathcal{B}}^{-1} {}$

**Замечание** $x^b = T_{\mathcal{B} \xrightarrow{} \mathcal{A}} \cdot x^a$

**Утверждение** Пусть $\mathcal{A} = \{a_1, \dots, a_n\}$, $\mathcal{B} = \{b_1, \dots, b_n\}$ и $\mathcal{C} = \{c_1, \dots, c_n\}$ - базисы

Тогда $T_{\mathcal{A} \xrightarrow{} \mathcal{C}} = T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \cdot T_{\mathcal{B} \xrightarrow{} \mathcal{C}}$

$
\square c = b \cdot T_{\mathcal{B} \xrightarrow{} \mathcal{C}} \\
b = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \\
c = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{C}} \\
c = a \cdot T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \cdot T_{\mathcal{B} \xrightarrow{} \mathcal{C}}
$

Сравним и учтем, что разложение по базису единственно $\implies T_{\mathcal{A} \xrightarrow{} \mathcal{C}} = T_{\mathcal{A} \xrightarrow{} \mathcal{B}} \cdot T_{\mathcal{B} \xrightarrow{} \mathcal{C}} \blacksquare$

## Подпространтсва

**Определение** Подмножество $W$ векторного пространтсва $V$ называется подпространством, если оно само является пространством оносительно опрераций в $V$

**Замечание** Для проверки того, что $W$ является подпространостом достаточно проверять замкнутость оносительно сложения и умножения на число:

$
\forall x, y \in W, \forall \lambda \in F \implies x + y \in W, \lambda \cdot x \in W
$

*Примеры*:
1. $P[a, b]$ - многочлены определены на трезке $[a, b]$ - подпространство в $C[a, b]$
2. Пространство решений однородной СЛАУ $Ax = 0$ с $n$ незивестнами - подпространство в $\R^n (A \in M_n(\R))$
2. В любом линейном пространтсе есть подпространтво $\{0\}$

**Опредление** Множество $L(a_1, \dots, a_k) = \{\lambda_1 a_1 + \dots + \lambda_k a_k | \lambda_i \in F\}$ - множество всех линейных комбинаций векторов $a_1, \dots, a_k$ называется линейной оболочкой набора $a_1, \dots, a_k$

**Утверждения** $\forall a_1, \dots, a_k \in V \quad L(a_1, \dots, a_k)$ всегда является подпространством $k \in \N$

*Пример* В $V_3$ с базисом $i, j, k$. $L(i, j)$ - плоскость $Oxy$

**Определение** Рангом системы векторов $a_1, \dots, a_k$ в линеном пространстве называется размерность из линейными оболочками

$
Rg(a_1, \dots, a_k) = dim(L(a_1, \dots, a_k))
$
