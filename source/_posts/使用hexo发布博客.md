---
title: 使用hexo发布博客
date: 2023-04-19
tags: 
- hexo 
- github 
- GitHubPages 
- shell 
- blog
---

时间：2023-04-18
标签： #hexo #github #GitHubPages #shell #blog

---

按照以下步骤将您的 Markdown 文件发布到博客上：

1.  **创建新文章**：在 Hexo 项目目录中，运行以下命令以创建一个新的文章文件：

```shell
hexo new post "文章标题"
```
这将在 `source/_posts` 目录下创建一个新的 Markdown 文件，您可以用文本编辑器打开它。

2.  **编辑文章**：将您已经编写好的 Markdown 文件内容复制到新创建的文章文件中。如果需要，您可以在文件顶部的 front matter 中添加或编辑元数据（如标题、日期、标签等）。例如：
```yaml
---
title: "文章标题"
date: 2023-04-15
tags:
- 标签1
- 标签2
---

文章正文...

```
3.  **生成静态页面**：在项目目录中，运行以下命令以生成静态页面：
```shell
hexo generate
```
或
```shell
hexo g
```
这将在 `public` 文件夹中生成静态网页文件。

4.  **部署到 GitHub Pages**：在 Hexo 项目目录中的 `_config.yml` 文件中，配置好您的 GitHub Pages 仓库信息：
```yaml
deploy:
  type: git
  repo: https://github.com/your-username/your-username.github.io
  branch: main
```
然后安装 hexo-deployer-git 插件：
```shell
npm install hexo-deployer-git --save
```
部署博客：
```shell
hexo deploy
```
或
```shell
hexo d
```
这将把生成的静态页面推送到您的 GitHub Pages 仓库。

5.  **查看博客**：访问`https://your-username.github.io`，您应该能看到更新后的博客。请注意，GitHub Pages可能需要几分钟的时间来部署更新。

完成这些步骤后，您的Markdown文章就会发布到Hexo博客上。