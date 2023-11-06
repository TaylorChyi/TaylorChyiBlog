---
title: char 与 character 有什么区别 java
date: 2023-04-28
tags: 
- java 
- char 
- character 
- 封装类
---

时间：2023-04-24
标签： #java #char #character #封装类

---

在 Java 编程语言中，"char" 和 "character" 有一些不同之处，主要体现在以下方面：

1. 数据类型：
char：`char` 是 Java 的一种原始数据类型（primitive data type），用于表示单个 Unicode 字符。它的大小为 16 位（2 字节），可以表示从 0 到 65,535 之间的任何值。例如，定义一个 `char` 类型变量的语法如下：

```java
char letter = 'A';
```

Character：`Character` 是 Java 的一个封装类（wrapper class），它对 `char` 数据类型进行了封装，提供了一系列实用方法，例如字符分类、转换大小写等。例如，使用 `Character` 类的语法如下：

```java
Character letter = new Character('A');
```

2. 功能和方法：
char：`char` 类型本身没有任何方法，只能存储和表示单个字符。
Character：`Character` 类提供了许多用于操作字符的方法，如 `isLetter()`, `isDigit()`, `toUpperCase()`, `toLowerCase()` 等。

总之，`char` 是 Java 中的原始数据类型，用于存储单个字符，而 `Character` 是一个封装类，为字符操作提供了更丰富的方法。在实际编程中，根据需求选择使用哪种类型。//