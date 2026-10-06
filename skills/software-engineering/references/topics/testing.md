# 测试

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 这个测试通过时，究竟证明了什么？ | [SE-TEST-ORACLE 先确定预期依据与可观察结果](../rules/se-test-oracle.md) |
| 哪些风险需要在哪一层取得证据？ | [SE-TEST-RISK-LAYERS 按风险分配测试层次和反馈成本](../rules/se-test-risk-layers.md) |
| 下一步应验证什么，步子需要多小？ | [SE-TEST-INCREMENT 依据不确定性调整测试驱动步幅](../rules/se-test-increment.md) |
| 失败来自产品还是测试之间的污染？ | [SE-TEST-INDEPENDENT 让夹具和清理支持独立重复运行](../rules/se-test-independent.md) |
| 这个替身在帮助观察，还是在制造虚假通过？ | [SE-TEST-DOUBLES 用替身控制边界而不替换待证行为](../rules/se-test-doubles.md) |
| 测试为何频繁随无关改动一起坏掉？ | [SE-TEST-MAINTAIN 让测试说明一个行为并给出可定位失败](../rules/se-test-maintain.md) |
| 测试结束时是否真的观察到了本次异步操作？ | [SE-TEST-ASYNC 异步测试等待可观察完成并保存失败证据](../rules/se-test-async.md) |

按条件深入：明确行为需要形成可检查的预期结果，或需求变化可能影响接口、检查、运行及已有结论时，读取[验收依据与变更影响方法](../methods/acceptance-evidence-change-impact.md)。

按条件深入：需要隔离检查数据、选择依赖替身、核对真实提交，或辨别异步完成、超时及清理责任时，读取[夹具、替身与异步观察方法](../methods/fixtures-doubles-async-observation.md)。

按条件深入：需要修改难测的既有代码、建立行为保护，或在保持客户契约的前提下分步重构并接入新行为时，读取[从行为保护到渐进重构](../methods/refactoring-legacy-safety.md)。

按条件深入：当前行为已有独立预期，需要选择下一条检查、辨别失败原因、调整实现步幅或根据检查困难改善设计时，读取[反馈步幅与测试驱动设计方法](../methods/tdd-feedback-design.md)。

按条件深入：同一行为涉及局部逻辑、接口或真实协作，需要按风险选择验证范围及证据成本时，读取[风险、独立预期与验证层次方法](../methods/test-risk-oracles-layers.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
