---
title: 在 VS Code 中使用 Spring Boot Extension Pack 创建 Spring Boot 项目
date: 2023-04-19
tags: 
- VSCode 
- SpringBoot 
- SpringInitializr 
- Java 
- 项目创建 
- 依赖管理 
- ExtensionPack
---

时间：2023-04-12
标签： #VSCode #SpringBoot #SpringInitializr #Java #项目创建 #依赖管理 #ExtensionPack

---

以下是使用 VS Code 的 Spring Boot Extension Pack 来创建 Spring Boot 项目的步骤：

1.  在 VS Code 中，按下 `Ctrl + Shift + P`（Mac 下为 `Cmd + Shift + P`）打开命令面板。
    
2.  在命令面板中输入 "Spring Initializr"，然后选择 "Spring Initializr: Generate a Maven Project"（或 "Spring Initializr: Generate a Gradle Project"，取决于你喜欢的构建工具）。
    
3.  选择 "Java" 作为编程语言。
    
4.  输入 Group ID，这通常是你的公司或项目的域名反转，例如 "com.example"。
    
5.  输入 Artifact ID，这是你的项目名称，例如 "myproject"。
    
6.  选择项目打包方式，推荐选择 "Jar"。
    
7.  选择 Java 版本，推荐使用 "11" 或更高版本。
    
8.  在依赖列表中，添加所需的依赖，例如：
    
    -   搜索 "web" 并选择 "Spring Web"（用于创建 Web 应用和 RESTful API）。
    -   搜索 "mysql" 或 "postgresql" 并选择对应的 "MySQL Driver" 或 "PostgreSQL Driver"（根据你的数据库类型选择合适的驱动）。
    -   搜索 "jpa" 并选择 "Spring Data JPA"（用于实现数据访问层，可选）。
    -   根据项目需求，添加其他依赖。
9.  点击 "Finish" 生成项目。选择一个文件夹来保存生成的项目。VS Code 将自动解压项目并打开它。
    

至此，你已经使用 VS Code 的 Spring Boot Extension Pack 创建了一个 Spring Boot 项目。