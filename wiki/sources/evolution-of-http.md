---
title: Evolution of HTTP
type: source
status: active
domain: web-fundamentals
created: 2026-05-10
updated: 2026-05-10
tags:
  - wiki/source
  - web
  - http
  - protocol
source_files:
  - raw/assets/Evolution of HTTP.md
source_url: https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Evolution_of_HTTP
---

# Evolution of HTTP

MDN 官方指南，系统梳理 HTTP 从 1989 年诞生至今的全部主要版本与扩展。

## 摘要

本文档以时间线形式覆盖 HTTP 的完整演化：从 HTTP/0.9（单行协议，仅支持 GET 纯 HTML），到 HTTP/1.0（引入状态码、头部与 Content-Type），再到 HTTP/1.1（持久连接、管线化、Host 头、分块传输、缓存与内容协商），最后到 HTTP/2（二进制帧、多路复用、头部压缩）与 HTTP/3（基于 QUIC/UDP，消除 TCP 队头阻塞）。此外还涵盖 TLS/SSL 加密层、REST 架构风格、WebDAV 扩展、CORS/CSP 安全策略以及 WebSocket 与 SSE 等协议扩展。

## 关键要点

- **HTTP/0.9（1991）**：仅 `GET` 命令，无头部无状态码，只能传输 HTML，被称为"单行协议"。
- **HTTP/1.0（1996，RFC 1945）**：引入 HTTP 版本标识、状态码、请求/响应头部、`Content-Type`，支持传输任何 MIME 类型，但本质仍是"事后编撰"的非正式标准。
- **HTTP/1.1（1997，RFC 2068；后经 2616、7230–7235、9110–9112 多次修订）**：连接复用、管线化、分块传输、`Host` 头支持虚拟主机、增强缓存控制与内容协商，成为极度稳定的标准，统治互联网超过 15 年。
- **HTTP/1.1 的瓶颈**：TCP 连接建立的昂贵开销与 TCP 慢启动；虽通过 6 路并行连接缓解，但仍存在队头阻塞问题。
- **TLS/SSL 安全层（1994 起）**：Netscape 引入 SSL，后标准化为 TLS，从电子商务场景逐步扩展为全站加密的基础设施。
- **HTTP/2（2015，RFC 9113）**：基于 SPDY，二进制帧协议替代文本协议，单连接多路复用消除应用层队头阻塞，HPACK 头部压缩减少冗余。
- **HTTP/3（2022，RFC 9114）**：语义不变，传输层从 TCP 迁移到 QUIC（基于 UDP），在 QUIC 流级别实现独立丢包恢复，消除 TCP 层队头阻塞。
- **协议扩展生态**：WebDAV/CardDAV/CalDAV（1996 起）、REST（2000）、SSE、WebSocket、Alt-Svc、Client Hints、CORS、CSP、安全 Cookie 前缀等均建立在 HTTP 的可扩展性之上。
- **2022 里程碑**：HTTP 全套语义、缓存与各版本规范在 RFC 9110–9114 中重组并终于达到 Internet Standard（STD 97）地位。

## 证据

- MDN 文档以 HTTP 请求/响应的具体格式示例展示了各版本差异。
- 引用了众多 RFC（1945、2068、2616、7230–7235、9110–9114）。
- 引用了 W3Techs 的协议使用率统计数据，如 HTTP/2 在 2022 年 1 月达峰值 46.9%，HTTP/3 在 2022 年 10 月达 26%。
- 提到了 CERN、Netscape Communications、Google 在关键阶段的历史角色。

## 开放问题

- HTTP/2 的广泛部署为何未在第 6 路并行连接之外完全消除队头阻塞（TCP 层面的根本限制）？
- HTTP/3 的 QUIC 是否会在某些网络环境下因 UDP 受限而回退到 TCP？
- 随着 HTTP 逐步二进制化，协议的可调试性与可读性是否已成为次要优先级？

## 相关页面

- [HTTP 协议演化](../concepts/http.md) – 从概念角度整合各版本 HTTP 的关键创新与设计取舍
- [Tim Berners-Lee](../entities/tim-berners-lee.md) – HTTP、HTML 与 Web 的创始人
