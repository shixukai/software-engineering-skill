# 架构、领域与集成设计

## 目录

- [1. 适用与输入](#1-适用与输入)
- [2. 执行](#2-执行)
- [3. 交付与结束](#3-交付与结束)
- [4. 按需知识](#4-按需知识)

## 1. 适用与输入

- 设计或评审系统架构、模块边界、数据与消息方案

最低输入：

- 业务目标、关键用例和已有架构
- 质量属性、规模范围与团队约束；未知明确列出

决定性未知：

- 影响切分的一致性或独立演进需求
- 故障模型、负载与恢复要求

## 2. 执行

依任务风险裁剪，步骤不是强制文档阶段。

1. 建立上下文、主要数据流、责任和外部依赖；用具体质量场景描述刺激、环境、响应与可度量目标。
2. 围绕业务不变量、变化原因和团队协作比较边界；限界上下文、模块、进程和部署单元分别论证。
3. 针对关键决定比较当前方案、最小改进与必要备选；逐项说明收益、代价、假设、迁移和失败路径。不要为了数量编造无价值方案。
4. 遇到事务、消息、缓存或并发，明确提交、确认、副作用和重试边界；检查重复、乱序、丢失、超时与部分成功。
5. 按风险选择模型推演、原型、负载/故障验证或专家评审；输出决定依据、可推翻条件和后续验证。

## 3. 交付与结束

交付用户实际需要的内容：

- 必要的 Mermaid 上下文/组件/序列图
- 关键决定与备选取舍、接口/数据契约
- 迁移步骤、风险及验证计划

完成依据：

- 关键质量场景都有支持或待验证依据
- 结构和运行保证一致，未把假设包装成事实

停止相应操作的条件：

- 关键不变量或平台语义未知，无法选择安全方案时先取证

避免：

- 默认微服务
- 把某模式当成目标
- 用书籍证明当前架构有缺陷

## 4. 按需知识

按当前问题选择主题、规则或方法章节。任务范围明确时可直接读已定位的章节；先核对该节的适用条件、例外与关联内容，再按判断需要补读，不把定位当作固定阅读边界。此表不要求一次全读。

常用：[架构取舍](../topics/architecture.md)；[领域与边界](../topics/domain.md)；[数据与一致性](../topics/data.md)；[消息与系统集成](../topics/integration.md)。

条件触发：[可靠性与运行](../topics/reliability.md)；[安全](../topics/security.md)；[决策与成本](../topics/economics.md)；[模型与方法](../topics/modeling.md)；[计算与数学基础](../topics/foundations.md)。

本流程直接依赖：[SE-ARCH-QUALITY-TRADEOFF](../rules/se-arch-quality-tradeoff.md)、[SE-ARCH-DISTRIBUTION-BOUNDARY](../rules/se-arch-distribution-boundary.md)、[SE-DOMAIN-CONTEXT](../rules/se-domain-context.md)、[SE-DATA-CONSISTENCY-CONTRACT](../rules/se-data-consistency-contract.md)。

按条件深入：需要围绕驱动因素逐轮细化设计时，可直达[第3.2节设计迭代](../methods/architecture-drivers-tradeoffs.md#32-围绕当前目标迭代设计)；对变化做轻量场景复评时，可直达[第8.3节轻量评估](../methods/architecture-drivers-tradeoffs.md#83-对变化和未评部分做轻量评估)；新业务、质量目标或关键约束要求改变模块、部署、数据或依赖边界，需要比较候选并规划演进时，读取[从架构驱动因素到方案取舍与演进](../methods/architecture-drivers-tradeoffs.md)。

按条件深入：同名概念在身份、状态、规则或决定责任上发生冲突，需要比较共享模型、定向转换与独立处理，或随新业务理解演进模型时，读取[上下文含义、协作关系与模型演进方法](../methods/context-meaning-model-evolution.md)。

按条件深入：遇到双写或派生状态更新、快照日志衔接、重建对账、派生版本启用或相关恢复问题时，读取[派生更新、重建与对账方法](../methods/data-derived-state-rebuild-reconciliation.md)。

按条件深入：变化涉及个人信息用途、字段与接收者、保留删除恢复或关键任务交互时；按实际变化选择相关段落，读取[数据用途、生命周期与关键交互](../methods/data-purpose-lifecycle-interaction.md)。

按条件深入：遇到编辑后旧值、读取倒退、复制确认或数据模型与分区取舍时，读取[读取观察、数据组织与分布选择方法](../methods/data-reading-distribution.md)。

按条件深入：需要分配端到端期限、判断副作用重试、定义熔断事件及真实资源隔离，或在混合负载、慢依赖、容量丢失和持续积压下选择保护与恢复动作时，读取[期限、重试、隔离与过载恢复方法](../methods/deadlines-retries-overload-recovery.md)。

按条件深入：业务规则跨对象，需要划定一致性边界或选择并发保护机制时，读取[从业务不变量到聚合与事务](../methods/invariants-aggregates-transactions.md)。

按条件深入：业务规则跨入口传播，需要比较过程、记录集或对象组织，或对象映射、未保存状态与跨请求编辑的并发和恢复责任不清时；按正文入口只读相关部分，读取[业务逻辑组织、持久化与跨请求工作方法](../methods/logic-persistence-session-boundaries.md)。

按条件深入：业务操作跨数据库、消息或外部服务，需要推导提交与确认的崩溃窗口、未知结果恢复、补偿或历史保留条件时，读取[原子效果、外部结果未知与恢复方法](../methods/message-atomic-effect-recovery.md)。

按条件深入：需要选择远程请求粒度、解释逐跳确认，或处理消息交付失败、业务结果未知与异常保留责任时，读取[消息交付、确认与异常处置方法](../methods/message-delivery-acknowledgment.md)。

按条件深入：需要判断重复或乱序消息能否再次处理，选择业务操作身份、本地原子去重、历史结果复用或保留清理条件时，读取[重复、乱序与去重状态方法](../methods/message-idempotency-ordering.md)。

按条件深入：需要改变数据结构、单位或精度，判断新旧读写及历史格式兼容，或安排回填、中断恢复、读写切换和旧结构退出时，读取[混合读写、数据迁移与恢复方法](../methods/mixed-version-data-migration.md)。

按条件深入：变化牵动无关代码、调用方依赖内部细节，或需要划分模块责任及检查接口行为替换时，读取[从变化需求到模块职责与接口契约](../methods/module-responsibilities-contracts.md)。

按条件深入：需要联合计算持久队列、结果历史和隔离消息的增长及保留，处理并发清理和空间耗尽，或选择备份链、恢复范围与恢复旧数据后的当前控制时，读取[持续资源、保留、清理与恢复方法](../methods/resource-retention-cleanup-recovery.md)。

按条件深入：变化涉及受保护读取、主体权限、数据流或实际控制时；先核对变化与保护结果，小型无关文字修改不展开安全全表，读取[信任边界、威胁与控制证据](../methods/trust-boundaries-threat-control-evidence.md)。

按条件深入：需要从用户成功含义定义服务指标与目标，计算滚动预算、处理分组或观测缺失，并确定告警、发布限制和恢复行动时，读取[用户结果、SLO、预算与告警行动方法](../methods/user-outcomes-slo-alert-actions.md)。
