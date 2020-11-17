---
title: Runtime errors
description: 
published: 1
date: 2020-11-17T12:46:14.147Z
tags: 
editor: undefined
dateCreated: 2020-11-05T19:57:48.877Z
---

# RE в системе Яндекс.Контест

> Эта страница меняется к лучшему, как и наши контесты. 
Если у Вас возникла ошибка RE1, теперь Вы можете понять почему именно произошла ошибка, открыв отчёт тестирования на примерах.

## Список доступных сборок
Теперь успешно компилируются все проекты на .Net Core 3.1, которые реализованы с использованием следующих сборок:

> `mscorlib.dll`
{.is-success}

> `netstandard.dll`
{.is-success}

> `System.dll`
{.is-success}

> `System.Core.dll`
{.is-success}

> `System.Console.dll`
{.is-success}

> `System.Runtime.dll`
{.is-success}

> `System.Runtime.Extensions.dll`
{.is-success}

> `System.Collections.dll`
{.is-success}

> `System.Linq.dll`
{.is-success}

Если Вам не хватает какой-то сборки, то следует написать об этом в тг @nchuykin, и мы добавим её или расскажем как можно решить задачу без неё.

## Как понять в какой сборке находится класс, который я хочу использовать?
Для этого достаточно открыть статью с описанием этого класса на docs.microsoft.com, переключить версию языка на .Net Core 3.1 и посмотреть название сборки.
![assembly_docs_microsoft.png](/assembly_docs_microsoft.png)

## Как посмотреть отчёт об ошибке
![report1.png](/report1.png)

## Как выглядит ошибка компиляции
![report2.png](/report2.png)

> Если кроме строки `Makefile:7: recipe for target 'run' failed` в выводе программы ничего нет, значит в Вашей программе произошла ошибка исполнения, к примеру, выход за границы массива.
