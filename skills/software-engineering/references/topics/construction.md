# 构建与错误处理

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 拆分后是否更容易理解做什么及为什么？ | [SE-CON-FUNCTION-BOUNDARY 以意图和抽象层级确定函数边界](../rules/se-con-function-boundary.md) |
| 调用者会不会把有状态操作误当成可重复查询？ | [SE-CON-SIDE-EFFECTS 让副作用与顺序约束在接口上可见](../rules/se-con-side-effects.md) |
| 这个条件是可能发生的输入错误，还是代码不应违反的假设？ | [SE-CON-VALIDATE-CONTRACTS 区分外部失败处理与内部断言](../rules/se-con-validate-contracts.md) |
| 失败时继续、降级还是停止，哪一种符合契约？ | [SE-CON-FAILURE-POLICY 根据错误后果确定一致的失败策略](../rules/se-con-failure-policy.md) |
| 错误分类能否帮助调用者作出不同决定？ | [SE-CON-CALLER-ERRORS 按调用者处理方式组织错误接口](../rules/se-con-caller-errors.md) |
| 这个空值是在表示没有结果，还是无法取得结果？ | [SE-CON-ABSENCE-CONTRACT 为空、缺失和失败定义不同语义](../rules/se-con-absence-contract.md) |

按条件深入：需要隔离检查数据、选择依赖替身、核对真实提交，或辨别异步完成、超时及清理责任时，读取[夹具、替身与异步观察方法](../methods/fixtures-doubles-async-observation.md)。

按条件深入：变化牵动无关代码、调用方依赖内部细节，或需要划分模块责任及检查接口行为替换时，读取[从变化需求到模块职责与接口契约](../methods/module-responsibilities-contracts.md)。

按条件深入：存在共享可变状态、跨执行者发布、后台等待或关闭取消责任，需要判断完整原子边界、通知推进与最后资源使用时，读取[共享状态、发布可见性与关闭责任](../methods/shared-state-visibility-shutdown.md)。

按条件深入：同一结构症状仍可能来自独立要求、共同变化或错误依赖，需要在保留、局部提取、窄范围搬移和算法替换候选之间作有依据的选择时，读取[从结构问题到候选变换](../methods/structural-change-candidates.md)。

按条件深入：当前行为已有独立预期，需要选择下一条检查、辨别失败原因、调整实现步幅或根据检查困难改善设计时，读取[反馈步幅与测试驱动设计方法](../methods/tdd-feedback-design.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
