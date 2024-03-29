---
title: 3. Теория групп
description: 
published: 1
date: 2021-03-18T16:47:37.679Z
tags: 
editor: markdown
dateCreated: 2021-03-18T11:27:25.555Z
---

# Определения и доказательства
## 1. Сформулируйте и докажите утверждение о том, какими могут быть подгруппы группы целых чисел по сложению
Подгруппы целых чисел по сложению

$\Z = <1>$

Подгруппы целых исел по сложению имеют вид $n\Z$, т. е. все элементы делящиеся на $n$, где $n \in \N$

$3\Z = \{\dots, -6, -3, 0, 3, 6, 9, \dots\} {}$

Любая подгруппа циклической группы будет циклической группой, рассмотрим образующие элементы $k$

$\= \{n \cdot k | n \in \Z \} {}$

W. I. P.

## 2. Сформулируйте и докажите теорему Лагранжа (включая две леммы)
**Лемма 1** $\forall g_1, g_2 \in G$ либо $g_1 H = g_2 H$ либо $g_1 H \cap g_2 H = \varnothing$

$\square$ Если $g_1 H \cap g_2 H \not= \varnothing$, то $\exists h_1, h_2 \in H: g_1 \cdot h_1 = g_2 \cdot h_2 \implies \\
\implies g_1 = g_2 \cdot \underbrace{h_2 \cdot h_1^{-1}}_{\in H} 
\implies g_1 H = g_2 \cdot \underbrace{h_2 \cdot h_1^{-1} H}_{\text{лежит в H}} = g_2 H$. 
Аналогично есть обратное включение $\implies g_1 H = g_2 H \ \blacksquare$

**Лемма 2** $|gH| = |H|, \forall g \in G$ (и для любой конечной подгруппы $H$)

$\square\ gH = \{g \cdot h | h \in H\} {}$
$|gH| \le |H|$
$|gH|$ может быть $\ne |H|$ только если $\exists h_1,h_2: gh_1 = gh_2 \implies g^{-1} g h_1 = g^{-1} g h_2 \implies h_1 = h_2$ $-$ противоречие $\implies$ совпадений нет $\blacksquare$

**Теорема** Пусть $G$ - конечная группа и $H \subseteq G$ - любая ее подгруппа. Тогда $|G| = |H| \cdot |G:H|$

$\square$ Любой элемент группы ($g$) лежит в своем левом смежном классе по $H$ ($gH$), смежные классы не пересекаются (по лемме 1) и любой из них содержит по $|H|$ (по лемме 2) $\blacksquare$

## 3. Докажите, что гомоморфизм инъективен тогда и только тогда, когда его ядро тривиально
$f$ - инъективно $\iff Ker(f) = \{e\} {}$

$\square G / Ker(f) \cong Im(f)$
$|G| \le |Im(f)|$ -- т. к. $f$ - функционально
$f$ - не инъективно если $|G| > |Im(f)|$
$|Im(f) = |G / Ker(f)| = |G:Ker(f)| = \frac{|G|}{|Ker(f)|} {}$
$|G| > \frac{|G|}{|Ker(f)|} \implies |Ker(f)| > 1$
если $|Ker(f)| = 1 \implies Ker(f) = \{e\} {}$
$|G/\{e\} = |G| = |Im(f)| \blacksquare$

## 4. Сформулируйте и докажите критерий нормальности подгруппы, использующий сопряжение
> **Опредление** Подгруппа $H$ группы $G$ назвывается **нормальной**, если $gH = Hg$, $\forall g \in G$
> Обозначение: $H \lhd G$ (направление треугольничка важно)

$H \lhd G \iff \forall g \in G: gHg^{-1} = H$

$\square$ $(\implies) gHg^{-1} = Hgg^{-1} = He = H$

$(\impliedby)gHg^{-1} = H | \cdot g$
$gHg^{-1}g = Hg$
$gH = Hg \blacksquare$


## 5. Сформулируйте и докажите критерий нормальности подгруппы, использующий понятие ядра гомоморфизма
**Критерий** $H \lhd G \iff \exists (f: G \to P): Ker(f) = H, f$ -- гомоморфизм

$\square (\impliedby)$
Хотим: $\forall z \in Ker(f) \forall g \in G: g^{-1}zg \in Ker(f)$
$Ker(g^{-1}zg) = f(g^{-1})e_Pf(g) = f(g^{-1}) f(g) = f(g^{-1}g) = f(e_G) = e_P \implies$
$\implies g^{-1}zg \in Ker(f) \implies g^{-1}Ker(f)g = Ker(f) \implies Ker(f) \lhd G$

$(\implies)$
Возмем $f: G \to G/H, f(a) = aH$
$\forall h \in H: f(h) = hH = H (=e) \implies H \subseteq Ker(f)$
$\nexists h \in G \smallsetminus H: f(h) = H$, т. к. $hH$ содержит $he = h, h \notin H$, значит класс другой $\implies$
$\implies H = Ker(f) \blacksquare$

## 6. Сформулируйте и докажите теорему о гомоморфизме групп
Пусть $f: G \to F$ -- гомоморфизм, тогда
$G / Ker(f) \cong Im(f)$

## 7. Докажите, что центр группы является её нормальной подгруппой

## 8. Сформулируйте и докажите утверждение о том, чему изоморфна факторгруппа группы по её центру

## 9. Сформулируйте и докажите теорему Кэли

## 10. Докажите, что характеристика поля может быть либо простым числом, либо нулем

## 11. Сформулируйте и докажите утверждение о том, каким будет простое подполе в зависимости от характери-стики

## 12. Сформулируйте и докажите критерий того, что кольцо вычетов по модулюnявляется полем

## 13. Докажите, что ядро гомоморфизма колец является идеалом

## 14. Сформулируйте и докажите утверждение о том, когда факторколько кольца многочленов над полем самоявляется полем

## 15. Выпишите и докажите формулу для описания изменения координат вектора при изменении базиса

## 16. Выпишите формулу для преобразования матрицы билинейной формы при замене базиса и докажите её

## 17. Выпишите формулу для преобразования матрицы линейного отображения при замене базиса и докажитееё