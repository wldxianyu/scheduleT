# scheduleT


## 简介
scheduleT 是全新一代分布式调度与计算框架，能让您轻松完成作业的调度与繁杂任务的分布式计算。

## 特性
- 提供资源治理和集群管理，支持多区域联邦，可横向扩展
- 支持资源调度且集群管理和资源调度逻辑拆分， 支持多调度器开发，满足多场景的调度需求
- DAG 工作流，支持任务编排，上下游任务间的数据传递


### 分层架构图

![](https://github.com/wldxianyu/scheduleT/blob/main/images/scheduleT_reference.svg)

- gateway-api-serve 网关层 资源操作入口， 认证，授权，访问控制，持久化
- nomad-server   核心层: 集群管理(故障检查)， 资源调度， 区域联邦
- nomad-drivers  驱动层: 标识任务以什么方式执行, 比如Docker, Java和二进制文件