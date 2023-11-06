---
title: CharSequence 与 String 的区别及作用
date: 2023-04-28
tags: 
- Java 
- CharSequence 
- String
---

时间：2023-04-28
标签： #Java #CharSequence #String

---

**CharSequence：**

CharSequence 是一个接口，它定义了一系列字符的通用只读访问方法。CharSequence 提供了对字符序列进行操作的统一接口，使得代码更具有通用性。Java 中的很多类实现了 CharSequence 接口，例如 String、StringBuilder 和 StringBuffer 等。

主要作用：CharSequence 接口的主要作用是为不同类型的字符序列提供一个统一的访问方式，便于编写更具有通用性的代码。

**String：**

String 是一个类，代表不可变的字符序列。当一个 String 对象被创建后，它的内容是不可更改的。由于 String 的不可变性，它在 Java 中被广泛用作字符串处理的基本类型。

主要作用：String 类的主要作用是表示和处理不可变的字符序列，例如存储文本、拼接字符串、查找子字符串等。

**区别：**

1. CharSequence 是一个接口，而 String 是一个实现了 CharSequence 接口的具体类。
2. CharSequence 接口定义了通用的只读字符序列访问方法，而 String 类提供了更多具体的操作方法，例如字符串拼接、替换、查找等。
3. String 对象的内容是不可变的，而其他实现 CharSequence 接口的类（如 StringBuilder 和 StringBuffer）的内容是可变的。

**举例说明：**

```java
public class CharSequenceExample {
    public static void printLength(CharSequence cs) {
        System.out.println("字符序列长度: " + cs.length());
    }

    public static void main(String[] args) {
        String string = "Hello, world!";
        StringBuilder stringBuilder = new StringBuilder("Hello, world!");
        StringBuffer stringBuffer = new StringBuffer("Hello, world!");

        // 使用统一的CharSequence接口处理不同类型的字符序列
        printLength(string); // 输出：字符序列长度: 13
        printLength(stringBuilder); // 输出：字符序列长度: 13
        printLength(stringBuffer); // 输出：字符序列长度: 13
    }
}
```

在这个例子中，我们定义了一个 `printLength` 方法，它接收一个 CharSequence 参数并打印其长度。我们创建了一个 String 对象、一个 StringBuilder 对象和一个 StringBuffer 对象，然后分别传入 `printLength` 方法。由于这三个对象都实现了 CharSequence 接口，我们可以使用统一的方法处理它们。