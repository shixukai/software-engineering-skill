# 来源目录与权利边界

本目录提供来源身份和书目定位。本目录保留来源质量及拒用限制，各方法与规则说明具体采用条件；未列出的章节不表示已核读。版本未确认的来源保持未确认。当前语言、平台和标准应另查对应版本的权威资料。

来源文件、完整提取文本、原书图像和书例代码均不随本包分发。列出来源不表示本项目拥有第三方作品的再许可权，也不表示来源作者认可本项目。第三方作品受其原有权利与许可约束；项目的 MIT 许可证不改变这些权利。

以下书目信息来自项目现有登记，未在本次整理中重新做全面书目核查。

## Accelerate: The Science of Lean Software and DevOps

标识：`accelerate`。

作者：Nicole Forsgren、Jez Humble、Gene Kim。

版本：2018 First Edition。

- 只采用方法中列出的有限主张及位置，不代表整章或全书采用。
- 第2章前置时间以成功生产运行为终点，第14章以可部署状态为终点，保留两种定义；未核实现行官方 DORA 标准或外部勘误。
- 区分四项指标分群、三项指标构念及单项关系；保留2016年中低组例外，效度与信度结论属于作者研究报告。
- 非概率样本、跨年不连接、分析类型及因果外推均有限制；不使用历史分组阈值或收益承诺。研究未独立复现。

## ACM Code of Ethics and Professional Conduct (2018)

标识：`acm-ethics-2018`。

来源：[官方页面或文档](https://www.acm.org/binaries/content/assets/about/acm-code-of-ethics-booklet.pdf)。

- 只采用规范条文；未将案例研究作为测试输入。

## The Algorithm Design Manual

标识：`algorithm-design-manual`。

作者：Steven S. Skiena。

版本：2020 Third Edition。

- 第三版原件为812文件页，存在原件空页及页树重复警告；已采用位置的有限核读不能认证整本文件的完整性。
- 自动解析曾将页眉误认作章节；章节范围须按真实目录及正文定位。
- 每条采用只限明确选择的正文概念，已读邻文不全部采用；不声明全书核读。
- 原书、页文本与渲染图不是运行依赖；静态推导不能证明当前平台行为或真实工程效果。

## The Algorithm Design Manual, Second Edition

标识：`algorithm-design-manual-2e-2008`。

作者：Steven S. Skiena。

版本：2008 Second Edition。

- 第二版原件为739文件页。文本提取出现 Bad annotation destination 警告；该警告不能直接证明正文缺失。
- 自动解析可能误认页眉与章节，章节范围须按该版真实目录及正文定位，不能套用第三版页码。
- 只采用明确选择的正文概念；邻文不全部采用，有限核读不能认证整本文件完整性，也不代表全书核读。
- 原书、页文本与渲染图不是运行依赖；静态推导不能证明当前平台行为或真实工程效果。

## Clean Code: A Handbook of Agile Software Craftsmanship

标识：`clean-code`。

作者：Robert C. Martin。

版本：未确认。

- 部分代码无专门代码标签，已回查采用段的原始XHTML；图8-2已看原图。
- 行数、每类都建接口、全面取消null和checked异常等偏好不推广为硬要求。
- try/catch不自动赋予事务回滚；命令查询分离不可破坏所需原子性。
- 历史Java/log4j示例不作为当前依赖行为证明；学习性测试也有维护成本。
- Java 5 容器性能、历史 API、字节码路径数量及具体框架行为均不作为现行保证。
- 限制共享和逻辑隔离不证明跨线程可见性；实际同步保证需核实语言/库文档。
- 不采用20行或一两层缩进为硬要求。
- 清单3-1、3-2、3-7和被引用4-7没有全文核读。
- 未执行或证明HtmlUtil变换。

## Code Complete

标识：`code-complete`。

作者：Steve McConnell。

版本：第2版。

- 采用范围为列出的节/段，不代表35章通读。
- 原生标记可保留代码但不保证示例符合当前语言版本；不复制为实现。
- 历史效果百分比、速度、代码行数、设备与DES调优表仅作历史背景。
- 25.4 CPU计时建议只适用于计算消耗分析；端到端等待指标的适配在规则中标注。
- 整数例12-1 原代码使用1000000，相邻解释出现100000及符号/数值不一致；仅采用“检查中间溢出”原则，不引用其计算结果。
- 不将浮点类型作为保持精确整数结果的通用溢出解法；比较容差不采用书例默认常数。
- 短路语义是目标语言/运算符性质，逻辑等价不自动保证求值行为相同。
- 3.5 明确面向评估已有架构；本篇架构生成与实验协议为多源综合，不能归为该节完整现成方法。
- 6.2例6-5仍声明 public ListContainer，正文却称容器表示已隐藏并反对该继承，原生标记确认此不一致；仅采用相邻一致抽象/隐藏容器的论证，不把该例作为正确C++实现。
- 6.2 Point getter/setter被称perfect encapsulation，不外推为所有多字段不变量已维护；需要本篇的完整变更操作和状态论证。
- 5.3把sin角度举例为degrees只作接口明确的示意，不能用于确定实际数学API单位；平台契约另核实。
- 所列采用段落不构成独立完整的业务不变量、事务保证、失败原子性、并发安全或安全输入验证方法；相关方法须由另列来源或明确的工程综合支持。
- 不采用历史效果倍率、参数个数硬阈值、语言/编译器绝对保证或透明性能论断；具体实现仍依语言版本、值/引用和生命周期语义。
- 直接、索引和阶梯访问在此仅列名，后续成员未读。
- 不继承固定性能结论或当前Unicode、Java保证。
- 缺失、重复、索引范围和版本一致性属于后续题设责任。

## Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation

标识：`continuous-delivery`。

作者：Jez Humble、David Farley。

版本：未确认。

- 仅采用所列章节范围，不声称全书实施体系已经经过当前工具链验证。
- 现代制品校验清单、配置安全引用、风险到验证映射、关卡状态与执行授权均标工程适配；原书只支持各条所列的基础思想。
- 数据库兼容顺序必须按当前读写语义验证，不将书中简化过程当作适用于所有迁移的算法。

## Cornell CS312 Lecture 12: Asymptotic Complexity

标识：`cornell-asymptotic`。

来源：[官方页面或文档](https://www.cs.cornell.edu/courses/cs312/2003sp/lectures/lec12.html)。

- 课程历史硬件例仅作上下文，不用于现行性能估计。
- 不采用正文后续将 times1/times2 线性/对数标签颠倒的总结句，以及 little-o 小节的重复自指句。

## Designing Data-Intensive Applications

标识：`data-intensive-applications`。

作者：Martin Kleppmann。

版本：未确认。

- 所用文件是社区中文译本，不能改标为出版商授权中文版或新版内容；原版版次仍待核实，未逐句核对英文原著。
- 原生 HTML 保留锚点，但段落提取存在列表重复；重复次数不作为观点权重。
- 图示核查只支持已明确采用的位置，未采用的公式、代码和图表不计为审定。
- 架构方法不把各服务 p99 简单相加或取最大当作整链 p99，也不将历史数量级增长当作统一重构阈值。
- 读取与分布方法仅采用所列连续正文；这些片段不能认证关键图示、代码、公式、完整协议及现行产品实现。
- 派生方法仅采用第11章主体0–336及第12章0–327中列明的原则；第12章401–410的小结不能替代328–400正文。未读正文、完整算法、精确图码、数学结论及当前产品仍未获认证。

## Domain-Driven Design Reference (Eric Evans, 2015-03)

标识：`ddd-reference-2015`。

作者：Eric Evans。

原作品登记许可：CC BY 4.0。详见[许可条款](https://creativecommons.org/licenses/by/4.0/)。

来源：[官方页面或文档](https://www.domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf)。

- 文档日期为2015-03，PDF为59页。文件存在异常换行，引用应结合原段落核对。
- 聚合与上下文概念仅补足方法所需依据，不证明另一个中文版原件的缺页已被恢复。

## Design Patterns: Elements of Reusable Object-Oriented Software

标识：`design-patterns`。

作者：Erich Gamma、Richard Helm、Ralph Johnson、John Vlissides。

版本：未确认。

- 具体中文译本版次未核实；文件元数据题名不能确定版次。英文名存在异常空格，采用名称须以原页为准。
- 部分代码和图示不在文字层；末六页参考信息的文字层不完整，不作采用依据。
- 模式效果是有条件的设计经验，不能证实现有系统缺陷或当前运行性能。
- 文件页15–28仅采用方法明确列出的节与页；15页关系总图、17–18页 OMT 记法及215页图像未核查的关系不采用。16、19、20、21、23、27、28及216–219页的图示核查只支持相应有限关系。
- 1.6.3的操作签名和1.6.4的接口/实现继承区别，不构成完整行为约定或替换安全证明；错误、副作用、完成时点和状态责任需要另行规定。
- 1.6.6 aggregation 指对象拥有、协作与生命周期，不能等同于 DDD 聚合或事务一致性边界。
- 表1-2仅支持按可变方面选择，不证明23种模式的完整工程能力。组合与委托也有协作复杂度和间接层成本，不能据此一律禁止继承。
- 215–218页有限文字中的共享策略结论，只适用于不保存调用间状态、明确参数或 Context 及缺省条件；模板和后续完整实现未采用。
- 216页类图不能认证生命周期、事务或并发；省略代码不能证明全程序行为等价。Window图不表示原接收者回调，Aggregator符号不保证释放。精确代码与现代语言行为仍需核实。

## Domain-Driven Design: Tackling Complexity in the Heart of Software

标识：`domain-driven-design`。

作者：Eric Evans。

版本：中文第1版。

- 原件为扫描PDF，OCR有字符误识；文字层不能单独支持关键判断。38–45页的采用以原图和连续上下文为依据，44–45页未取得可靠OCR。
- PDF103是第6章续文，并非完整章首。作者2015年的 Reference 单独作为来源，不能视为中文原件的恢复文本。
- PDF38未显示印刷页码16，该对应值由邻页连续位置推定；PDF39–45显示印刷17–23。不能将推定页码写成原页可见内容。
- 图6-3、图2-1与2-2只支持相应采用关系；图2-3仅用于语言共享范围。未采用的图示不视为已核实，也不随运行包分发原图。
- 来源核查未执行书例、实现行为或真实工程案例；质量标记不等于错误率，精确代码、原表格与原图未作全面认证。

## Patterns of Enterprise Application Architecture

标识：`enterprise-application-architecture`。

作者：Martin Fowler。

版本：未确认。

- 原件为扫描PDF，版次仍待确认，识别质量和历史示例限制保留；代码、表格与图示未作精确认证。
- 页码偏移随插页改变，须使用各段核对的文件页与印刷页，不能套用全书统一偏移。
- 架构方法中“不要分布对象”针对细粒度远程对象协作，不能推广为禁止所有分布；不采用历史调用倍率或 XML/RPC/SOAP 优劣。
- 文件页181、199、202和338的指定含混说明或谓词未采用；隔离级别名称、联接数量、旧语言限制、会话安全简述和固定清理周期均不作为当前保证。

## Enterprise Integration Patterns

标识：`enterprise-integration-patterns`。

作者：Gregor Hohpe、Bobby Woolf。

版本：未确认。

- 原件为扫描PDF，正文按印刷页和章级位置定位；不能直接信任二级书签。
- 中文旧译“死文字通道”对应 Dead Letter Channel；运行规则采用“死信”用语，同时保留原节名。
- 代码OCR存在符号错误，未复制为运行实现，未执行书中示例。局部OCR页数不能代表全书已读或方法采用范围。

## Go context official documentation comments — bounded cancellation / Done / CancelFunc snapshot

标识：`go-context-cancellation`。

版本：2026-09-30取得的官方context.go注释快照；未固定发布版本。

来源：[官方页面或文档](https://go.dev/src/context/context.go)。

- 本来源是未固定发布版的官方context.go文档注释快照；只有列出的取消、Done、CancelFunc和WithCancel注释已核读。
- 取消表达应停止，CancelFunc不等待工作停止；观察Done只说明取消状态，不证明工作者退出或最后资源使用结束。
- CancelFunc的重复与并发调用保证不可扩成任意应用close或资源释放保证；宿主及精确发布版对应未认证。

## The Go Programming Language Specification — language version go1.27 (May 26, 2026)

标识：`go-language-spec`。

版本：网页标题明确标示语言版本go1.27，日期May 26, 2026。

来源：[官方页面或文档](https://go.dev/ref/spec)。

- 本来源限定网页标示的语言版本go1.27及7个已读片段；规范网页URL可变，采用时按版本及内容摘要确认。
- 当前宿主、编译器和库版本未认证；不将Go保证迁移为跨语言保证。
- 发送、接收、关闭及select的单步行为不证明应用组合条件、公平、取消优先级或整组任务退出。

## The Go Memory Model (version of June 6, 2022)

标识：`go-memory-model`。

来源：[官方页面或文档](https://go.dev/ref/mem)。

- 这是 Go 的明确语言模型，不能把具体保证照搬至其他语言。
- 实际任务仍须核实目标语言、版本、库操作的同步保证；未采用竞态程序允许结果作为编程策略。

## Go sync.Cond API — sync@go1.27.1

标识：`go-sync-cond`。

版本：官方pkg.go.dev固定sync@go1.27.1的Cond文档。

来源：[官方页面或文档](https://pkg.go.dev/sync@go1.27.1#Cond)。

- 本来源固定为sync@go1.27.1，仅核读Cond、NewCond、Broadcast、Signal和Wait文档。
- 观察及改变条件、调用Wait须遵守关联L；通知不等于条件持续为真、未来许可、公平或参与者已退出。
- 未固定cond.go仅作独立注释旁证，不认定与go1.27.1精确同版；宿主Go版本未认证。
- Go Wait的文档不支持虚假唤醒返回；循环仍需复查条件，取消和结束依赖完整应用协议。

## Growing Object-Oriented Software, Guided by Tests

标识：`growing-object-oriented-software`。

作者：Steve Freeman、Nat Pryce。

版本：未确认。

- 只采用列明的原则章节和局部小节，没有审阅全书示例的行为正确性。
- 异步测试的操作关联、责任人和失败证据清单属于工程适配，不是原书直接规定。
- 模块职责方法采用PDF73–81、84–85、88–89、94–96的正文原则，PDF90仅作上下文。图6.1/6.2/7.1未采用；图8.1/8.2的有限观察关系仅用于已明确引用的方法。书例代码未作为方法实现或评估夹具。
- Object Peer Stereotypes 是职责判断启发式；fire-and-forget 描述对象协作，不能证明跨进程交付、事务或合规保证。
- 共享可变引用能突破访问修饰符的封装；复制、共享、借用或转移须依具体接口约定和语言语义选择，不能强制复制所有值。
- 第5章只采用用户目的、业务结果、具体失败原因与检查粒度原则；独立预期及已有结论适用性清单属于工程适配。
- PDF43–44、56–62、65、67–68、70、94–96及图2.4/2.5、8.1/8.2仅支持明确的对象与替身观察关系。四类验证范围及风险安排是工程适配，未执行真实连接。
- PDF31–32、254、263–265仅采用指定小节，265页止于 Confused Object 标题前。第4章仅采用PDF56–57和60–61，第5章采用PDF64–70；局部图示与构造依赖检查不能替代整章审定。PDF29–30、269仅为上下文。
- 采用测试自身问题与生产设计问题的区分、预期失败与诊断、准备性重构、逐步保持行为及按反馈调整粒度。共同使用、相同生命周期和命名仅是职责线索，不按参数数量拆分；书例未执行，纯函数不据此强加对象结构。

## Java Concurrency in Practice

标识：`java-concurrency-in-practice`。

作者：Brian Goetz、Tim Peierls、Joshua Bloch、Joseph Bowbeer、David Holmes、Doug Lea。

版本：2006。

- 只采用方法列出的性能、构造、发布、所有权及共享计算片段，不声明全书通读。2006年正文与2011年EPUB元数据日期含义不同；出版社完整版本未确认。
- 静态核读与原创推导不能证明当前平台行为、实际性能、基准工具或 Skill 效果；未执行书例。
- 性能来源中的 S40、S41、S46–S49 保留各自范围。Listing 12.12 的传送项数与整数截断、图12.3的线程批次样本与断轴影响解释，不能忽略。
- S48仅采用必要工作与完成路径；完整 Amdahl 公式、历史曲线与队列排名未采用。
- 构造、发布与所有权判断保留2006年Java条件、final初始化例外及持续修改责任；实施时必须核对目标语言、运行时与库版本。
- C14仅采用4.1.3，不采用4.3完整委托。独占移交仍要求正确发布、唯一接收和旧别名停用。
- §11.4–11.4.4与§13.5的有限锁相关片段，不认证当前JDK实现或历史性能收益；来源支持不能自动替代当前正文、接入与行为验收。

## Working Effectively with Legacy Code

标识：`legacy-code`。

作者：Michael Feathers。

版本：未确认。

- PDF52、53文字层为空，采用内容通过原图人工阅读与局部语义记录补足，不声称整本OCR。
- PDF54文字层代码损坏：不采用后半静态方法改写例；接缝依据使用52/53原图及44、48–49、55–56清晰正文。
- 其他页也有OCR标识符、括号损坏；不移植示例代码，只采用核查过的方法与条件。
- PDF177（印刷160）对Java数值转换的泛化表述及译注不作语言语义依据；保留路径和转换边界检查方法。
- 原图代码存在省略上下文，视觉核对不等于编译或工程验证。
- PDF172（印刷155）第二个最终测试片段未保留前一片段的assoc设置；只采用特征测试的定义、操作原则和可疑结果调查，不复制该示例作为可运行测试。
- PDF79（印刷62）外覆类历史语言片段未作可编译核验；采用6.4的步骤、条件与代价，不移植源代码。
- 25.14只采用PDF314末至318的25.15标题前；25.15只采用PDF318动机与首例，后续步骤未核读。构造/求值时点、资源所有权和多个外部效果的兼容性仍需目标工程证据。
- 第11章采用影响草图、所有客户/继承范围检查和影响传播的列明片段；不声称完整示例代码验证或全语言影响分析。
- 版次仍待核实；6.2步骤6错号按语义顺序解释，79接口/extends、81字段e/employee及前后日志差异不作可运行模板，80省略代码与73规范OCR丢弃区域均不扩大采用；11.4不采用。

## The Mythical Man-Month

标识：`mythical-man-month`。

作者：Frederick P. Brooks Jr.。

版本：二十周年纪念版。

- 原件的 OPS/chapter6.html 与 OPS/chapter30.html 有XML不合规位置，原件未修复。
- chapter30异常标签可能使宽松HTML提取遗漏Parnas相关自我修正；有关采用依据为chapter31独立完整段落，不能据错误提取形成相反结论。
- chapter31仅采用指定小节。HTML换行与书页不能可靠对应，使用原生路径定位。
- 质量标记不等于错误率；精确代码、原表格和原图未作全面认证。

## NASA Systems Engineering Handbook: 6.8 Decision Analysis

标识：`nasa-decision-analysis`。

来源：[官方页面或文档](https://www.nasa.gov/reference/6-8-decision-analysis/)。

- 采用公开网页的文本内容，只限6.8.1指定子节，不包括6.8.2。
- 模型或评分不能替代业务标准、证据与决策责任；未知符合性的处理属于工程适配。

## NASA Systems Engineering Handbook: Appendix C

标识：`nasa-requirements`。

来源：[官方页面或文档](https://www.nasa.gov/reference/appendix-c-how-to-write-a-good-requirement/)。

- 验收记录中的版本、证据状态、变更关系和检查步骤属于工程适配；列出验证方法不等于已经执行验证，也不证明业务选择正确。

## NIST/SEMATECH e-Handbook 1.3.5.2

标识：`nist-confidence-mean`。

来源：[官方页面或文档](https://www.itl.nist.gov/div898/handbook/eda/section3/eda352.htm)。

- 未把页面示例的均值区间公式作为任意工程数据的默认算法；不同数据需核实抽样和分布前提。

## NIST/SEMATECH e-Handbook: Underlying Assumptions

标识：`nist-eda-assumptions`。

来源：[官方页面或文档](https://www.itl.nist.gov/div898/handbook/eda/section2/eda21.htm)。

- 采用的是公开网页工具提取文字快照，不是原始HTML；只支持指定段落，不认证完整公式或实验。
- 成组或随机安排不能保证全部干扰已排除；不相关不等于独立，实际样本和估计方法适用条件另核。

## NIST/SEMATECH e-Handbook: Randomized block designs

标识：`nist-randomized-block-designs`。

来源：[官方页面或文档](https://www.itl.nist.gov/div898/handbook/pri/section3/pri332.htm)。

- 采用的是公开网页工具提取文字快照，不是原始HTML；只支持指定段落，不认证完整公式或实验。
- 成组或随机安排不能保证全部干扰已排除；不相关不等于独立，实际样本和估计方法适用条件另核。

## NIST SP 800-218, SSDF Version 1.1

标识：`nist-ssdf-1-1`。

来源：[官方页面或文档](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-218.pdf)。

- 仅采用规则明确标明的段落，不把片段核查扩展为整份文档通读。

## NVDA 2026.2 User Guide

标识：`nvda-user-guide-2026-2`。

版本：NVDA 2026.2 User Guide。

来源：[官方页面或文档](https://download.nvaccess.org/documentation/en/userGuide.html)。

- 仅采用冻结NVDA 2026.2手册七节的有限操作条件；动态URL不替换该快照。
- 实际键盘布局和修饰键以当前用户配置为准；未安装或执行NVDA，未执行目标界面或全面可访问性评价。

## OWASP Threat Modeling Cheat Sheet

标识：`owasp-threat-modeling`。

来源：[官方页面或文档](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)。

- 仅采用规则明确标明的段落，不把片段核查扩展为整份文档通读。

## Peopleware: Productive Projects and Teams

标识：`peopleware`。

作者：Tom DeMarco、Timothy Lister。

版本：第3版。

- 组织行为建议来自作者经验及所引研究，未独立复现研究，不把相关性改写为因果定律。
- 规则中的有期限改进实验、团队层面观测和权限保护为工程适配，不是原书直接提供的管理标准。

## A Philosophy of Software Design

标识：`philosophy-of-software-design`。

作者：John Ousterhout。

版本：July 2021 Second Edition v2.0。

- 第9章采用范围未包含9.5–9.6及其所引前章；第7.1–7.4的有限采用不能补足其余引用章节。
- 短片段与数十行的讨论属于作者判断，不能作为普遍阈值。
- 图9.1与9.2省略内容不能证明完整路径等价或通用 goto 建议。
- 第7.1–7.4仅解释浅转发、共同接口与包装替代的条件；图7.1不能证明删层安全，历史13/15不是阈值，语言示例不认证当前平台。
- 第12、13、15及19章只采用各方法明确定位的片段和例外，不代表这些整章或全书采用。

## The Pragmatic Programmer: From Journeyman to Master

标识：`pragmatic-programmer`。

作者：Andrew Hunt、David Thomas。

版本：英文原著第1版；中文2011年版。

- 本文件是From Journeyman to Master版本中文译本，不是20周年新版。
- 原生目录存在失效锚点，使用已核实的章节文件定位。
- 代码以图片存在；采用依据限于00006–00008、00010、00062、00069–00073、00079–00081；其他未经核查图片不作采用依据。
- 不承诺书中的CORBA/RMI、EJB或AOP历史语义适用于当前技术栈。
- 第25节的 auto_ptr、finalize 以及旧工具推荐不迁移为当前 API 指导；未承诺垃圾回收会及时清理外部资源。
- 第32节的“大多数算法亚线性”、仅凭循环结构推断阶及具体对数倍率不采用；复杂度定义由 Cornell 原始课程支持。
- 第 9 节数据库与部署模式替换的乐观表述仅用于说明隔离目标；不保证切换时长、配置透明性或数据迁移成本。
- 第21节 text/part0019_split_001.html 的合约违背否定句与前条件责任及第23节断言说明存在语义冲突；原生HTML已核实，未核读其他版本，不确定是翻译还是转录问题，不采用该争议句，不修改原件。
- 第21–26节只采用登记的正文及已视觉核对图码；不把外部输入校验替换为断言，不把正常业务失败等同于终止服务，不将异常或资源释放解释为业务未生效或已回滚。
- 资源书例省略错误处理；不保证原子写入或一般异常安全，auto_ptr、finalize及其他历史API不作为当前语言保证。
- 使用中文第1版译本，未对照英文原版或20周年版，不把现代版内容倒归当前版本。
- 原生HTML与可见图片是采用依据；辅助TXT移除格式，仅供检索，不替代图示核查。
- 只声明定向来源核读；不宣称全书精华提炼完成、工程行为得到验证或用户场景正确率。
- 状态模型、歧义清单、判别例以及具体责任字段属于工程适配，应另按DDD/NASA原文及独立审阅支持，不虚构为作者现成框架。
- 第36节仅采用范围增长的有关段落；书中新增数量和项目延期不作为工程阈值。具体变更影响表、验收记录和重新检查步骤属于工程适配。

## Refactoring: Improving the Design of Existing Code

标识：`refactoring`。

作者：Martin Fowler。

版本：第2版。

- 已采用2.1–2.2、2.4–2.6、1.3、4.1/4.3/4.5/4.6、6.1、6.11及11.1的登记范围；6.1仅采用列明范例。不等于全书或整个重构目录加工。
- 抽取代码按EPUB原始标记核对，未运行原书示例。
- 工具安全性、编译器优化与语言特性需按具体环境再查；不将作者六行函数偏好写成硬阈值。
- 11.1原生XHTML的删除线是变更步骤语义；文本证据保留[DELETED:…]，不得把被删除的告警调用当成新查询的实际副作用。此为抽取风险，不据此判定原书错误。
- 6.11中间代码存在参数不一致；未运行书中代码。重构的保护域、纯结构与行为变更分开提交、回退只撤销当前小步、并发或不稳定查询下不机械拆分等属于条件化工程综合，不声称原书提供完备执行保证。
- 后续完整范例未读。
- 原书测试步骤只读未执行。
- 失败时点、输入一致性和具体语言分派仍需单独证据。
- 只读动机范围，不宣称完整搬移字段手法已读。
- 不从同时传递直接推导必须合并。
- 没有读后续完整范例。
- 剪切步骤不提供可自由重排的许可。
- 继承体系中的行为保持不能由简要步骤自动认证。
- 节点127未被改写、校勘或擅自替换成另一API规定。
- Java代理和迭代器说法仅作为该历史文本，不证明当前平台。
- 未读后续完整示例，不证明并发安全或深拷贝。
- 10.2、10.5、10.6只在引言被提及，其具体手法未读。
- 求值顺序、异常、清理和副作用保持是后续推导责任。
- 类和abstract简要步骤不证明某平台替换安全。
- 字面值判定保留为作者在此处的定义，不推广为静态类型定理。
- 音乐会例子只作文字上下文，未执行或复用为新题设。

## Release It! Design and Deploy Production-Ready Software

标识：`release-it`。

作者：Michael T. Nygard。

版本：未确认。

- 文件页与所采用印刷页的对应只适用于该原件，不能推断其他文件也相同。
- 第5章5.1–5.4用于相关规则，5.5与5.6另用于相关方法。其他预取页面不代表采用或完整阅读；页边重复与图示不作为额外主张依据。

## Quality Attribute Workshops (QAWs), Third Edition

标识：`sei-qaw-2003`。

作者：Mario R. Barbacci、Robert Ellison、Anthony J. Lattanze、Judith A. Stafford、Charles B. Weinstock、William G. Wood。

来源：[官方页面或文档](https://www.sei.cmu.edu/documents/716/2003_005_001_14249.pdf)。

- 仅采用PDF20–23／印刷8–11，完整报告可得不能证明全文核读。
- 场景分析仅支持描述和比较质量需求，不能证明具体架构满足指标。
- 原PDF日期与官网目录日期不同，需区分各自含义。

## Site Reliability Engineering: How Google Runs Production Systems

标识：`site-reliability-engineering`。

版本：未确认。

- EPUB多数图像资源无扩展名；图4-1仅按相应图像内容核对，提取器图片总数不能作为语义覆盖证据。
- 所读章节的真实事件仅用于理解来源条件，未复现、改写为夹具或用于真实案例评价。
- 一般错误预算不能覆盖隐私、安全或不可破坏的业务不变量。

## Software Architecture in Practice

标识：`software-architecture-in-practice-4e`。

作者：Len Bass、Paul Clements、Rick Kazman。

版本：Fourth Edition。

- 只采用各方法明确的有限段落，不代表全章或全书提炼。
- 历史实例、图片、人数、时长与整套组织流程不作为本方法要求；具体步骤与虚构推演属于工程适配。
- 来源支持不能替代对当前正文与接入的检查；真实工程效果未评估。

## Software Engineering at Google

标识：`software-engineering-at-google`。

版本：Official 2020 HTML edition。

原作品登记许可：CC BY-NC-ND 4.0。详见[官方版权说明](https://abseil.io/resources/swe-book)与[许可条款](https://creativecommons.org/licenses/by-nc-nd/4.0/)。该许可不是对本项目改编或再许可的授权。

来源：[官方页面或文档](https://abseil.io/resources/swe-book)。

编辑者：Titus Winters、Tom Manshreck、Hyrum Wright；官方2020 HTML版。

- 仅采用各方法与规则列明的片段，不代表整章、全书或未选内容已被采用。来源位置本身不能替代对当前正文适用性的核对。
- 第13章节点136–137及第14章节点117、123–127仅有局部采用；第15章的未选片段不在采用范围。第21章MVS片段只作历史上下文，不能用来扩展采用。
- 第18、21、23章及测试相关片段只支持明确列出的主张、条件和限制，不能认证当前平台行为。
- 不随包分发原书正文、代码或图示；历史数量不作为当前工程阈值。来源支持不证明 Skill 行为或真实工程效果。

## Software Requirements

标识：`software-requirements-3e`。

作者：Karl E. Wiegers、Joy Beatty。

版本：Third Edition。

- 只采用各方法明确的有限段落，不代表全章或全书提炼。
- 历史实例、图片、人数、时长与整套组织流程不作为本方法要求；具体步骤与虚构推演属于工程适配。
- 来源支持不能替代对当前正文与接入的检查；真实工程效果未评估。

## SWEBOK Guide V4.0a

标识：`swebok-v4a`。

来源：[官方页面或文档](https://ieeecs-media.computer.org/media/education/swebok/swebok-v4.pdf)。

- 知识范围目录用于查漏，不能表示逐节掌握；只对列明的采用段落进行核对。
- PDF362的掷骰方差算式及整数范围表述存在疑点，不采用这些数字、公式或表示法。
- 所据文件封面为 V4.0a / Released August 2026；官网更新日期与PDF不同，须区分版本及日期。
- PDF319表16.1把 Big-O/Ω/Θ 与最坏/最好/平均情形混淆，little-o/omega文字也不作为形式定义依据；整表不采用。
- PDF320表16.2将固定k的n^k及n!列入指数类、n log n列入对数类；整表不采用。
- PDF347的虎存在量词公式不作为逻辑指导，只采用相邻的所有/存在自然语言含义。
- 需求相关内容仅采用确认、验收表达、附加属性、版本、变更责任、追踪及预期结果判断原则；SWEBOK不决定每次工作的固定阶段。
- 第4.3节关于测试语言没有歧义、测试全过即可视作完全正确的概括，不作为普遍保证。书中航班表、ATM金额、优先级公式及历史例子不作为方法示范或测试输入。
- 对6.2、7.3及其他列明段落的定向采用，不能扩展为全书或完整需求章核读。

## Systems Performance: Enterprise and the Cloud

标识：`systems-performance`。

作者：Brendan Gregg。

版本：Pearson copyright 2021 Second Edition。

- 仅采用各方法明确的有限片段，不代表全书核读或全部候选采用。静态核读与原创推导不能证明当前平台行为、实际性能、基准工具或 Skill 效果。
- 第2版、版权2021。原性能方法S35–S39、S42–S45使用各自列出的范围，PDF文件页与印刷页分别定位。
- 196页未采用表的重排及229页疑似缺字限制保留，不能把提取结果无条件当作原页完整含义。
- 图4.4分别表示DB向客户端提供metrics和Web Server提供UI；计数、采样、追踪、off-CPU及符号归因均保留条件。
- SP-C04与SP-C07仅有有限定位支持，143–144页的虚拟地址上下文未额外采用；后续资源统计判断仍只限各方法明确的对象与范围。

## Test-Driven Development: By Example

标识：`test-driven-development`。

作者：Kent Beck。

版本：中文第1版。

- 原件为扫描PDF，既有文字层不足以作为正文依据。PDF21–27、111–124、131–135的局部OCR不能证明全书已可靠转写。
- 扫描可能包含邻页条带，OCR可能混入邻页内容或错误代码；采用概念须结合连续上下文和原图，不声明完成代码级校勘。
- PDF24、26、111、113–122、131–134的关键图像已核对，其他文字范围的读取方式不同，不能一概宣称逐页图像已检查。
- 第1章印刷页偏移18，第25/26/28章偏移14，不能给整书套用一个偏移。
- 邻页条带与OCR不作为数值或API主张依据；独立预期的具体要求属于工程适配，学习测试通过不能证明整个应用可运行。
- 第32章PDF164–174／印刷150–160仅支持其明确采用的正文判断；未执行书中代码。
- 第32章的效果说明包含作者经验与当时的证据限制；Darach的适用性挑战仍为未决问题，不能转为技术类别的允许或禁止表。完成条件由测试列表、临时实现清理和工程验收综合形成，不能归为原章的完整检查表。
- 原文转录与来源审阅不能替代工程验证。

## Threat Modeling: Designing for Security

标识：`threat-modeling`。

作者：Adam Shostack。

版本：EPUB metadata date 2014-02-17; numbered edition unconfirmed。

- 只采用各方法明确列出的有限段落，不声明全书重新提取或通读。运行不依赖原件或完整提取缓存。
- 书目元数据日期不能确定版次；历史来源不能提供当前平台、密码方案或标准认证保证。

## W3C WAI Easy Checks — A First Review

标识：`w3c-easy-checks`。

来源：[官方页面或文档](https://www.w3.org/WAI/test-evaluate/preliminary/)。

- 页面含旧浏览器操作说明，未采用；当前还有新稿链接，本规则只采用稳定原则与检查边界。

## xUnit Test Patterns: Refactoring Test Code

标识：`xunit-test-patterns`。

作者：Gerard Meszaros。

版本：未确认。

- 正文提取可读且采用位置按印刷页核对，但代码与表格没有全面校勘。
- 书中原则具有判断性并相互制约，只采用明确列明的范围。
- PDF86–87／印刷23–24仅支持有限测试判断。风险、观察层次与成本表属于工程适配；不采用失败层次唯一定位原因、一次手工检查保证正确或固定比例等绝对化解释。
- 第13章连续核读，其他章节只采用列明部分；相邻上下文不全部采用。未执行书例、Skill或真实案例。
- 资源所有权字段、原始失败与清理失败的分别记录、残留复用条件及独立事务已提交的反例，属于工程适配。此来源不能独自支持异步等待与后台任务停止的完整方法。

