---
title: java. Util. Function.* 介绍
date: 2023-04-28
tags: 
- Java 
- FunctionalInterfaces 
- javautilFunction
---

时间：2023-04-27
标签： #Java #FunctionalInterfaces #javautilFunction

---

Java. Util. Function 包是 Java 8 引入的一个功能性接口（Functional Interface）包，它包含了一组常用的功能性接口，主要用于支持 Lambda 表达式和方法引用等函数式编程特性。这些接口主要可以分为以下几类：

1. Function<T, R>
   - Function 接口表示一个接受一个参数并返回结果的函数。它有一个抽象方法 apply (T t)，用于将此函数应用于给定的参数。
   - 示例：Function<Integer, String> intToString = i -> Integer.ToString (i);

2. Consumer<T>
   - Consumer 接口表示一个接受一个输入参数且无返回结果的操作。它有一个抽象方法 accept (T t)，用于执行有关参数的操作。
   - 示例：Consumer<String> printer = s -> System.Out.Println (s);

3. Predicate<T>
   - Predicate 接口表示一个接受一个参数并返回一个布尔值结果的谓词。它有一个抽象方法 test (T t)，用于根据给定的参数计算布尔值结果。
   - 示例：Predicate<Integer> isEven = i -> i % 2 == 0;

4. Supplier<T>
   - Supplier 接口表示一个无输入参数且返回一个结果的供应商。它有一个抽象方法 get ()，用于返回结果。
   - 示例：Supplier<Double> randomDouble = () -> Math.Random ();

5. BiFunction<T, U, R>
   - BiFunction 接口表示一个接受两个参数并返回一个结果的函数。它有一个抽象方法 apply (T t, U u)，用于将此函数应用于给定的参数。
   - 示例：BiFunction<Integer, Integer, Integer> add = (a, b) -> a + b;

6. UnaryOperator<T>
   - UnaryOperator 接口表示一个接受一个参数并返回相同类型结果的操作。它继承了 Function<T, T> 接口。
   - 示例：UnaryOperator<Integer> square = x -> x * x;

7. BinaryOperator<T>
   - BinaryOperator 接口表示一个接受两个相同类型参数并返回相同类型结果的操作。它继承了 BiFunction<T, T, T> 接口。
   - 示例：BinaryOperator<Integer> multiply = (x, y) -> x * y;

这些功能性接口的主要目的是提供一组基本的函数签名，以支持 Java 中的函数式编程。它们可以与 Lambda 表达式、方法引用和 Stream API 一起使用，以实现更简洁、易读的代码。