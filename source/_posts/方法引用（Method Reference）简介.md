---
title: 方法引用（Method Reference）简介
date: 2023-04-28
tags: 
- Java 
- 方法引用 
- Lambda表达式
---

时间：2023-04-27
标签： #Java #方法引用 #Lambda表达式

---

方法引用（Method Reference）是 Java 8 引入的一种简化 lambda 表达式的语法。它允许您直接引用现有方法（静态方法、实例方法、构造函数）而无需显式地编写 lambda 表达式。方法引用通常用在函数式接口的实现中，例如在流（Stream）操作或其他高阶函数中。

方法引用有四种类型：

1. 静态方法引用：当引用的方法是一个静态方法时，使用类名:: 方法名的形式表示。例如，`Integer::parseInt` 是 `Integer` 类的 `parseInt` 静态方法的引用。

```java
Function<String, Integer> parseInt = Integer::parseInt;
```

2. 实例方法引用：当引用的方法是一个实例方法时，使用对象实例:: 方法名的形式表示。例如，`str::toUpperCase` 是 `str` 实例的 `toUpperCase` 方法的引用。

```java
String str = "hello";
Supplier<String> toUpperCase = str::toUpperCase;
```

3. 类的实例方法引用：当引用的方法是一个实例方法，但需要用类名引用时，使用类名:: 方法名的形式表示。这种情况下，第一个参数会成为方法的调用者。例如，`String::compareToIgnoreCase` 是 `String` 类的 `compareToIgnoreCase` 实例方法的引用。

```java
Comparator<String> ignoreCaseComparator = String::compareToIgnoreCase;
```

4. 构造函数引用：当引用的方法是一个类的构造函数时，使用类名:: new 的形式表示。例如，`ArrayList::new` 是 `ArrayList` 类的构造函数引用。

```java
Supplier<ArrayList<String>> arrayListSupplier = ArrayList::new;
```

方法引用提供了一种更简洁、易读的方式来表示 lambda 表达式，尤其是在函数签名与现有方法签名完全匹配的情况下。

在没有方法引用的情况下，我们可以使用 Lambda 表达式来实现上述示例。这里是原始示例（使用方法引用）：

```java
list.stream().map(String::toUpperCase).collect(Collectors.toList());
```

在不使用方法引用的情况下，我们可以将其改写为：

```java
list.stream().map(str -> str.toUpperCase()).collect(Collectors.toList());
```

这里，我们使用了 Lambda 表达式 `str -> str.toUpperCase()` 来替换原始的方法引用 `String::toUpperCase`。这个 Lambda 表达式接收一个字符串参数 `str`，并调用其 `toUpperCase()` 方法将其转换为大写。虽然这种写法相对于方法引用略显冗长，但在不支持方法引用的情况下，它仍然是一种简洁、易读的替代方案。