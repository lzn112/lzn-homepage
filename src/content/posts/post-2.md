---
title: 'Database Notes — 从首页开始整理'
author: Zenan Lin
date: '06-23-2025'
image:
    url: '/images/image-2.webp'
    alt: 'Database Notes'
---
把数据库相关的学习笔记整理到一个入口里。

## SQL 基础

结构化查询语言（SQL）是关系型数据库的标准语言。核心操作包括：

- **DDL（Data Definition Language）**：CREATE、ALTER、DROP
- **DML（Data Manipulation Language）**：SELECT、INSERT、UPDATE、DELETE
- **DCL（Data Control Language）**：GRANT、REVOKE

## 索引优化

索引是提高查询性能的关键手段：

- B+Tree 索引是最常用的索引结构
- 联合索引遵循最左前缀原则
- 覆盖索引可以避免回表查询
- 索引不是越多越好，维护索引也有代价

## 事务与隔离级别

ACID 特性是事务的核心保证：

- **原子性（Atomicity）**：事务要么全部成功，要么全部回滚
- **一致性（Consistency）**：事务前后数据保持一致状态
- **隔离性（Isolation）**：并发事务之间互不干扰
- **持久性（Durability）**：已提交的事务永久生效

四种隔离级别：Read Uncommitted → Read Committed → Repeatable Read → Serializable
