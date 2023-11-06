---
title: Lambda 表达式简介
date: 2023-04-28
tags: 
- Java 
- Lambda表达式 
- 函数式编程
---

时间：2023-04-27
标签： #Java #Lambda表达式 #函数式编程

---

Lambda 表达式（Lambda Expression）是 Java 8 引入的一种新的编程构造，用于表示一种简洁、匿名的函数表达式。它允许您将函数（方法）作为参数传递给其他方法，或者作为返回值。Lambda 表达式在函数式编程中尤为重要，因为它们提供了一种更简洁、易读的方式来表示代码中的行为。

关于 Lambda 的名字来源于计算机科学中的 Lambda 演算（Lambda Calculus），这是一种数学形式化系统，用于研究函数抽象、函数应用等概念。Lambda 演算在计算机科学中具有重要地位，因为它为理解编程语言的基本结构和原理提供了理论基础。

在 Java 中，Lambda 表达式的语法如下：

```java
(parameters) -> { body }
```

其中：

- `parameters`：表示输入参数列表，可以是零个、一个或多个参数。如果只有一个参数，可以省略括号。
- `->`：箭头符号，表示将参数传递给函数体。
- `body`：表示函数体，包含执行的代码。如果函数体只有一条语句，可以省略大括号。

Lambda 表达式的一个典型应用场景是 Java 中的函数式接口。函数式接口是只包含一个抽象方法的接口，如 Runnable、Comparator 和 Callable 等。使用 Lambda 表达式，可以简洁地表示这些接口的实现，例如：

```java
Runnable r = () -> System.out.println("Hello, Lambda!");
```

这里，Lambda 表达式 `() -> System.out.println("Hello, Lambda!");` 表示一个没有参数且没有返回值的函数，实现了 Runnable 接口的 `run` 方法。使用 Lambda 表达式可以使代码更简洁、易读，尤其是在处理集合、流（Stream）操作或其他高阶函数时。