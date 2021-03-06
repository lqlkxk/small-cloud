# Small-Cloud

[![Codecov](https://codecov.io/gh/alibaba/spring-cloud-alibaba/branch/master/graph/badge.svg)](https://codecov.io/gh/alibaba/spring-cloud-alibaba)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

小罗维护的一个项目。

有关英文文档，请参见[English document](https://github.com/yulo2020/small-cloud/blob/master/README-en.md)

Small-Cloud致力于为微服务开发提供一个脚手架。 该项目包括用于开发分布式应用程序服务的必要组件，支持多应用程序访问，并使开发人员可以轻松地使用Spring Cloud编程模型来开发分布式应用程序服务。

使用Github，您只需要添加一些注释和少量配置即可将Spring Cloud应用程序连接到分布式应用程序解决方案，并使用此支架快速构建分布式应用程序系统。

## 主要功能
* **服务认证授权**：基于Spring Security和OAuth2框架，支持4种授权模式，分为auth-server和auth-client，满足功能的同时尽可能的让代码简洁。
* **服务注册、发现和配置**：默认使用阿里的Nacos作为服务注册、发现和远程配置，生产环境可集群。
* **分布式基础公共支持**：small-core包含了常用的公共核心类。
* **网关服务**：以Spring Cloud官方的spring-cloud-gateway作为网关，支持动态路由、参数验签、token验证、限流和熔断等服务。
* **系统监控**：基于 spring-boot-admin-starter-server 为微服务应用实时监控的能力。
* **分布式事务**：基于txcln，使用 @EnableTransactionManagement 注解， 高效并且对业务几乎零侵入地解决分布式事务问题。
* **服务链路追踪**：基于zipkin提供服务链路追踪，支持mysql持久化。
* **消息驱动能力**：基于 Spring Cloud Stream 为微服务应用构建消息驱动能力。
* **分布式任务调度**：提供秒级、精准、高可靠、高可用的定时（基于 Cron 表达式）任务调度服务。同时提供分布式的任务执行模型，如网格任务。网格任务支持海量子任务均匀分配到所有 Worker（schedulerx-client）上执行。


## 模块说明
```lua
small-cloud                     -- 父项目，依赖管理
│  ├─small-auth-client    -- oauth2客户端依赖
│  ├─small-auth-server    -- oauth2服务端[8050]
│  ├─small-core         -- 公共的依赖
│  ├─small-docs           -- 项目文档
│  ├─small-gateway       -- 网关服务[9020]
│  ├─small-modules               -- 业务模块一级工程
│  │  ├─small-order         -- 订单服务
│  │  ├─small-user          -- 用户中心[8020]
│  │  ├─small-spider        -- 网络蜘蛛工程
│  ├─small-monitor       -- 监控中心
│  ├─small-naocos        -- 服务注册和配置中心
│  ├─small-starter        -- starter通用工具一级工程
│  │  ├─small-starter-redis --redis
│  │  ├─敬请期待
│  ├─small-txlcn          -- txlcn分布式事务管理服务
│  ├─small-zipkin         -- 服务链路追踪服务

```


## 开发规范




