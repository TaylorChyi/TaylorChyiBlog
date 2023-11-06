---
title: Path 与 Paths 的关系与区别
date: 2023-04-19
tags: 
- Java 
- Path 
- Paths
---

时间：2023-04-18
标签： #Java #Path #Paths

---

>import java.nio.file.Paths; import java.nio.file.Path; 为什么会存在两个歧义性很高的两个包在同一个包下，二者的功能的区别是什么

在这个例子中，我们使用了两个不同的类，它们都在 `java.nio.file` 包中：`Paths` 和 `Path`。虽然它们的名称很相似，但它们具有不同的功能和用途。

1.  `java.nio.file.Path`：`Path` 是一个接口，表示文件系统中文件或目录的路径。它提供了一种在文件系统中导航和操作文件的方法。`Path` 对象包含了路径信息，可以用来创建、删除、读取和修改文件或目录。
    
2.  `java.nio.file.Paths`：`Paths` 是一个工具类，包含一些静态方法，用于创建 `Path` 对象。它是一个方便的工具类，用于将字符串路径转换为 `Path` 对象，以便在文件系统中进行操作。
    

虽然它们的名字很相似，但它们的功能是互补的。我们通常使用 `Paths` 类中的静态方法创建一个 `Path` 对象，然后使用 `Path` 对象来操作和访问文件系统。

在本例中，我们使用 `Paths.get()` 方法将字符串形式的目录路径转换为 `Path` 对象。接着，我们使用 `Path` 对象来操作文件路径，例如获取文件名（`path.getFileName().toString()`）。