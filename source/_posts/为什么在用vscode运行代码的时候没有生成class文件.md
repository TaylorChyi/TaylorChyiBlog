---
title: 为什么在用vscode运行代码的时候没有生成class文件
date: 2023-04-19
tags: 
- VSCode 
- Java 
- Class 
---

时间：2023-04-12
标签： #VSCode #Java #Class 

---

在使用 VSCode 编写并运行 Java 代码时，默认情况下，编译生成的 `.class` 文件通常存储在内存中，并不会直接在文件系统中生成。这使得运行 Java 代码更加高效，因为不需要频繁地读写磁盘。这也是为什么你在项目目录下没有看到 `.class` 文件的原因。

但是，如果你希望查看或保存生成的`.class`文件，可以通过以下步骤将它们输出到项目目录中：

1.  在VSCode中，打开Settings（快捷键`Ctrl+,`），然后点击右上角的“Open Settings (JSON)”图标，这将打开`settings.json`文件。
2.  在 `settings.json` 文件中，添加以下配置：
```json
{
    "java.debug.settings.console": "internalConsole",
    "java.dependency.outputPath": "output",
    "java.project.outputPath": "output"
}
```
这里，我们将 `java.project.outputPath` 设置为 `output`。这意味着编译生成的 `.class` 文件将被保存到名为 `output` 的文件夹中。你可以根据自己的需求更改该值。

3.  保存`settings.json`文件，然后重新运行你的Java程序。

现在，在你指定的输出文件夹（如`output`）中，你应该能够看到生成的`.class`文件。请注意，这种做法会在磁盘上生成额外的文件，可能会影响性能。在开发过程中，通常不需要将`.class`文件保存到磁盘。这种方法主要用于调试或特殊需求。