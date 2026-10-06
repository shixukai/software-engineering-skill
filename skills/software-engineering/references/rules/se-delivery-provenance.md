# SE-DELIVERY-PROVENANCE 锁定完整构建基线并晋级同一制品

## 目录

- [1. 判断问题](#1-判断问题)
- [2. 条件与证据](#2-条件与证据)
- [3. 操作与取舍](#3-操作与取舍)
- [4. 验证与反例](#4-验证与反例)
- [5. 来源](#5-来源)

## 1. 判断问题

准备发布的东西是否就是被验证的那一份？

## 2. 条件与证据

适用：

- 构建、打包、依赖更新或制品晋级
- 需要重现或回滚一个已发布版本

不适用或需调整：

- 不同目标架构确需不同构建时分别生成和验证，不冒称跨目标字节一致
- 不能把密钥、个人数据或无关构建产物一并提交到源仓库

必要证据：

- 源码修订、依赖锁定及工具链版本
- 构建脚本、配置模式、环境基线与迁移版本
- 制品标识、校验值和各阶段验证记录

## 3. 操作与取舍

1. 记录重建所需的源码、脚本、精确依赖和工具链；环境差异作为受控配置管理。秘密仅保留安全引用及注入要求。
2. 从受控基线构建一次并生成稳定制品标识；下游验收与发布使用该制品，防止晋级时重新编译悄悄改变内容。
3. 配置变化也视为行为变化，保存实际配置版本和兼容关系；制品、配置、数据迁移共同组成发布清单。
4. 检查旧版本恢复所需工件与基线仍可取得；重建成功与已发布制品一致性分别验证。

- 保留依赖和制品提高可追溯性但消耗存储与治理成本
- 可重建并不自动意味着逐位确定性；必须声明当前重现标准

## 4. 验证与反例

- 发布制品的校验值与验收记录一致
- 依赖与环境不依赖某位工程师机器上的未记录状态
- 清单可定位制品、配置和迁移的匹配组合且不泄露秘密

反例：验收环境用依赖版本A打包通过，发布阶段重新解析浮动依赖得到B，却沿用A的测试结论。

## 5. 来源

以下支持方法选择，不能据此证明当前项目存在问题。标记说明：原书观点、多源综合、工程适配分别对应来源主张及本规则的加工关系。

- **工程适配**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第2章：Using Version Control / Managing Dependencies / Managing Software Configuration。支持：PDF67、69、72–74说明构建输入、精确依赖与配置风险；秘密引用是工程适配。。定位：PDF 文件页 67；印刷页 33。来源标识：`continuous-delivery`。
- **工程适配**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第2章：Managing Your Environments。支持：PDF83–85支持受控环境基线。。定位：PDF 文件页 83；印刷页 49。来源标识：`continuous-delivery`。
- **工程适配**：Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation，第5章：Only Build Your Binaries Once。支持：PDF147–150支持同一制品晋级与代码配置分离。。定位：PDF 文件页 147；印刷页 113。来源标识：`continuous-delivery`。

详细身份与版本见[来源目录](../sources.md)。
