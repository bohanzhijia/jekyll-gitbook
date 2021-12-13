---
title: Dubbo History
author: 锋言锋语
date: 2021-12-13
category: dubbo
layout: post
---

Dubbo项目目录介绍

```html
-- dubbo-build-tools 构建工具模块
-- dubbo-cluster 集群模块：将多个服务提供方伪装为一个提供方，包括：负载均衡, 集群容错，路由，分组聚合等。集群的地址列表可以是静态配置的，也可以是由注册中心下发。
-- dubbo-common 公共逻辑模块：提供工具类和通用模型
-- dubbo-compatible 兼容低版本模块：兼容老版本提供，未来可能删除
-- dubbo-config 配置模块：是 Dubbo 对外的 API，用户通过 Config 使用Dubbo，隐藏 Dubbo 所有细节。
-- dubbo-configcenter 配置中心模块：支持apollo、nacos、zk
-- dubbo-container 容器模块：是一个 Standlone 的容器，以简单的 Main 加载 Spring 启动，因为服务通常不需要 Tomcat/JBoss 等 Web 容器的特性，没必要用 Web 容器去加载服务。
-- dubbo-demo 快速启动示例。
-- dubbo-dependencies 依赖包模块
-- dubbo-dependencies-bom 依赖bom
-- dubbo-distribution
-- dubbo-filter 过滤器模块：提供了内置的过滤器
-- dubbo-metadata 元数据中心：支持nacos、redis、zk等
-- dubbo-metrics 指标统计模块
-- dubbo-monitor 监控模块：统计服务调用次数，调用时间的，调用链跟踪的服务。
-- dubbo-native 适配器
-- dubbo-native-plugin 适配器
-- dubbo-plugin 插件模块：提供了内置的插件。
-- dubbo-registry 注册中心模块：基于注册中心下发地址的集群方式，以及对各种注册中心的抽象。
-- dubbo-remoting 远程通信模块：提供通用的客户端和服务端的通讯功能。
    -- dubbo-remoting-api 定义了 Dubbo Client 和 Dubbo Server 的接口 <重点>
    -- dubbo-remoting-http 基于 Jetty 或 Tomcat 实现
    -- dubbo-remoting-netty 基于 Netty 3 实现。
    -- dubbo-remoting-netty4 基于 Netty 4 实现。<重点>
    -- dubbo-remoting-zookeeper 相当于 Zookeeper Client ，和 Zookeeper Server 通信。 <重点>
    -- dubbo-remoting-zookeeper-curator5 相当于 Zookeeper Client ，和 Zookeeper Server 通信。
-- dubbo-rpc 远程调用模块：抽象各种协议，以及动态代理，只包含一对一的调用，不关心集群的管理。
    -- dubbo-rpc-api 抽象各种协议以及动态代理，实现了一对一的调用。
    -- dubbo-rpc-dubbo
    -- dubbo-rpc-grpc
    -- dubbo-rpc-injvm
    -- dubbo-rpc-rest
    -- dubbo-rpc-triple
-- dubbo-serialization 序列化模块
-- dubbo-spring-boot
-- dubbo-test 测试模块。
```
