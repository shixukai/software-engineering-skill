# 消息与系统集成

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 消息在什么时刻被认为安全，失败后由谁处理？ | [SE-INTEGRATION-DELIVERY 明确持久交付与不可处理消息的边界](../rules/se-integration-delivery.md) |
| 重试会不会重复或倒退业务状态？ | [SE-INTEGRATION-IDEMPOTENCY 把重复与乱序分别纳入副作用协议](../rules/se-integration-idempotency.md) |
| 所谓恰好一次到底覆盖哪些效果？ | [SE-INTEGRATION-ATOMIC-EFFECT 核实消费确认与业务效果的原子范围](../rules/se-integration-atomic-effect.md) |

按条件深入：遇到双写或派生状态更新、快照日志衔接、重建对账、派生版本启用或相关恢复问题时，读取[派生更新、重建与对账方法](../methods/data-derived-state-rebuild-reconciliation.md)。

按条件深入：需要分配端到端期限、判断副作用重试、定义熔断事件及真实资源隔离，或在混合负载、慢依赖、容量丢失和持续积压下选择保护与恢复动作时，读取[期限、重试、隔离与过载恢复方法](../methods/deadlines-retries-overload-recovery.md)。

按条件深入：业务操作跨数据库、消息或外部服务，需要推导提交与确认的崩溃窗口、未知结果恢复、补偿或历史保留条件时，读取[原子效果、外部结果未知与恢复方法](../methods/message-atomic-effect-recovery.md)。

按条件深入：需要选择远程请求粒度、解释逐跳确认，或处理消息交付失败、业务结果未知与异常保留责任时，读取[消息交付、确认与异常处置方法](../methods/message-delivery-acknowledgment.md)。

按条件深入：需要判断重复或乱序消息能否再次处理，选择业务操作身份、本地原子去重、历史结果复用或保留清理条件时，读取[重复、乱序与去重状态方法](../methods/message-idempotency-ordering.md)。

按条件深入：需要联合计算持久队列、结果历史和隔离消息的增长及保留，处理并发清理和空间耗尽，或选择备份链、恢复范围与恢复旧数据后的当前控制时，读取[持续资源、保留、清理与恢复方法](../methods/resource-retention-cleanup-recovery.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
