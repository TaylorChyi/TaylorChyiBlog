---
title: 如何查看项目有没有使用spring boot框架
date: 2023-04-19
tags: 
- java 
- spring 
- SpringBoot 
---

时间：2023-04-19
标签： #java #spring #SpringBoot 

---

要查看项目是否使用了 Spring Boot 框架，可以通过以下方式进行：

1.  查看项目依赖

在项目的 pom.xml 文件中查找是否存在 spring-boot-starter-parent 或 spring-boot-starter-web 等 Spring Boot 相关的依赖。这些依赖通常是 Spring Boot 项目所必需的，并且包含了 Spring Boot 相关的配置和功能。

例如，下面是一个 Spring Boot 项目的 pom.xml 文件示例：
```xml
<project>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>2.6.2</version>
    <relativePath />
  </parent>

  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
  </dependencies>
</project>
 ```
在上述示例代码中，可以看到该项目的父依赖为 spring-boot-starter-parent，并且项目依赖了 spring-boot-starter-web，这表明该项目是一个基于 Spring Boot 框架构建的 Web 项目。

2.  查看启动类
在项目的源代码中查找是否存在类似于以下代码的启动类：

```java
@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```
在上述示例代码中，使用 `@SpringBootApplication` 注解标注了 `MyApplication` 类，并且在 `main` 方法中调用了 `SpringApplication.run` 方法启动应用程序。这是 Spring Boot 项目的典型启动方式，因此如果存在类似的启动类，则表明该项目是基于 Spring Boot 框架构建的。

如果以上方式均没有找到 Spring Boot 相关的依赖和启动类，那么该项目可能没有使用 Spring Boot 框架。