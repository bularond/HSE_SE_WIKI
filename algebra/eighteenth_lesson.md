---
title: 18. RSA, кольца, поля
description: 
published: 1
date: 2021-02-10T12:30:33.475Z
tags: 
editor: markdown
dateCreated: 2021-02-10T11:21:22.422Z
---

## RSA
RSA - криптографический алгоритм с открытым ключем. Применяется в TLS/SSL. Общая идея: 

1. Выбираем дла дольших простых числа $p$ и $q$ (лучше больше 2048 бит каждое)
2. Вычисляется модуль $n = p \cdot q$
3. Вычисляем фукнию Эйлера: $\varphi(n) = \varphi(p \cdot q) = (p - 1) \cdot (q - 1)$
4. Выбирается целое натуральное число $e$ (открытая экспонента) $1 < e < \varphi(n)$ и взаимнопростое с $\varphi(n)$
5. Вычисляется "секретная экспонента" $d$ - обратное к $e$ по модулю $\varphi(n)$, т. е. решение уравнения $\\x \cdot e = 1 \mod \varphi(n) \iff x \cdot e = 1 + k \cdot \varphi(n)$. Вычисляется с помощью расширенного аолгоритма Евклида
6. Пара ($e$, $n$) публикуется в виде открытого ключа RSA, а пара ($d$, $n$) - держится в секрете

Шифрование и дешифрование: 

Пусть В хочет отправить А сообщение $M$ (это всегда числа в диапозоне от $0$ до $n - 1$)

Шифрование: Берем открытый ключ А: ($e$, $n$) и сообщение $M$, тогда отправленный пакет $C = M^e \mod n$

Дешифровка: $M = C^d \mod n = M^{ed} \mod n = M^{1 + k \cdot \varphi(n)} \mod n = \\
= M \cdot (M^{\varphi(n)})^k \mod n = M \cdot 1^k \mod n = M$

## Кольца

**Определения**: Пусть $K \not= \varnothing$ - множество, на котором заданы 2 бинарные операции: "$+$", "$\cdot$" такие, что:

1. $(K, +)$ - абелева группа
2. $(K, \cdot)$ - полугруппа
3. Уможение дистрибутивно по сложению:

$
\forall a, b, c \in K \\
(a + b) \cdot c = a \cdot c + b \cdot c \\
c \cdot (a + b) = c \cdot a + c \cdot b
$

Тогда $(K, +, \cdot)$ - кольцо

*Замечание* $(K, +)$ аддитивная группа кольца

$(K, \cdot)$ - мультипликативная полугруппа кольца

**Определение** Подмножество $L \subseteq K$ называется подкольцом, если: $\forall x, y \in L$

1. $x - y \in L$ (т. е. $L$ - подгруппа аддитивной группы кольца)
2. $x \cdot y \in L$ т. е. множество $L$ замкнуто относительно умножения

*Примеры*

1. Числовые кольца: $(\Z, +, \cdot)$ - кольцо целых чисел ($\Z \subset \mathbb{Q} \subset \R \subset \mathbb{C}$ - цепочка числовых подколец)
2. Полное матричное кольцо: $(M_n(\R), +, \cdot)$ (где $M_n(\R)$ - квадратные матрицы $n \times n$ с вещественными коэфициентами, "$+$" - сложение матриц, "$\cdot$" - умножение матриц)

**Определение** Если $(K, \cdot)$ - моноид, то говорят, что $(K, +, \cdot)$ - кольцо с еденицей

3. Кольцо вычетов. Пусть $m \in \N m > 1$. Тогда множество $m\Z \sub \Z$ - подкольцо в $\Z$. $\Z$ разбивается на классы чисел сравнимых по модулю $m$ (т. е. имеющих одинаковый остаток при делении на $m$). Можно складывать и умножать эти классы.

Пример: $(\Z_4, +, \cdot)$

$$
\begin{array}{c|c|c|c|c|}
+ & 0 & 1 & 2 & 3 \\
\hline
0 & 0 & 1 & 2 & 3 \\
\hline
1 & 1 & 2 & 4 & 0 \\
\hline
2 & 2 & 3 & 0 & 1 \\
\hline
3 & 3 & 0 & 1 & 2 \\
\hline
\end{array}
$$

$$
\begin{array}{c|c|c|c|c|}
\cdot & 0 & 1 & 2 & 3 \\
\hline
0 & 0 & 0 & 0 & 0 \\
\hline
1 & 0 & 1 & 2 & 3 \\
\hline
2 & 0 & 2 & 0 & 2 \\
\hline
3 & 0 & 3 & 2 & 1 \\
\hline
\end{array}
$$

**Определение** Если $a \cdot b = 0$ при $a \not= 0$ и $b \not= 0$ в кольце $K$, $a$ называется левым, а $b$ правим делителем нуля

**Определение** Если $\forall x, y \in K: x \cdot y = y \cdot x$  (т. е. умножение коммутативно) то коцльцо $(K, +, \cdot)$ называется коммутативным

**Определение** Коммутативное кольцо с $1 \not= 0$ и без делителей нуля называется целостным кольцом (областью целостности)

**Определение** $\varphi: K_1 \to K_2$ - гомоморфизм колец: $\forall a, b \in K_1:$

1. $\varphi(a + b) = \varphi(a) \oplus \varphi(b)$
2. $\varphi(a \cdot b) = \varphi(a) * \varphi(b)$

**Определение** Подмножество $I$ кольца $K$ называется (двусторонним) идеалом, если оно:

1. Является подгруппой $(K, +)$ по сложению
2. $\forall a \in I \forall r \in K: r \cdot a \in I \land a \cdot r \in I$

*Пример* $m\Z$ - мдеал в кольце $\Z$. $C$ подгрпуппа в $(\Z, +)$. $m \cdot k$ - элемент $m\Z$ и $r = n$ - произвольное целое $\implies a \cdot r$ и $r \cdot a$ здесь $m \cdot k \cdot n \in m\Z$

**Определение** Пусть $K$ - коммутативное кольцо с единицей. Тогда $K[x]$ - кольцо многочленов от $x$ с коэфициентами из $K$. Операции: сложение многочленов, умножение многочленов

*Пример* $\R[x]$ - множество всех многочленов с вещественными коэфициентами. Это кольцо

*Пример* идеала: $I = \{(x^2 + 1) \cdot f(x) | f(x) \in \R[x]\}$

**Определение** Идеал $I$ называется главным, если $\exists a \in K: I = \{r \cdot a | r \in K\}$. Говорят, что идеал $I$ порожден $a$

*Замечание* В $\Z$ все идеалы главные

**Определение** Элемент коммутативного кольца c "$1$" назвыается обратимым, если существует элемент $a^{-1}$: $a \cdot a^{-1} = a^{-1} \cdot a = 1$

**Утверждение** Все обратимые элементы кольца $K$ (с еденицей) образуют группу $U(K)$ по умножениею - это называется мультипликативная группа кольца

**Определение** Поле $P$ - это коммутативное кольцо с еденицей ($1 \not= 0$) в которой каждый элемент кроме элемент $a \not= 0$ обратим

*Пример* $\mathbb{Q}, \R, \mathbb{C}$ - поля

**Определение** Подполе - это подмножество поля, которое само является полем относительно тех же операций

*Пример* $\mathbb{Q} \subset \R \subset \mathbb{C} {}$

*Пример* $\Z_p$, где $p$ - простое, тоже является полем

**Лемма** $Ker(\varphi)$, где $\varphi$ - гомоморфизм колец, всегда являетя идеалом в кольце $K_1$ ($\varphi: K_1 \to K_2$)