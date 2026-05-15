---
title: Tim Berners-Lee
type: entity
status: active
domain: web-fundamentals
created: 2026-05-10
updated: 2026-05-10
tags:
  - wiki/entity
  - person
  - web
  - http
source_files:
  - raw/assets/Evolution of HTTP.md
---

# Tim Berners-Lee

英国计算机科学家，World Wide Web、HTTP 协议、HTML 语言及第一个 Web 浏览器与服务器的创造者。

## 关键事实

- **1989 年**：在 CERN 工作期间撰写了构建超文本系统的提案，最初称为 *Mesh*，后改名为 *World Wide Web*。
- **1990 年底**：完成了 Web 的四个基础构建块——HTML（超文本格式）、HTTP（传输协议）、WorldWideWeb（首个浏览器兼编辑器）、httpd（首个服务器）。
- **1991 年 8 月 6 日**：在 `alt.hypertext` 新闻组发帖，被视为 World Wide Web 作为公开项目的正式起点。
- 他所设计的 HTTP/0.9 极其简单，被称为"单行协议"，仅支持 `GET` 方法与纯 HTML 传输。

## 核心贡献

### 协议设计哲学

Berners-Lee 对 HTTP 的原始设想不仅是只读的文档检索，而是一种**分布式文件系统**——人们可以在远程添加和移动文档。这一设想后来在 WebDAV 扩展中得到了部分实现，但真正的读写 Web 至今仍未完全兑现。

### 简单性优先

HTTP/0.9 的极简设计——单行请求、无元数据、响应即文件——使协议能在 CERN 的半可信实验环境中快速落地并向外传播。这种"够用就好"的设计哲学为后续版本的渐进式演化奠定了基础。

### 架构愿景

他提出的超文本系统建立在 TCP/IP 之上，利用已有基础设施而非重新发明传输层。这一务实决策使 Web 得以在互联网已有的基础之上快速增长。

## 相关页面

- [HTTP 协议演化](../concepts/http.md) — 从 Berners-Lee 的 HTTP/0.9 到现代 HTTP/3 的完整演化历程
- [Evolution of HTTP (MDN)](../sources/evolution-of-http.md) — 本篇实体信息的直接来源
