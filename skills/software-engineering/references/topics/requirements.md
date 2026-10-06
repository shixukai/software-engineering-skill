# 需求与验收

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 什么事实足以表明需求得到满足？ | [SE-REQ-ACCEPTANCE 把需求写成可检查的行为与约束](../rules/se-req-acceptance.md) |
| 这一变化还会使哪些已确认结论失效？ | [SE-REQ-CHANGE 用关系追踪需求变更的影响](../rules/se-req-change.md) |

按条件深入：明确行为需要形成可检查的预期结果，或需求变化可能影响接口、检查、运行及已有结论时，读取[验收依据与变更影响方法](../methods/acceptance-evidence-change-impact.md)。

按条件深入：需要确定需求信息的提供者与获取方式、确认整理后的含义时，可直达[第1.1节用户代表](../methods/requirements-language-behavior.md#11-按任务选择用户代表)、[第1.2节获取方式](../methods/requirements-language-behavior.md#12-按当前未知选择获取方式)或[第1.3节转述确认](../methods/requirements-language-behavior.md#13-保留来源并确认转述)；同一句需求会导向不同结果、业务承诺互相冲突，或测试预期因领域术语和业务结果尚未澄清而无法确定时，读取[歧义、领域语言与可观察行为方法](../methods/requirements-language-behavior.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
