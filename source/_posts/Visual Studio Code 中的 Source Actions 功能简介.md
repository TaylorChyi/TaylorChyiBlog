---
title: Visual Studio Code 中的 Source Actions 功能简介
date: 2023-04-19
tags: 
- VisualStudioCode 
- VSCode 
- SourceActions 
- 代码重构 
- 代码生成 
- 开发工具 
---

时间：2023-04-18
标签： #VisualStudioCode #VSCode #SourceActions #代码重构 #代码生成 #开发工具 

---

在 Visual Studio Code 中，Source Actions 是一组针对源代码进行操作的快捷功能。它们可以帮助您自动执行常见的代码重构和改进任务，例如排序导入、移除未使用的导入、自动生成方法实现等。这些功能可以提高开发效率，减少手动修改代码的需求。

以下是一些常见的 Source Actions：

1.  **Organize Imports (整理导入)**：自动整理和优化当前文件的导入语句。它会删除未使用的导入，同时按字母顺序或其他规则对导入进行排序。
2.  **Generate Getters and Setters (生成 getter 和 setter 方法)**：针对选定的类属性自动生成 getter 和 setter 方法。这可以方便地封装类的内部实现，提供统一的访问接口。
3.  **Generate Constructors (生成构造函数)**：自动生成构造函数，以便根据类的属性初始化对象。
4.  **Generate toString(), hashCode() and equals() methods (生成 toString()、hashCode() 和 equals() 方法)**：自动生成类的 toString()、hashCode() 和 equals() 方法，用于实现对象的字符串表示、哈希计算和相等性判断。
5.  **Extract Method (提取方法)**：将选定的代码片段提取到一个新的方法中，以便重用和简化代码。
6.  **Extract Variable (提取变量)**：将选定的表达式提取到一个新的变量中，以便重用和简化代码。

要使用 Source Actions，您可以右键单击编辑器中的代码，然后选择 "Source Action" 菜单。此外，您还可以打开命令面板（按 `Ctrl+Shift+P` 或 `Cmd+Shift+P`），然后输入 "Source Action" 来查找和执行相应的操作。在使用特定编程语言时，可能需要安装相应的扩展以启用 Source Actions 功能。例如，在使用 Java 时，可以安装 "Java Extension Pack" 扩展来启用这些功能。

原本 Source Actions 功能并没有设置快捷键，在我们按下 `Ctrl+Shift+P` 或  `Cmd+Shift+P `并输入"Source Action" 后，相应的后面有一个齿轮图标，点击该图标按钮可以在弹出的页面中为该功能设置快捷键，例如，`Cmd+option+a`