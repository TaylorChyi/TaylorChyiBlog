---
title: 变量捕获（Variable Capture）
date: 2023-04-28
tags: 
- Java 
- Lambda 
- AnonymousClass 
- VariableCapture
---

时间：2023-04-26
标签： #Java #Lambda #AnonymousClass #VariableCapture

---

变量捕获是指在闭包（如 Lambda 表达式或匿名内部类）中访问和使用其外部作用域的变量的过程。在 Java 中，变量捕获主要出现在以下两种场景：

1. 匿名内部类中的变量捕获
   - 在匿名内部类中，可以访问其外部作用域的 final 变量。在 Java 8 之前，这些变量必须显式地声明为 final。
   - 从 Java 8 开始，引入了 effectively final 的概念，即使变量没有显式地声明为 final，只要它们在初始化之后没有被修改，就可以在匿名内部类中使用。

2. Lambda 表达式中的变量捕获
   - Lambda 表达式也可以捕获其外部作用域的变量，但这些变量必须是 final 或 effectively final。
   - 要求捕获的变量是 final 或 effectively final 的原因是为了避免多线程环境下的数据竞争和同步问题。

示例：

```java
public class VariableCaptureExample {
    public static void main(String[] args) {
        int localVar = 10;

        // 匿名内部类中的变量捕获
        new Thread(new Runnable() {
            @Override
            public void run() {
                System.out.println("Anonymous Class localVar: " + localVar);
            }
        }).start();

        // Lambda 表达式中的变量捕获
        new Thread(() -> System.out.println("Lambda localVar: " + localVar)).start();
    }
}
```

总结：变量捕获是指在闭包（如 Lambda 表达式或匿名内部类）中访问和使用其外部作用域的变量的过程。在 Java 中，这些捕获的变量必须是 final 或 effectively final，以避免多线程环境下的数据竞争和同步问题。