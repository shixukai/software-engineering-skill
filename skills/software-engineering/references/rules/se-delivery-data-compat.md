# SE-DELIVERY-DATA-COMPAT 把数据库迁移与应用回退分别证明

## 目录

- [1. 判断问题](#1-判断问题)
- [2. 条件与证据](#2-条件与证据)
- [3. 操作与取舍](#3-操作与取舍)
- [4. 验证与反例](#4-验证与反例)
- [5. 来源](#5-来源)

## 1. 判断问题

应用切回旧版后，新旧数据还能被正确处理吗？

## 2. 条件与证据

适用：

- 修改持久化结构或数据含义
- 滚动发布、共享数据库或跨版本运行

不适用或需调整：

- 不得把有价值的持久数据当成可随时重建的临时夹具
- 不可逆变换不能伪装成有完整反向迁移
- 未经权限与数据保护条件确认不执行生产迁移

必要证据：

- 现有与目标 schema、数据约束和应用版本矩阵
- 迁移过程中的写入、锁定、容量及停机约束
- 备份恢复、不可逆变化和外部副作用

## 3. 操作与取舍

1. 版本化迁移，列明每一步的前置版本、后置版本、幂等或重复执行限制与失败处理。
2. 优先评估兼容过渡，逐步安排结构扩展、应用读写切换、数据迁移与旧结构收缩；每个中间状态都验证仍在运行的旧新版本，退出回退窗口后再移除旧支持。具体顺序按依赖和读写语义确定。
3. 明确回退是否丢失发布后的交易、关系或新字段；单纯恢复旧备份不满足保留新写入的要求。
4. 在允许的隔离数据上验证正常迁移、中断、旧新应用共存和恢复；覆盖约束违例与新增写入，而不只测试空数据库。
5. 兼容迁移不可行时比较停写、备份恢复、前向修复和经验证的补偿，记录所需时间与数据损失边界。

- 保持双版本兼容延长过渡代码寿命，但允许分离应用部署与数据变更
- 备份只解决特定恢复点；持续写入及不可逆副作用增加恢复复杂度

## 4. 验证与反例

- 兼容矩阵与恢复边界有证据
- 迁移状态可识别，部分完成不会被误认成功
- 保留数据的要求在回退检查中明确验证

反例：新增约束在空库迁移成功，现存记录违约导致生产迁移中断；自动反向脚本又删除了发布后新增数据。

## 5. 来源

以下支持方法选择，不能据此证明当前项目存在问题。标记说明：原书观点、多源综合、工程适配分别对应来源主张及本规则的加工关系。

- **工程适配**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第12章：Versioning Your Database / Managing Orchestrated Changes。支持：PDF362–365讨论版本化脚本、约束/数据删除限制与多应用依赖。。定位：PDF 文件页 362；印刷页 328。来源标识：`continuous-delivery`。
- **工程适配**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第12章：Rolling Back without Losing Data / Decoupling Application Deployment from Database Migration。支持：PDF365–367区分保留新交易与应用回退，支持兼容过渡。。定位：PDF 文件页 365；印刷页 331。来源标识：`continuous-delivery`。
- **多源综合**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第10章：Rolling Back by Redeploying the Previous Good Version。支持：旧版本重部署可能停机并丢失备份后的新数据。。定位：PDF 文件页 294；印刷页 260。来源标识：`continuous-delivery`。

详细身份与版本见[来源目录](../sources.md)。
