# SPEC.md - test-xxl-job

## 1. Project Overview

- **Project Name**: test-xxl-job
- **Project Type**: Maven Java Project (Spring Boot)
- **Description**: XXL-JOB分布式任务调度平台的学习测试项目，演示任务调度、定时任务、分片任务、失败重试等核心功能。
- **Location**: /Users/junw/Documents/GitHub/test-xxl-job

## 2. Build Status

**Compilation: FAILED**

### Compilation Errors
```
- org.apache.ibatis.annotations does not exist (Mapper annotation missing)
- javax.annotation does not exist
- javax.servlet.http does not exist (HttpServletRequest)
```
**Root Cause**: Missing MyBatis and Servlet API dependencies in pom.xml

## 3. Project Structure

```
test-xxl-job/
├── pom.xml
├── src/main/java/wo1261931870/testxxljob/
│   ├── controller/
│   ├── dao/           # MyBatis Mapper DAOs
│   ├── service/
│   └── XxlJobApplication.java
├── src/main/resources/
│   ├── application.properties
│   └── templates/     # FreeMarker templates
│   └── static/        # CSS, JS, plugins
└── target/
```

## 4. Technology Stack

- Java 17+
- Spring Boot 3.x
- XXL-JOB 2.x
- MySQL
- MyBatis
- FreeMarker

## 5. Key Features

- Bean模式任务
- GLUE模式任务
- 脚本任务
- 分片广播
- 失败重试
- 故障转移
- CRON表达式调度

## 6. README Status

- README.md: EXISTS
- SPEC.md: CREATED (this file)

## 7. Gitignore

Standard Java gitignore covering:
- Compiled class files (*.class)
- Log files (*.log)
- Package archives (*.jar, *.war, etc.)
- IDE files (.idea, .iml)
- OS files (.DS_Store)

## 8. Build Fix Suggestions

To fix compilation, add the following dependencies to pom.xml:

```xml
<dependency>
    <groupId>org.mybatis.spring.boot</groupId>
    <artifactId>mybatis-spring-boot-starter</artifactId>
    <version>3.0.3</version>
</dependency>
<dependency>
    <groupId>jakarta.servlet</groupId>
    <artifactId>jakarta.servlet-api</artifactId>
    <scope>provided</scope>
</dependency>
```

## 9. Last Updated

2026-04-22
