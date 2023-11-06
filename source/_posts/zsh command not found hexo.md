---
title: zsh command not found hexo
date: 2023-04-19
tags: 
- zsh 
- hexo 
- 环境配置
---

时间：2023-04-18
标签： #zsh #hexo #环境配置

---

>zsh: command not found: hexo

这个错误通常是由于 Hexo 没有正确安装或者没有将其添加到系统路径中导致的。请按照以下步骤尝试解决这个问题：

1.  确保您已经安装了 Node.js 和 npm。您可以在命令行中运行以下命令来检查它们的版本：
```shell
node -v
npm -v
```
如果您还没有安装它们，请访问 [Node.js官方网站](https://nodejs.org/)下载并安装相应的版本。

2.  全局安装 Hexo。在命令行中运行以下命令：
```shell
npm install -g hexo-cli
```
这将在全局范围内安装 Hexo 命令行工具。在安装过程中，可能需要管理员权限。

3.  检查 Hexo 是否已成功安装。在命令行中运行以下命令：
```shell
hexo -v
```
如果您看到了 Hexo 的版本信息，那么说明 Hexo 已经成功安装。接下来，您可以继续按照之前的说明操作。

如果您仍然遇到“command not found”的错误，那么可能是因为Hexo的可执行文件没有被添加到系统路径中。请按照以下步骤进行操作：

1.  找到 Hexo 的安装路径。运行以下命令：
```shell
npm config get prefix
```
这将显示 npm 的全局安装路径。Hexo 的可执行文件通常位于该路径下的 `bin` 文件夹中。

2.  将Hexo的可执行文件路径添加到系统路径中。对于macOS和Linux用户，您需要编辑`~/.bashrc`（Bash用户）或`~/.zshrc`（Zsh用户）文件。对于Windows用户，您需要编辑环境变量。具体操作方法如下：

-   **macOS/Linux**：打开 `~/.bashrc` 或 `~/.zshrc` 文件，添加以下内容（==替换 `<npm-global-path>` 为实际路径==）：
```zsh
export PATH=$PATH:<npm-global-path>/bin
```
然后运行以下命令以使更改生效：
```shell
source ~/.bashrc
```
或
```shell
source ~/.zshrc
```
-   **Windows**：右键点击“计算机”（或“此电脑”）图标，选择“属性”。在“系统”窗口中，点击“高级系统设置” > “环境变量”。在“系统变量”区域中，找到名为“Path”的变量，点击“编辑”按钮。在“编辑环境变量”窗口中，将Hexo的可执行文件路径（`<npm-global-path>\bin`）添加到变量值中。请注意，不同路径之间应使用分号（`;`）分隔。