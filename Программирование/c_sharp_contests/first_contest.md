---
title: 1 Контест
description: 
published: 1
date: 2020-11-17T13:49:15.345Z
tags: 
editor: undefined
dateCreated: 2020-11-12T12:09:33.073Z
---

# Первый контест

## 1 Задание
``` C#
using System;

namespace Task1
{
    internal static class Program
    {
        private const int PrintCount = 3;

        private static void Main(string[] args)
        {
            var input = Console.ReadLine();

            for (var i = 0; i < PrintCount; i++)
                Console.WriteLine(input);
        }
    }
}
```

## 2 Задание

``` C#
using System;

namespace Task2
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            int a, b;
            
            if (!ReadNumber(out a))
                return;

            if (!ReadNumber(out b))
                return;

            Console.WriteLine(a - b);
        }

        private static bool ReadNumber(out int number)
        {
            var input = Console.ReadLine();
            if (int.TryParse(input, out number))
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 3 Задание

``` C#
using System;

namespace Task3
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            int a;
            
            if (!ReadNonNegativeNumber(out a))
                return;
            
            Console.WriteLine(a % 10);
        }

        private static bool ReadNonNegativeNumber(out int number)
        {
            var input = Console.ReadLine();
            if (int.TryParse(input, out number) && number >= 0)
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 4 Задание

``` C#
using System;

namespace Task4
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            int a, b;

            if (!ReadNumber(out a))
                return;

            if (!ReadNumber(out b))
                return;

            Console.WriteLine(a > b ? "First" : a < b ? "Second" : "Equal");
        }

        private static bool ReadNumber(out int number)
        {
            var input = Console.ReadLine();
            if (int.TryParse(input, out number))
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 5 Задание

``` C#
using System;

namespace Task5
{
    internal static class Program
    {
        // Value must be even
        private const int NumberLength = 4;

        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            int number;

            var lowerLimit = Math.Pow(10, NumberLength - 1);
            var upperLimit = Math.Pow(10, NumberLength) - 1;

            var input = Console.ReadLine();
            if (input == null || !int.TryParse(input, out number) || number < lowerLimit || number > upperLimit)
            {
                Console.WriteLine("Incorrect input");
                return;
            }

            var result = true;
            for (var i = 0; i < NumberLength / 2; i++)
            {
                if (input[i] == input[NumberLength - i - 1])
                    continue;

     
           result = false;
                break;
            }

            // We only need "True" and "False" output
            Console.WriteLine(result ? "True" : "False");
        }
    }
}
```

## 6 Задание

``` C#
using System;

namespace Task6
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            double a, b;

            if (!ReadPositiveDouble(out a))
                return;

            if (!ReadPositiveDouble(out b))
                return;

            Console.WriteLine("{0:F5}", Math.Sqrt(a * a + b * b));
        }

        private static bool ReadPositiveDouble(out double number)
        {
            var input = Console.ReadLine();
            if (double.TryParse(input, out number) && number > 0)
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 7 Задание

``` C#
using System;

namespace Task7
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            double a;

            if (!ReadNonNegativeDouble(out a))
                return;

            Console.WriteLine((int) (a * 10) % 10);
        }

        private static bool ReadNonNegativeDouble(out double number)
        {
            var input = Console.ReadLine();
            if (double.TryParse(input, out number) && number >= 0)
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 8 Задание

``` C#
using System;

namespace Task8
{
    internal static class Program
    {
        private const char LowerAlphabetLimit = 'a';
        private const char UpperAlphabetLimit = 'z';

        private static void Main(string[] args)
        {
            var input = Console.ReadLine();
            if (input == null || input.Length > 1 || input[0] < LowerAlphabetLimit || input[0] > UpperAlphabetLimit)
            {
                Console.WriteLine("Incorrect input");
                return;
            }
            
            Console.WriteLine(input[0] - LowerAlphabetLimit + 1);
        }
    }
}
```

## 9 Задание

``` C#
using System;

namespace Task9
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            double a;

            if (!ReadDouble(out a))
                return;

            var decimalA = Math.Truncate(a);

            // ReSharper disable once CompareOfFloatsByEqualityOperator
            if (Math.Abs(a - decimalA) == 0.5)
                Console.WriteLine(decimalA % 2 == 0 ? (decimalA > 0 ? decimalA + 1 : decimalA - 1) : decimalA);
            else
                Console.WriteLine((int) Math.Round(a));
        }

        private static bool ReadDouble(out double number)
        {
            var input = Console.ReadLine();
            if (double.TryParse(input, out number))
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```

## 10 Задание

``` C#
using System;

namespace Task10
{
    internal static class Program
    {
        private static void Main(string[] args)
        {
            // Contest compiler doesn't support "out var"
            double x, y;

            if (!ReadDouble(out x))
                return;

            if (!ReadDouble(out y))
                return;

            var sum = x * x + y * y;

            // We only need "True" and "False" output
            Console.WriteLine(sum >= 1 && sum <= 2 ? "True" : "False");
        }

        private static bool ReadDouble(out double number)
        {
            var input = Console.ReadLine();
            if (double.TryParse(input, out number))
                return true;

            Console.WriteLine("Incorrect input");
            return false;
        }
    }
}
```