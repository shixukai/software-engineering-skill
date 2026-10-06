# 架构取舍

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 哪种方案在当前约束下值得实现？ | [SE-ARCH-QUALITY-TRADEOFF 用质量场景比较方案](../rules/se-arch-quality-tradeoff.md) |
| 模块是否确实需要独立进程或服务？ | [SE-ARCH-DISTRIBUTION-BOUNDARY 证明进程与部署边界的收益](../rules/se-arch-distribution-boundary.md) |

按条件深入：需要围绕驱动因素逐轮细化设计时，可直达[第3.2节设计迭代](../methods/architecture-drivers-tradeoffs.md#32-围绕当前目标迭代设计)；对变化做轻量场景复评时，可直达[第8.3节轻量评估](../methods/architecture-drivers-tradeoffs.md#83-对变化和未评部分做轻量评估)；新业务、质量目标或关键约束要求改变模块、部署、数据或依赖边界，需要比较候选并规划演进时，读取[从架构驱动因素到方案取舍与演进](../methods/architecture-drivers-tradeoffs.md)。

按条件深入：同名概念在身份、状态、规则或决定责任上发生冲突，需要比较共享模型、定向转换与独立处理，或随新业务理解演进模型时，读取[上下文含义、协作关系与模型演进方法](../methods/context-meaning-model-evolution.md)。

按条件深入：需要选择远程请求粒度、解释逐跳确认，或处理消息交付失败、业务结果未知与异常保留责任时，读取[消息交付、确认与异常处置方法](../methods/message-delivery-acknowledgment.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
