---
title: 被 Lambda 表达式引用的局部变量必须是 final 或者是等同 final 效果的
date: 2023-04-28
tags: 
- Java 
- Lambda 
- Final 
- EffectivelyFinal
---

时间：2023-04-26
标签： #Java #Lambda #Final #EffectivelyFinal

---

确实，被 Lambda 表达式引用的局部变量必须是 final 或者是等同 final 效果的，这也被称为“effectively final”。

1. 为什么局部变量必须是 final 或者 effectively final：
   - Lambda 表达式会创建一个匿名类的实例，这个实例可能在另一个线程中执行。为了避免数据不一致的问题，Lambda 表达式要求局部变量是 final 或者 effectively final。
   - Final 变量的值是不可改变的，这就避免了在多线程环境下的数据竞争和同步问题。
   - 对于 effectively final 变量，虽然它们没有显式地被声明为 final，但在实际使用过程中，它们的值没有被改变，所以它们也被视为不可变的。

2. 什么是 effectively final：
   - 当一个局部变量满足以下条件时，它被认为是 effectively final：
     1. 变量没有被显式地声明为 final。
     2. 在初始化之后，变量的值没有被改变。

总结：在 Java 中，被 Lambda 表达式引用的局部变量必须是 final 或者 effectively final。这是为了避免在多线程环境下的数据竞争和同步问题。Effectively final 指的是变量在实际使用过程中，它们的值没有被改变，所以它们也被视为不可变的。