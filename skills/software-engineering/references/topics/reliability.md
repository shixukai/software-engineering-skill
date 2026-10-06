# 可靠性与运行

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 依赖变慢时何时停止等待和消耗资源？ | [SE-RELIABILITY-DEADLINE 给等待和执行设置端到端预算](../rules/se-reliability-deadline.md) |
| 重试有恢复收益还是只会放大故障？ | [SE-RELIABILITY-RETRY-BUDGET 以故障类型和预算决定重试](../rules/se-reliability-retry-budget.md) |
| 一个依赖或租户能否耗尽所有能力？ | [SE-RELIABILITY-ISOLATION 让局部失效保持局部](../rules/se-reliability-isolation.md) |
| 系统持续运行后会因积累而失效吗？ | [SE-RELIABILITY-STEADY-STATE 为积累的资源设计上限与回收](../rules/se-reliability-steady-state.md) |
| 怎样量化足够可靠并决定改进优先级？ | [SE-RELIABILITY-SLO 从用户结果制定可靠性目标](../rules/se-reliability-slo.md) |
| 发现的是用户受损、资源风险还是无关噪声？ | [SE-RELIABILITY-MONITORING 让监测支持行动和诊断](../rules/se-reliability-monitoring.md) |
| 容量边界在哪里，越界后还能保留多少有效服务？ | [SE-RELIABILITY-CAPACITY 验证过载后的存活与恢复](../rules/se-reliability-capacity.md) |
| 怎样恢复服务而不让并行操作相互干扰？ | [SE-RELIABILITY-INCIDENT 按影响组织故障响应](../rules/se-reliability-incident.md) |
| 故障之后怎样降低复发概率或影响？ | [SE-RELIABILITY-POSTMORTEM 把复盘转成可验证改进](../rules/se-reliability-postmortem.md) |

按条件深入：需要分配端到端期限、判断副作用重试、定义熔断事件及真实资源隔离，或在混合负载、慢依赖、容量丢失和持续积压下选择保护与恢复动作时，读取[期限、重试、隔离与过载恢复方法](../methods/deadlines-retries-overload-recovery.md)。

按条件深入：需要协调多人或跨时段的事件响应、明确交接，或从复盘证据选择改进并判断措施有效性时，读取[事件交接与复盘改进方法](../methods/incident-handoff-learning.md)。

按条件深入：需要联合计算持久队列、结果历史和隔离消息的增长及保留，处理并发清理和空间耗尽，或选择备份链、恢复范围与恢复旧数据后的当前控制时，读取[持续资源、保留、清理与恢复方法](../methods/resource-retention-cleanup-recovery.md)。

按条件深入：存在共享可变状态、跨执行者发布、后台等待或关闭取消责任，需要判断完整原子边界、通知推进与最后资源使用时，读取[共享状态、发布可见性与关闭责任](../methods/shared-state-visibility-shutdown.md)。

按条件深入：需要从用户成功含义定义服务指标与目标，计算滚动预算、处理分组或观测缺失，并确定告警、发布限制和恢复行动时，读取[用户结果、SLO、预算与告警行动方法](../methods/user-outcomes-slo-alert-actions.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
