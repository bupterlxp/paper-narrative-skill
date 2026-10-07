---
name: paper-narrative
description: "Develop evidence-grounded AI/ML paper narratives and revise abstracts, introductions, experiments, conclusions, and rebuttals. Use six narrative paradigms to select a contribution, connect claims to evidence, and remove defensive prose while preserving scientific scope. Use for research positioning, manuscript restructuring, shortening, or anti-defensive academic editing; not generic marketing or grammar-only proofreading."
metadata:
  short-description: "六大叙事范式 × 证据约束的反防御学术写作"
---

# Paper Narrative

找出证据支持的核心贡献，按问题、贡献、证据组织论文，再把句子写得直接、准确、有分量。六大范式帮助确定研究定位；反防御编辑让读者更快读到这个定位。方法论文、理论论文、基准和负结果研究都可使用，不要求每篇都发现根因或刷新 SOTA。

## 按请求选择入口

| 用户要什么 | 直接交付 | 按需读取 |
|---|---|---|
| 润色一段、去掉防御语气、压缩篇幅 | 改好后的文字；必要时附关键修改理由 | [反防御编辑](references/anti-defensive-writing.md)、[改写实例](examples/before-after.md) |
| 写标题、摘要、引言、结论，或重构初稿 | 成稿或新结构；标明真正缺证据的地方 | [论文写作](references/paper-workflows.md#c-写作与重构) |
| idea 定位、已有结果找主线、设计实验 | 最有依据的定位、主张与最小区分实验 | [六大范式](references/narrative-framework.md)、[研究定位](references/paper-workflows.md#b-研究定位与实验) |
| 复盘论文或获奖工作 | 原文位置支持的主张—证据图与可迁移问题 | [论文复盘](references/paper-workflows.md#a-论文复盘) |
| 模拟审稿、rebuttal、回复质疑 | 分级问题或可直接使用的逐条回应 | [审稿检查](references/reviewer-stress-test.md)、[rebuttal](references/paper-workflows.md#d-审稿与-rebuttal) |

只改一段时，在内部核对主张即可，不要求用户先填表，不输出整套范式诊断。遵守用户对语言、字数、语气和改动幅度的约束；“最小改动”保留结构，“重构”才调整主线和段序。

## 先定能说什么

从现有材料记录关键主张、来源位置和证据状态；复杂任务使用账本，简单任务在内部核对即可：

| 状态 | 含义 | 写入论文时 |
|---|---|---|
| F · fact | 材料明确提供的结果/定义；同时记来源是用户提供还是已核验 | 在原有条件内陈述，不把用户提供自动说成独立验证 |
| I · inference | 对事实的解释，尚有替代解释 | 用“支持……解释”等与证据匹配的动词 |
| P · proposal | 拟议方法、预测或尚未执行的实验 | 写成提议或未来动作，不改成完成时 |
| U · unknown | 未提供或无法确定 | 只在必要处标 `[待补：具体信息]`，或省去依赖它的结论 |

来源标签、审稿猜测和工作便笺放在编辑说明中，通常不进入摘要正文。不编造数字、方差、统计显著性、引用、会议奖项、图表编号或已完成的修订。保留用户的 LaTeX 引用、交叉引用、符号和术语对应关系。

缺信息时先完成可确定的部分；只有答案会改变含义、比较条件或成稿用途时才询问。占位符用于缺失的事实，不用来替代已经提供的数据。

## 找到核心贡献

概括为 **问题/现象 → 本文贡献 → 支持证据 → 成立范围**。需要机制解释时再加入诊断、干预和替代解释；研究历史不必变成论文段序。

从 [六大范式](references/narrative-framework.md) 寻找最贴合材料的主线，辅助范式只在增加解释力时使用；若都不贴切，直接按问题—贡献—证据组织，不勉强套标签：

1. 根因手术刀：机制诊断与干预；
2. 反直觉重构：检验默认设定并提出替代；
3. 理论照亮经验：明确假设下的形式化结果；
4. 新基准暴露失效：把重要漏洞变成可靠测量；
5. 社会价值叙事：真实使用者、约束和可量化影响；
6. 极简统一美学：共同接口/表征及其收益。

优先陈述可核对的价值：新测量、受约束条件下的收益、理论结果、机制证据或可靠的负结果。相关性和普通消融不能升级成根因证明；方法更简单也不能自动升级为更快、更省或更易部署。原主张被反例否定时修改主张，并保留否定它的关键结果。

研究规划可输出：`主张 | 当前证据/来源 | 区分预测 | 测试与对照 | 推翻条件 | 下一步`。实验只覆盖会影响主张的疑点；理论任务以定义、证明和反例为主，不为凑流程强加实证实验。

## 再做反防御编辑

按 [编辑规则](references/anti-defensive-writing.md) 将证据转换为成稿：

- **贡献先出现。** 开头明确问题、本文动作与已有结果。将“我们先做 A、后来做 B”改成最终成立的论证顺序。
- **用事实替代自评。** 删除“遗憾的是”“我们不得不承认”这类情绪；将“效果有限”改为具体结果与条件。必要的 `under assumption`、`on these datasets`、`may` 或表示资源数量的 `only` 不按词表删除。
- **边界与相关主张相邻。** 影响结论理解的样本范围、理论假设、预算和已知反例保留在主张附近；完整协议、辅助诊断和重复结果可按篇幅放到对应章节/附录。
- **不靠换口径制造优势。** 改叙事焦点要有任务需求或有效测量依据。事后发现的优势标为探索性；新指标、新子集和机制解释若未验证，列为后续实验，不写成确认性结论。
- **准确陈述权衡。** 同时保留相关收益与代价；“相当”“无损”“显著”“首次”等须有对应证据。关键负结果、必需基线和真实评审问题都具有论证职责。

这里的反防御是消除无根据的自我贬低，让成立的贡献显眼；不会降低证据要求。来源与规则调整见 [整合记录](references/upstream-integration.md)。

## 交付与复核

改稿默认先给 **成稿**，再给会影响理解的 **修改说明**；只有实际缺口才列 **待补证据**。用户只要正文就只交正文，在正文中保留必要限定。实验规划和论文复盘再使用主张表、范式分析；不机械附上全套风险清单。

对照输入复核：数值、单位、分母、基线、条件、假设、完成状态和引用是否一致；局部失败是否被扩大，重要反例是否被删；是否出现无依据的正面或负面结论。完整审稿压力测试按用户任务调用 [reviewer-stress-test.md](references/reviewer-stress-test.md)。

用户提供的 [35 篇种子清单](references/seed-corpus.md) 供找叙事近邻，奖项、数字和归因仍须核验。它不是已确认的最佳论文数据库。
