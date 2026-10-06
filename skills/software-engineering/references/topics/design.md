# 模块和接口设计

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 这次变化应该被哪个边界吸收？ | [SE-CON-CHANGE-ISOLATION 按变化原因隔离实现，并计算提前抽象的成本](../rules/se-con-change-isolation.md) |
| 这些相似实现是否表达同一条需要共同变化的知识？ | [SE-CON-KNOWLEDGE-DRY 消除同一知识的多份维护责任](../rules/se-con-knowledge-dry.md) |
| 复用实现是否需要暴露父类内部结构？ | [SE-CON-COMPOSITION 按替换需求和契约选择组合或继承](../rules/se-con-composition.md) |
| 引入这个模式究竟解决哪个已经存在的设计问题？ | [SE-CON-PATTERN-SELECTION 从需要隔离的变化选择模式](../rules/se-con-pattern-selection.md) |
| 算法变体是否需要独立替换或演进？ | [SE-CON-STRATEGY-VARIANTS 仅在算法变体具有独立价值时提取策略](../rules/se-con-strategy-variants.md) |
| 业务代码是否需要直接知道第三方接口的全部细节？ | [SE-CON-DEPENDENCY-BOUNDARY 用窄接口和学习性测试约束外部依赖](../rules/se-con-dependency-boundary.md) |

按条件深入：已确认算法变体或受支持父类扩展点，需要比较条件、函数、策略、继承与组合并追踪选择、状态和资源责任时，读取[条件、函数、策略与对象协作](../methods/conditional-strategy-composition-inheritance.md)。

按条件深入：变化牵动无关代码、调用方依赖内部细节，或需要划分模块责任及检查接口行为替换时，读取[从变化需求到模块职责与接口契约](../methods/module-responsibilities-contracts.md)。

按条件深入：同一结构症状仍可能来自独立要求、共同变化或错误依赖，需要在保留、局部提取、窄范围搬移和算法替换候选之间作有依据的选择时，读取[从结构问题到候选变换](../methods/structural-change-candidates.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
