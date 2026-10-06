# 重构与遗留演进

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 把这段代码移到新函数后，值、顺序和副作用是否保持？ | [SE-CON-EXTRACT-SAFE 提取函数时逐项保护数据流和控制流](../rules/se-con-extract-safe.md) |
| 当前一步是在改结构还是改功能，失败后如何定位？ | [SE-CON-REFACTOR-STEPS 用可验证的小步保持重构行为](../rules/se-con-refactor-steps.md) |
| 所有使用者都在本次改动控制范围内吗？ | [SE-CON-PUBLISHED-CONTRACT 对无法同时修改的调用者保留迁移兼容](../rules/se-con-published-contract.md) |
| 哪些现有行为需要在这次修改中保护？ | [SE-CON-LEGACY-CHARACTERIZE 用特征测试记录当前行为并标识可疑结果](../rules/se-con-legacy-characterize.md) |
| 无需修改待测试调用处，能在哪里替换依赖行为？ | [SE-CON-LEGACY-TEST-SEAM 为测试选择可控制的接缝与激活点](../rules/se-con-legacy-test-seam.md) |
| 能否把新增能力做成独立可测的小块？ | [SE-CON-LEGACY-SPROUT 在旧代码难测时隔离新行为并核对接入](../rules/se-con-legacy-sprout.md) |
| 为了获得测试反馈，最少必须改哪些代码？ | [SE-CON-LEGACY-CONSERVATIVE 首个测试建立前限制解依赖改动](../rules/se-con-legacy-conservative.md) |
| 现有测试能否感知这次可能引入的错误？ | [SE-CON-LEGACY-TARGETED 验证被改路径和接线，不只看测试通过](../rules/se-con-legacy-targeted.md) |
| 现在重构的收益是否值得本次扩大改动？ | [SE-CON-REFACTOR-SCOPE 让重构服务当前任务或明确的维护收益](../rules/se-con-refactor-scope.md) |

按条件深入：已确认算法变体或受支持父类扩展点，需要比较条件、函数、策略、继承与组合并追踪选择、状态和资源责任时，读取[条件、函数、策略与对象协作](../methods/conditional-strategy-composition-inheritance.md)。

按条件深入：遗留改动经多个客户、共享对象或父子类分叉，或需在难构造旧类中选择新生/外覆过渡并核对旧入口时，读取[从分叉影响到遗留代码的有限过渡](../methods/legacy-impact-transition.md)。

按条件深入：需要修改难测的既有代码、建立行为保护，或在保持客户契约的前提下分步重构并接入新行为时，读取[从行为保护到渐进重构](../methods/refactoring-legacy-safety.md)。

按条件深入：同一结构症状仍可能来自独立要求、共同变化或错误依赖，需要在保留、局部提取、窄范围搬移和算法替换候选之间作有依据的选择时，读取[从结构问题到候选变换](../methods/structural-change-candidates.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
