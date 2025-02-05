---
aliases:
    - /zh/overview/what/ecosystem/protocol/grpc/
description: ""
linkTitle: gRPC
title: gRPC
type: docs
weight: 4
---



## 特性说明

Dubbo 自 2.7.5 版本开始支持原生 gRPC 协议，对于计划使用 HTTP/2 通信，或者想利用 gRPC 带来的 Stream、反压、Reactive 编程等能力的开发者来说，
都可以考虑启用 gRPC 协议。

> 从 Dubbo 3 开始，Dubbo 提供的 Triple 协议原生支持 gRPC 协议。

#### 支持 gRPC 的好处
* 为期望使用 gRPC 协议的用户带来服务治理能力，方便接入 Dubbo 体系
* 用户可以使用 Dubbo 风格的，基于接口的编程风格来定义和使用远程服务

## 使用场景

- 需要立即响应才能继续处理的同步后端微服务到微服务通信。
- 需要支持混合编程平台的 Polyglot 环境。
- 性能至关重要的低延迟和高吞吐量通信。
- 点到点实时通信 - gRPC 无需轮询即可实时推送消息，并且能对双向流式处理提供出色的支持。
- 网络受约束环境 - 二进制 gRPC 消息始终小于等效的基于文本的 JSON 消息。

## 使用方式 - Java

[示例](https://github.com/apache/dubbo-samples/tree/master/3-extensions/protocol/dubbo-samples-grpc)

## 使用方式 - Go

TBD

## 使用方式 - Node.js

TBD

## 使用方式 - Rust

暂不支持

### 步骤
1. 使用 IDL 定义服务
2. 配置 compiler 插件，本地预编译
3. 配置暴露/引用 Dubbo 服务
