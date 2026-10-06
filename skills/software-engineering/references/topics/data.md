# 数据与一致性

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 哪些读取必须看到哪些写入？ | [SE-DATA-CONSISTENCY-CONTRACT 把一致性要求写成可观察保证](../rules/se-data-consistency-contract.md) |
| 当前隔离或锁能防住实际竞争吗？ | [SE-DATA-CONCURRENCY-INVARIANTS 从交错执行检验并发控制](../rules/se-data-concurrency-invariants.md) |
| 新旧读写者能安全共存和回退吗？ | [SE-DATA-EVOLUTION 验证混合版本和历史数据兼容](../rules/se-data-evolution.md) |
| 缓存、索引和分析副本怎样恢复一致？ | [SE-DATA-DERIVED-SYNC 为派生数据确定权威源与重建路径](../rules/se-data-derived-sync.md) |

按条件深入：遇到双写或派生状态更新、快照日志衔接、重建对账、派生版本启用或相关恢复问题时，读取[派生更新、重建与对账方法](../methods/data-derived-state-rebuild-reconciliation.md)。

按条件深入：遇到编辑后旧值、读取倒退、复制确认或数据模型与分区取舍时，读取[读取观察、数据组织与分布选择方法](../methods/data-reading-distribution.md)。

按条件深入：业务规则跨对象，需要划定一致性边界或选择并发保护机制时，读取[从业务不变量到聚合与事务](../methods/invariants-aggregates-transactions.md)。

按条件深入：业务规则跨入口传播，需要比较过程、记录集或对象组织，或对象映射、未保存状态与跨请求编辑的并发和恢复责任不清时；按正文入口只读相关部分，读取[业务逻辑组织、持久化与跨请求工作方法](../methods/logic-persistence-session-boundaries.md)。

按条件深入：业务操作跨数据库、消息或外部服务，需要推导提交与确认的崩溃窗口、未知结果恢复、补偿或历史保留条件时，读取[原子效果、外部结果未知与恢复方法](../methods/message-atomic-effect-recovery.md)。

按条件深入：需要选择远程请求粒度、解释逐跳确认，或处理消息交付失败、业务结果未知与异常保留责任时，读取[消息交付、确认与异常处置方法](../methods/message-delivery-acknowledgment.md)。

按条件深入：需要判断重复或乱序消息能否再次处理，选择业务操作身份、本地原子去重、历史结果复用或保留清理条件时，读取[重复、乱序与去重状态方法](../methods/message-idempotency-ordering.md)。

按条件深入：需要改变数据结构、单位或精度，判断新旧读写及历史格式兼容，或安排回填、中断恢复、读写切换和旧结构退出时，读取[混合读写、数据迁移与恢复方法](../methods/mixed-version-data-migration.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
