# 集成交付

## 目录

- [1. 按问题选择](#1-按问题选择)
- [2. 使用边界](#2-使用边界)

## 1. 按问题选择

只读取与当前决定有关的条目，不默认展开全部规则。

| 问题 | 规则 |
|---|---|
| 哪些集成或组织假设必须先被最小实现验证？ | [SE-DELIVERY-SKELETON 早期贯通最小构建、部署与验收链路](../rules/se-delivery-skeleton.md) |
| 准备发布的东西是否就是被验证的那一份？ | [SE-DELIVERY-PROVENANCE 锁定完整构建基线并晋级同一制品](../rules/se-delivery-provenance.md) |
| 什么条件允许这个版本进入下一阶段？ | [SE-DELIVERY-GATES 让每个交付关卡产生明确证据](../rules/se-delivery-gates.md) |
| 重跑或部分失败后，部署会留下什么状态？ | [SE-DELIVERY-IDEMPOTENT 部署先验证前提，再收敛到声明状态](../rules/se-delivery-idempotent.md) |
| 何时继续、暂停或恢复服务，由谁判断？ | [SE-DELIVERY-RELEASE 在发布前明确执行、观察与恢复条件](../rules/se-delivery-release.md) |
| 应用切回旧版后，新旧数据还能被正确处理吗？ | [SE-DELIVERY-DATA-COMPAT 把数据库迁移与应用回退分别证明](../rules/se-delivery-data-compat.md) |

按条件深入：需要贯通最薄交付路径、选择发布候选，或判断产物、配置与环境变化后哪些证据支持进入下一阶段时，读取[同一制品与晋级证据方法](../methods/artifact-promotion-evidence.md)。

按条件深入：部署已有部分完成、结果未知或迟到动作，或需要按停机、容量、观察及共享状态选择发布和退出方式时，读取[部署中断与收敛方法](../methods/deployment-interruption-convergence.md)。

按条件深入：需要改变数据结构、单位或精度，判断新旧读写及历史格式兼容，或安排回填、中断恢复、读写切换和旧结构退出时，读取[混合读写、数据迁移与恢复方法](../methods/mixed-version-data-migration.md)。

## 2. 使用边界

需要先满足规则的证据与适用条件。多个来源冲突时比较目标、上下文和代价；无法消解则保留分支与待核实事项。已有项目约定和用户授权决定实际执行范围。
