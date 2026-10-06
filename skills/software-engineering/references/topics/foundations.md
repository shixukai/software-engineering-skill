# 计算与数学基础

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 规模或输入分布变化后，当前算法还能满足预算吗？ | [SE-FOUND-ALGORITHM 按输入规模和情形估算算法成本](../rules/se-found-algorithm.md) |
| 所选表示是否维护业务关系并支持主要操作？ | [SE-FOUND-DATA-STRUCTURE 从操作和不变量选择数据结构](../rules/se-found-data-structure.md) |
| 资源由谁释放，部分失败后还剩什么？ | [SE-FOUND-RESOURCE 让资源拥有者覆盖每条退出路径](../rules/se-found-resource.md) |
| 各个操作线程安全，组合后的业务步骤也安全吗？ | [SE-FOUND-CONCURRENCY 分别证明共享状态的原子性与可见性](../rules/se-found-concurrency.md) |
| 没有数据错误时，任务是否仍可能永远等下去？ | [SE-FOUND-LIVENESS 检查等待、关闭和资源获取是否能推进](../rules/se-found-liveness.md) |
| 逻辑改写保持真值，也保持求值行为吗？ | [SE-FOUND-LOGIC 把条件组合变成可检查的判定](../rules/se-found-logic.md) |
| 输入合法时，中间运算、转换或舍入会越界吗？ | [SE-FOUND-NUMERIC 沿中间结果核对数值范围与精度](../rules/se-found-numeric.md) |

按条件深入：输入输出建模、数据结构/算法候选或正确性与规模成本需要具体比较时，读取[问题建模、算法选择与正确性验证](../methods/algorithm-modeling-design-validation.md)。

按条件深入：数值单位、中间范围、舍入、条件求值或表示替换需要具体推导时，读取[数值范围、条件求值与表示选择](../methods/numeric-range-evaluation-representation.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
