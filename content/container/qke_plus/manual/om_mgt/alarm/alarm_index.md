---
title: "告警指标说明"
description: QKE 支持的告警指标
draft: false
keyword: QKE,告警,指标
weight: 1
---

QKE 与云监控 CloudSat 对接，通过在 CloudSat 中设置指标告警规则，您可以及时发现容器服务的异常状况，以保证您业务的稳定性和可靠性。

QKE 支持的告警指标如下表所示。

| 指标                | 监控周期 | 单位/取值                         | 说明                            | 配置建议                                                     |
| :------------------ | -------- | :-------------------------------- | :------------------------------ | ------------------------------------------------------------ |
| 正在运行的 Pod 数量 | 5分钟    | 整数，>= 0                        | 集群节点上运行的 Pod 数量       | 根据节点类型进行配置，例如：4c/8g时，阈值建议配置为 20。     |
| 数据盘使用率        | 5分钟    | %，[0, 100]                       | 节点内数据盘使用量占总量之比    | 如果持续 1 分钟超过 80%，建议告警。                          |
| 系统盘使用率        | 5分钟    | %，[0, 100]                       | 节点内系统盘使用量占总量之比    | 如果持续 1 分钟超过 80%，建议告警。                          |
| 内存使用率          | 5分钟    | %，[0, 100]                       | 节点内内存使用量占节点总量之比  | 如果持续 1 分钟超过 50%，建议告警。                          |
| CPU 负载            | 5分钟    | 核，整数，>= 0                    | 节点内已使用的内存              | 如果持续 1 分钟超过 CPU 核数，建议告警。                     |
| CPU 使用率          | 5分钟    | %，[0, 100]                       | 节点内 CPU 使用量占节点总量之比 | 如果持续 1 分钟超过 50%，建议告警。                          |
| apiserver 的连通性  | 5分钟    | **1** 表示正常<br/>**0** 表示异常 | apiserver 是否能正常连接        | 如果持续 1 分钟，一直为 0（异常），则表示 apiserver 连接异常。 |

> **说明**
>
> 监控指标的最大值、最小值、平均值及总和，是指在一个监控周期内，指标的最大值、最小值、平均值及总和。

