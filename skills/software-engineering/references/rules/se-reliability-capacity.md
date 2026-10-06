# SE-RELIABILITY-CAPACITY 验证过载后的存活与恢复

## 目录

- [1. 判断问题](#1-判断问题)
- [2. 条件与证据](#2-条件与证据)
- [3. 操作与取舍](#3-操作与取舍)
- [4. 验证与反例](#4-验证与反例)
- [5. 来源](#5-来源)

## 1. 判断问题

容量边界在哪里，越界后还能保留多少有效服务？

## 2. 条件与证据

适用：

- 容量规划、性能风险或过载保护设计

不适用或需调整：

- 没有容量相关变化的普通局部改动，不强制负载测试

必要证据：

- 请求大小、代价、分布、突发、扇出与资源需求
- 当前瓶颈、容量余量及故障时可用容量
- 队列、拒绝、降级与恢复规则

## 3. 操作与取舍

1. 按实际请求成本和资源限制描述负载，避免仅用平均QPS代表所有工作。
2. 建立逐渐增长、突发、部分容量丢失和慢依赖的场景，观察有效吞吐、尾延迟、错误和积压。
3. 在资源耗尽前有界排队、拒绝或降级；优先保护业务必要操作。
4. 检查降载后能否自动恢复，避免仅证明峰值吞吐而未验证恢复路径。
5. 实验在获准环境中进行，限定影响范围与停止条件；采用的工作负载须符合当前任务的数据与操作约束。

- 容量余量和隔离增加成本，队列吸收突发但增加延迟和积压。
- 降级逻辑本身需验证，过度复杂会增加新的失效路径。

## 4. 验证与反例

- 明确正常、饱和和过载各阶段行为
- 过载时核心有效吞吐不会无界崩溃
- 降载及依赖恢复后能退出降级并消化允许的积压

反例：压测只缓慢预热后记录峰值，实际突发时缓存未热且重试放大，系统越过拐点无法自行恢复。

## 5. 来源

以下支持方法选择，不能据此证明当前项目存在问题。标记说明：原书观点、多源综合、工程适配分别对应来源主张及本规则的加工关系。

- **多源综合**：Designing Data-Intensive Applications，第1章：描述负载；应对负载的方法。支持：负载分布和关键参数决定架构适用性。。定位：ch1.html#描述负载。来源标识：`data-intensive-applications`。
- **多源综合**：Site Reliability Engineering: How Google Runs Production Systems，第21章：The Pitfalls of Queries per Second。支持：请求成本不同，容量要对应受限资源。。定位：ch027.xhtml#the-pitfalls-of-queries-per-second。来源标识：`site-reliability-engineering`。
- **多源综合**：Site Reliability Engineering: How Google Runs Production Systems，第22章：Preventing Server Overload；Testing for Cascading Failures。支持：过载保护、突发与渐进负载、恢复行为和非关键依赖测试。。定位：ch028.xhtml#xref_cascading-failure_testing。来源标识：`site-reliability-engineering`。

详细身份与版本见[来源目录](../sources.md)。
