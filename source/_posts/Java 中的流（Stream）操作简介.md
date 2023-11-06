---
title: Java 中的流（Stream）操作简介
date: 2023-04-28
tags: 
- Java 
- Stream 
- 函数式编程
---

时间：2023-04-27
标签： #Java #Stream #函数式编程

---

Java 8 引入了流（Stream）操作，这是一种新的抽象，允许对集合进行高效、声明式的处理。流操作主要用于对集合进行各种转换、过滤、排序等操作，使得处理数据更加简洁、易读。

流（Stream）的核心特点如下：

1. 声明式编程：流操作使用声明式编程风格，这使得您可以表达想要完成的任务，而不需要指定如何执行任务的详细步骤。

2. 无状态：流操作是无状态的，这意味着流操作不会修改底层数据结构。相反，它们通过生成新的结果来处理数据。

3. 懒加载：流操作支持懒加载，这意味着操作仅在需要结果时才会执行，从而提高性能。

4. 并行化：流操作可以自动并行化处理，这使得在多核处理器上处理大量数据更加高效。

流操作主要分为两类：

1. 中间操作（Intermediate Operations）：这些操作在 Stream 上执行，返回一个新的 Stream。这些操作是惰性的，只有在终止操作被调用时才会执行。例如：filter、map、flatMap 等。

2. 终止操作（Terminal Operations）：这些操作会终止 Stream 并生成结果。当终止操作被调用时，所有的中间操作会一次性执行。例如：collect、reduce、forEach、sum 等。

以下是一个简单的 Stream 操作示例：

```java
List<String> names = Arrays.asList("John", "Alice", "Bob", "Cathy");

// 使用 Stream 操作过滤、转换和排序名字列表
List<String> sortedNames = names.stream()
    .filter(name -> name.length() > 3)      // 过滤长度大于 3 的名字
    .map(String::toUpperCase)               // 将名字转换为大写
    .sorted()                               // 对名字进行排序
    .collect(Collectors.toList());          // 将结果收集为一个新的列表

System.out.println(sortedNames);           // 输出：[ALICE, CATHY]
```

在这个示例中，我们使用流操作对名字列表进行过滤、转换和排序。使用 Stream API，我们可以以一种更加声明式、易读的方式完成这些操作。