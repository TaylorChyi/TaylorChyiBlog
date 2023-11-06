---
title: bashrc 与 zshrc的区别
date: 2023-04-19
tags: 
- bash 
- zsh 
---

时间：2023-04-18
标签： #bash #zsh 

---

`~/.bashrc`（Bash 用户）和 `~/.zshrc`（Zsh 用户）是 shell 配置文件。它们分别为 Bash 和 Zsh shell 提供配置和个性化设置。当您打开一个新的终端会话时，系统会自动加载这些配置文件，从而应用您为 shell 定义的任何自定义设置、别名、环境变量等。

1.  **Bash**：Bash（Bourne Again Shell）是许多Linux发行版中默认的shell。macOS的早期版本也使用了Bash作为默认shell。`~/.bashrc`文件用于为Bash shell提供个性化设置。它可以包含您希望在每个新的终端会话中自动执行的命令和设置，例如定义别名、设置环境变量和更改提示符样式。
    
2.  **Zsh**：Zsh（Z shell）是另一种流行的Unix shell，它为用户提供了一些额外的功能，如命令补全、主题和插件支持。从macOS Catalina开始，Zsh成为macOS的默认shell。`~/.zshrc`文件用于为Zsh shell提供个性化设置，其功能与`~/.bashrc`相似，但针对Zsh shell。
    

您只有`~/.zshrc`文件可能是因为您的系统使用Zsh作为默认shell。要确认当前正在使用的shell，请在终端中运行以下命令：

bashCopy code

```shell
echo $SHELL
```

这将显示您正在使用的shell，例如`/bin/bash`或`/bin/zsh`。

您可以根据需要在`~/.zshrc`文件中添加自定义设置、别名和环境变量。要编辑此文件，您可以使用文本编辑器（例如`nano`、`vim`或`Visual Studio Code`）打开它，然后保存更改。在更改配置文件后，请确保运行`source ~/.zshrc`命令以使更改生效。