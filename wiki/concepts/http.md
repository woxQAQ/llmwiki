---
title: HTTP 协议演化
type: concept
status: active
domain: web-fundamentals
created: 2026-05-10
updated: 2026-05-10
tags:
  - wiki/concept
  - web
  - http
  - protocol
source_files:
  - raw/assets/Evolution of HTTP.md
---

# HTTP 协议演化

HTTP 的演化史是一场在"保持简单"与"适应爆炸性增长的需求"之间的持续张力。从实验室里交换纯文本文件的单行协议，到支撑全球视频流、实时通信与电商的基础设施，HTTP 的每个大版本都回应了一个具体而尖锐的瓶颈。

## 版本演进总览

| 版本 | 年份 | 传输层 | 核心创新 |
|------|------|--------|----------|
| HTTP/0.9 | 1991 | TCP | 单行 `GET`，无头无状态码，仅传 HTML |
| HTTP/1.0 | 1996 | TCP | 状态码、HTTP 头部、Content-Type 支持多格式 |
| HTTP/1.1 | 1997 | TCP | 连接复用、管线化、Host 头、分块传输、缓存协商 |
| HTTP/2 | 2015 | TCP | 二进制帧、多路复用、HPACK 头部压缩 |
| HTTP/3 | 2022 | QUIC(UDP) | 流级独立丢包恢复，消除 TCP 队头阻塞 |

## 核心设计取舍

### 简单性 vs. 性能

HTTP/0.9 的设计极其简单——单行请求、无元数据、响应就是文件本身。正是这种简单性使 HTTP 在早期得以快速实现和部署。但随后每个版本都在增加复杂度以换取性能：

- HTTP/1.0 通过头部引入元数据层的可扩展性，但每次请求仍需新建 TCP 连接。
- HTTP/1.1 通过连接复用降低了连接开销，但文本协议的解析成本与队头阻塞成为新瓶颈。
- HTTP/2 用二进制帧协议彻底解决了应用层队头阻塞，但这也意味着协议对人类不再可读（不可手动调试）。
- HTTP/3 将传输层从 TCP 切换到 QUIC，以 UDP 为基础在流级别独立处理丢包，代价是与传统网络中间件的兼容性。

### 可扩展性作为第一原则

HTTP 的头部机制使其成为一种"元协议"——可以在不改变核心协议的情况下添加新能力。一系列关键扩展都建立在这一基础之上：

- **安全层**：从 SSL 到 TLS，HTTP 语义之上叠加了加密与认证。
- **内容协商**：`Accept`、`Accept-Language`、`Accept-Encoding` 等头部使客户端和服务器可以就内容格式达成一致。
- **缓存体系**：`Cache-Control`、`ETag`、`Last-Modified` 构建了分层缓存基础设施。
- **安全策略**：CORS 和 CSP 通过新的头部集合放宽或收紧同源策略。
- **协议升级**：WebSocket 通过 HTTP 的 `Upgrade` 机制协商协议切换；Alt-Svc 允许将资源标识与位置解耦。

### 队头阻塞的三次解决尝试

队头阻塞（Head-of-Line Blocking）是贯穿 HTTP 演化史的核心问题：

1. **HTTP/1.1 的管线化**：理论上允许一个请求尚未完成就发送下一个，但实践中支持有限，多数主流浏览器因兼容性关闭了管线化。
2. **HTTP/2 的多路复用**：在同一个 TCP 连接上以独立的二进制帧并行传输多个流，消除了应用层的队头阻塞。但由于所有流共享同一个 TCP 连接，TCP 层的丢包重传仍会阻塞所有流。
3. **HTTP/3 的 QUIC**：将每条流的数据包丢失与重传完全独立化，真正消除了传输层的队头阻塞。

## REST 与 Web 应用的崛起

2000 年，Roy Fielding 提出 REST 架构风格，将 HTTP 重新解释为一种以资源为中心的交互协议。与 WebDAV 等需要服务器端专门实现的扩展不同，REST 仅依赖标准的 HTTP 方法（GET、POST、PUT、DELETE）和 URI 设计，使任何 Web 应用都可以暴露可编程接口。RESTful API 在 2010 年代成为主流，但也因各网站自行定义非标准 API 而失去了 WebDAV 式的互操作性。

## 安全模型的共生演化

HTTP 与 Web 安全模型的关系是逆向形成的——同源策略在 HTTP 创建之后才发展出来，而后又通过 HTTP 头部被逐步放松：

- **CORS**：允许服务器声明哪些外部源可以访问其资源。
- **CSP**：允许服务器限制浏览器可以加载和执行的内容来源。
- **安全 Cookie 前缀**：`__Secure-` 和 `__Host-` 前缀防止 Cookie 被非安全上下文篡改。

## 证据与来源

- [Evolution of HTTP (MDN)](../sources/evolution-of-http.md) 是本文的主要信息来源。
- 各版本 RFC：1945、2068、2616、7230–7235、9110–9114。
- W3Techs 统计数据佐证 HTTP/2 和 HTTP/3 的采用率变化。

## 开放问题

- HTTP/3 的 UDP 基础是否会在某些企业防火墙或受限网络环境中成为障碍？
- HTTP/2 的峰值采用率（2022 年 1 月 46.9%）之后是否会逐步被 HTTP/3 取代，还是会长期共存？
- 随着 HTTP 走向二进制化，协议透明度下降是否会导致调试工具与开发者教育成本上升？

## 相关页面

- [Tim Berners-Lee](../entities/tim-berners-lee.md) — HTTP、HTML 与 World Wide Web 的创造者
