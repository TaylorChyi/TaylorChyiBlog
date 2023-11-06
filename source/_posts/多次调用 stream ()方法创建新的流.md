---
title: 多次调用 stream ()方法创建新的流
date: 2023-04-28
tags: 
- Java 
- Stream 
- 字符串处理
---

时间：2023-04-28
标签： #Java #Stream #字符串处理

---

在提供的代码中，`FileToWordsRegexp` 类的构造器将文件内容读取到一个字符串变量 `all` 中（跳过第一行注释，并将其转换为单行字符串）。接下来，类中的 `stream()` 方法使用这个 `all` 字符串来创建一个新的流。

在 `main` 方法中，我们可以看到 `stream()` 方法被多次调用以在已存储的字符串 `all` 中创建新的流。请参考以下代码片段：

```java
fw.stream()
  .limit(7)
  .map(w -> w + " ")
  .forEach(System.out::print);

fw.stream()
  .skip(7)
  .limit(2)
  .map(w -> w + " ")
  .forEach(System.out::print);
```

在这两个代码片段中，我们分别调用了两次 `fw.stream()` 方法。每次调用都会创建一个新的基于 `all` 字符串的流。第一次调用 `fw.stream()` 时，我们限制了流的前 7 个元素并打印它们。第二次调用 `fw.stream()` 时，我们跳过了前 7 个元素，然后限制接下来的 2 个元素并打印它们。

这个例子展示了如何多次调用 `stream()` 方法在已存储的字符串中创建一个新的流。因为 `all` 字符串是在构造器中读取并存储的，所以我们可以在同一个 `FileToWordsRegexp` 实例上多次调用 `stream()` 方法，每次都会返回一个新的基于 `all` 字符串的流。