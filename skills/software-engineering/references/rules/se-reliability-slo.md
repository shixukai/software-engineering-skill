# SE-RELIABILITY-SLO 从用户结果制定可靠性目标

## 目录

- [1. 判断问题](#1-判断问题)
- [2. 条件与证据](#2-条件与证据)
- [3. 操作与取舍](#3-操作与取舍)
- [4. 验证与反例](#4-验证与反例)
- [5. 来源](#5-来源)

## 1. 判断问题

怎样量化足够可靠并决定改进优先级？

## 2. 条件与证据

适用：

- 建立服务运行目标或平衡交付速度与可靠性

不适用或需调整：

- 缺乏服务用户或可解释指标的局部任务，不强制建立SLO体系

必要证据：

- 用户重要操作与失败影响
- 可测SLI的范围、分母、窗口和采集点
- 业务负责人认可的目标与变更决策权限

## 3. 操作与取舍

1. 选择少量能反映用户结果的SLI，区分成功、延迟、数据耐久与正确性。
2. 定义测量口径、窗口、目标和排除项；区分内部目标SLO与带后果的约定SLA。
3. 按约定目标计算可接受失败预算，明确接近或耗尽预算时如何调整发布和可靠性工作。
4. 目标和政策由有权责任人确认；安全、隐私或必须保持的业务不变量不能被一般可用性预算抵销。

- 目标过严会挤占成本与演进，过松损害用户。
- 平均可用性可能掩盖关键群体或操作受损，需要适当分组。

## 4. 验证与反例

- 用定义重算SLI得到一致结果
- 预算政策有责任主体和实际可执行动作
- 指标口径不会把真正用户失败从分母中任意排除

反例：用服务器存活率宣称服务达标，关键用户操作持续返回错误内容却未计入失败。

## 5. 来源

以下支持方法选择，不能据此证明当前项目存在问题。标记说明：原书观点、多源综合、工程适配分别对应来源主张及本规则的加工关系。

- **多源综合**：Site Reliability Engineering: How Google Runs Production Systems，第3章：Risk Tolerance of Services；Motivation for Error Budgets。支持：风险容忍、错误预算和团队共同决策；隐私失效与普通可用性损失性质不同。。定位：ch008.xhtml#motivation-for-error-budgets14。来源标识：`site-reliability-engineering`。
- **多源综合**：Site Reliability Engineering: How Google Runs Production Systems，第4章：Service Level Terminology；Indicators/Objectives in Practice。支持：SLI、SLO、SLA、测量口径与用户需求之间的关系。。定位：ch009.xhtml#service-level-terminology。来源标识：`site-reliability-engineering`。

详细身份与版本见[来源目录](../sources.md)。
