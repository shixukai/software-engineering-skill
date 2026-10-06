# 领域与边界

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 业务描述与实现是否表达同一个规则？ | [SE-DOMAIN-LANGUAGE 在业务场景中检验术语](../rules/se-domain-language.md) |
| 哪些概念应共享，哪些应分开？ | [SE-DOMAIN-CONTEXT 显式标出模型适用边界与转换](../rules/se-domain-context.md) |
| 事务脚本、表模块或领域模型哪种更合适？ | [SE-DOMAIN-MODEL-COST 按规则复杂度选择领域逻辑组织方式](../rules/se-domain-model-cost.md) |
| 哪些状态必须一起成立和提交？ | [SE-DOMAIN-AGGREGATE 用不变量定义一致性边界](../rules/se-domain-aggregate.md) |

按条件深入：同名概念在身份、状态、规则或决定责任上发生冲突，需要比较共享模型、定向转换与独立处理，或随新业务理解演进模型时，读取[上下文含义、协作关系与模型演进方法](../methods/context-meaning-model-evolution.md)。

按条件深入：业务规则跨对象，需要划定一致性边界或选择并发保护机制时，读取[从业务不变量到聚合与事务](../methods/invariants-aggregates-transactions.md)。

按条件深入：业务规则跨入口传播，需要比较过程、记录集或对象组织，或对象映射、未保存状态与跨请求编辑的并发和恢复责任不清时；按正文入口只读相关部分，读取[业务逻辑组织、持久化与跨请求工作方法](../methods/logic-persistence-session-boundaries.md)。

按条件深入：需要确定需求信息的提供者与获取方式、确认整理后的含义时，可直达[第1.1节用户代表](../methods/requirements-language-behavior.md#11-按任务选择用户代表)、[第1.2节获取方式](../methods/requirements-language-behavior.md#12-按当前未知选择获取方式)或[第1.3节转述确认](../methods/requirements-language-behavior.md#13-保留来源并确认转述)；同一句需求会导向不同结果、业务承诺互相冲突，或测试预期因领域术语和业务结果尚未澄清而无法确定时，读取[歧义、领域语言与可观察行为方法](../methods/requirements-language-behavior.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
