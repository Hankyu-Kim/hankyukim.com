---
title: "return VS yield"
publishDate: "10 Jun 2024"
description: "--------------------------------------------------"
tags: ["return", "yield", "C#"]
---

Most of programming language, functions normally hands over the value using ***return*** keyword. But using ***yield*** keyword can bring the value very different way.

The first noticeable difference is that when using the ***return*** keyword, the result value is provided only once, and the ***yield*** keyword provides the result value divided by multiple times.

<br>

```csharp
using System;
using System.Collections.Generic;

class Program
{
static IEnumerable GetNumber()
{
yield return 10;
yield return 20;
yield return 30;
}

static void Main(string[] args)
{
foreach (int num in GetNumber())
{
Console.WriteLine(num);
}
}
}
```