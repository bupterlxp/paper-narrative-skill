# Paper Narrative

**六大叙事范式 × 反防御学术写作。** 从 AI/ML 研究材料中找到证据支持的核心贡献，组织问题、方法与实验，再直接写出清楚、有分量的论文文字。

适用于研究定位、摘要与引言、整篇重构、局部润色、压缩和 rebuttal。既保留六大范式的研究思路，也融入 [Anti-Defensive Writing](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill) 的贡献聚焦与直接表达。

[Skill 入口](SKILL.md) · [十组完整改写](examples/before-after.md) · [上游整合记录](references/upstream-integration.md)

## 先看改写结果

以下是**虚构教学示例**，不是实际论文或实验结果。

### 最小改动：删掉情绪，贡献和范围都说清楚

**改前**

> 虽然本方法在两个同领域数据集上提高了准确率，但我们必须承认，实验仅使用一个 8B 模型。遗憾的是，跨领域泛化尚未评估。

**改后**

> 本方法在两个同领域数据集上提高了准确率，实验使用一个 8B 模型。跨领域泛化尚未评估。

去掉“虽然”“必须承认”“遗憾”，保留实验实际覆盖的范围。段序与作者意思保持一致。

### 完整英文摘要：从实验流水账到有依据的贡献

**可用材料**：BudgetSelect 为检索增强问答选择固定预算的证据，无需重训。四个英文 QA 集；同一模型、同一 A100、batch size 1。全量上下文基线宏平均准确率 84%、p95 延迟 300 ms；本方法 82%、120 ms。应用要求 p95 ≤150 ms；跨语言未评估。

**改前**

> We first tried using all retrieved context and then reduced the evidence budget. Although BudgetSelect is faster, we must admit that it only achieves 82% accuracy and fails to surpass the full-context baseline. Unfortunately, the improvement is limited because we have not tested other languages. We believe this promising approach could potentially be useful in the future.

**改后**

> BudgetSelect selects evidence for retrieval-augmented question answering under a fixed context budget, without retraining. We evaluate it on four English QA datasets against a full-context baseline using the same model on one A100 GPU at batch size 1. BudgetSelect achieves 82% macro-average accuracy with 120 ms p95 latency, compared with 84% and 300 ms for the baseline. It meets the application's 150 ms latency requirement with 60% lower p95 latency at a cost of two percentage points in accuracy.

贡献很具体：以 2 个百分点的准确率代价，达到给定的延迟要求。范围已限定为英文 QA，结尾聚焦这个已成立的结果。读者能看见价值，也能评估是否适合自己的场景。

### 45 词内：直接交付可用正文

使用同一组材料，要求英文、按空白分词、不超过 45 词、只要正文。输出为 **44 词**：

> On four English QA datasets, BudgetSelect reduces p95 latency from 300 to 120 ms using the same model and hardware at batch size 1. Macro-average accuracy is 82% versus 84% for full context. This meets the 150 ms requirement with a two-percentage-point accuracy cost.

[完整示例集](examples/before-after.md) 还包括均值与波动、相关性与因果、反例、事后选子集、理论与 LaTeX、尚未完成实验的 rebuttal，以及负结果论文。

## 怎么用

将材料附在下面任意请求之后即可，无需先填写完整的研究诊断表。

**最小改动**

```text
用 $paper-narrative 最小改动润色下面这段英文。
去掉无信息的防御语气，保留段序、事实、范围、LaTeX 引用和术语。
只给可直接粘贴的正文。
```

**已有结果找主线**

```text
用 $paper-narrative 分析下面的问题定义、方法和实验结果。
选最有证据的一条叙事主线，写出核心贡献，再重写英文摘要。
已有结果和建议补做的实验分开；不要替我补数字。
```

**压缩**

```text
用 $paper-narrative 将下面摘要压到 150 个英文词以内，按空白分词计数。
保留关键数字、比较条件和影响结论的范围，输出正文与词数。
```

**回复审稿人**

```text
用 $paper-narrative 回复下面的实际评审意见。
我会提供现有证据、已完成修改和拟补实验。
先给英文回复，严格区分已做与计划做，再列需要我补的信息。
```

## 两部分如何配合

六大范式帮助选定贡献；反防御编辑把它转成读者容易理解的文字。研究定位需要主张与证据图，局部润色直接交改稿。

| 范式 | 要找的贡献 | 写作时突出什么 |
|---|---|---|
| 根因手术刀 | 可检验的机制解释 | 干预改变了什么，排除了什么解释 |
| 反直觉重构 | 默认设定的有效替代 | 实际代价、公平比较与替代方案收益 |
| 理论照亮经验 | 定理、界、构造或形式化结果 | 结论及其假设，不把条件写成道歉 |
| 新基准暴露失效 | 原来漏测的重要现象 | 测量有效性、系统性发现与范围 |
| 社会价值叙事 | 真实流程中的约束与收益 | 谁使用、测到了什么、影响到哪里 |
| 极简统一美学 | 共享接口、表示或原则 | 覆盖的任务及实际复杂度变化 |

整合后的具体变化：

- **成稿优先**：按请求输出正文、最小修改或重构稿，不机械附上全套审稿清单。
- **贡献聚焦**：删开发流水账和无信息的自我贬低，用已有结果说明价值。
- **事实保真**：保留必要假设、关键反例、真实权衡、引用和实验状态。
- **实验服务论证**：主效果、机制、约束内价值、替代解释和失败边界都有位置。
- **按需重构**：原主张不成立就修正主张；事后子集或新指标的优势仍标为探索性。

“反防御”按句子的功能判断，不使用负面词禁表。`only 1% of parameters` 可以是资源优势，`under assumption H` 是定理条件，`underperforms at 64k` 可以是必须报告的结果。

## 安装

这是文本 skill，日常使用不需要 Python 包或额外插件。全新安装到 Codex 的技能目录：

```bash
git clone https://github.com/bupterlxp/paper-narrative-skill.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/paper-narrative"
```

已有同名 Git 安装可在保留本地修改的前提下更新：

```bash
git -C "${CODEX_HOME:-$HOME/.codex}/skills/paper-narrative" pull --ff-only
```

在支持加载 `SKILL.md` 的其他工具中，也可按其技能目录约定安装整个文件夹。

## 文件与维护

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 入口选择、共享约束与交付方式 |
| [六大范式](references/narrative-framework.md) | 研究定位、贡献层次与证据选择 |
| [反防御编辑](references/anti-defensive-writing.md) | 句子功能、段落组织与压缩规则 |
| [论文工作流](references/paper-workflows.md) | 复盘、定位、写作与 rebuttal |
| [审稿压力测试](references/reviewer-stress-test.md) | 按需全面审稿与语义复核 |
| [改写实例](examples/before-after.md) | 十组材料与可交付成稿 |
| [检查场景](evals/scenarios.md) | 可复用请求与人工检查标准 |
| [35 篇种子语料](references/seed-corpus.md) | 用户原稿的叙事索引，文献与奖项仍需核验 |

示例与检查场景用于核对事实保留、主张强度和交付约束，不代表已测得模型成功率或论文录用率。格式校验也不能替代实际使用中的判断。

## 来源

感谢 [Adkid-Zephyr/anti-defensive-writing-Skill](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill)。本次基于其 `82d3140` 版本改编，保留 [MIT 许可与署名](licenses/anti-defensive-writing-MIT.txt)，具体采纳与调整见 [整合记录](references/upstream-integration.md) 和 [文件校验清单](references/upstream-manifest.json)。上游许可不自动扩大到本仓库其余内容。
