---
title: 'JAVA — JVM & Core Fundamentals'
author: Zenan Lin
date: '05-27-2025'
image:
    url: '/images/image-1.webp'
    alt: 'Java JVM Architecture'
---
## JVM & JRE & JDK

JDK（Java Development Kit）是 Java 开发工具包，包含 JRE + javac + javadoc（文档生成器）+ jdb（调试器）+ jconsole（监控工具）+ javap（反编译工具）等。

**JVM（Java Virtual Machine）** 是运行 Java 字节码的虚拟机，负责类加载、字节码执行、内存管理和垃圾回收。

**JRE（Java Runtime Environment）** 是运行已编译 Java 程序所需的环境，包含 JVM + 核心类库。

## JVM 内存模型

JVM 内存主要分为以下几个区域：

- **堆（Heap）**：存放对象实例，是 GC 的主要区域
- **方法区（Method Area）**：存储类信息、常量、静态变量
- **虚拟机栈（VM Stack）**：每个线程私有，存储局部变量表、操作数栈等
- **本地方法栈（Native Method Stack）**：为 Native 方法服务
- **程序计数器（Program Counter Register）**：记录当前线程执行的字节码行号

## Java 异常体系

Java 异常分为两大类：

- **Checked Exception**：编译时异常，必须显式处理（try-catch 或 throws）
- **Unchecked Exception**：运行时异常（RuntimeException 及其子类），不强制处理

## 序列化

序列化是将对象转换为字节序列的过程，反序列化则是将字节序列恢复为对象。实现 `Serializable` 接口即可让对象支持序列化。
