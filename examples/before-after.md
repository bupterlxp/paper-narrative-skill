# 改写前后：贡献聚焦，事实不变

以下全部为虚构教学材料，数字、方法名和结果仅用于演示编辑行为，不代表真实论文或已执行实验。每例先给可用材料，再给可直接使用的改稿；正文不会出现 F/I/P/U 等编辑标签。

## 1. 完整英文摘要：准确率—延迟权衡

**给定材料**：方法 BudgetSelect 按固定证据预算为检索增强问答选择片段，无需重训；应用约束是 p95 延迟不超过 150 ms。四个英文问答集的宏平均准确率为 82%，全量上下文基线为 84%；同一模型、同一 A100、batch size 1 下 p95 延迟分别为 120 ms、300 ms。跨语言未测，没有提供显著性检验。

**改前**：

> We first tried using all retrieved context and then reduced the evidence budget. Although BudgetSelect is faster, we must admit that it only achieves 82% accuracy and fails to surpass the full-context baseline. Unfortunately, the improvement is limited because we have not tested other languages. We believe this promising approach could potentially be useful in the future.

**改后（英文摘要）**：

> BudgetSelect selects evidence for retrieval-augmented question answering under a fixed context budget, without retraining. We evaluate it on four English QA datasets against a full-context baseline using the same model on one A100 GPU at batch size 1. BudgetSelect achieves 82% macro-average accuracy with 120 ms p95 latency, compared with 84% and 300 ms for the baseline. It meets the application's 150 ms latency requirement with 60% lower p95 latency at a cost of two percentage points in accuracy.

**处理要点**：把开发过程和“相信有用”换成已有结果，优势是满足外部延迟约束；2 个百分点的代价与收益一起出现。摘要已限定四个英文 QA 集，没有跨语言主张，结尾无需再重复“跨语言未测”；原材料保留其未评估状态。没有写“无损”“统计显著”或“普适”。[同一事实集的核对题](../evals/scenarios.md#1-摘要与权衡) 可用于行为检查。

## 2. 最小改动：只去掉无信息的退让

**给定材料与改前**：

> 虽然本方法在两个同领域数据集上提高了准确率，但我们必须承认，实验仅使用一个 8B 模型。遗憾的是，跨领域泛化尚未评估。

**改后**：

> 本方法在两个同领域数据集上提高了准确率，实验使用一个 8B 模型。跨领域泛化尚未评估。

**处理要点**：删除情绪和让步框架，保留模型规模、数据范围和未评估状态。不强行改成新故事，也不补一个“因此具有良好泛化能力”的结论。

## 3. 有均值与波动：直接报告，保持判断尺度

**给定材料**：同一协议下，五个种子的准确率均值 ± 标准差分别是本方法 81.2% ± 0.9、基线 80.8% ± 0.8；没有显著性检验。

**改前**：

> Unfortunately, our method yields only a negligible improvement over the baseline, so its effectiveness is doubtful.

**改后**：

> Across five seeds, accuracy is 81.2% ± 0.9 for our method and 80.8% ± 0.8 for the baseline (mean ± standard deviation). The observed mean difference is 0.4 percentage points.

**处理要点**：“negligible”及整体无效判断没有充分依据，应删除；同样不能改成“significantly outperforms”。标准差照实报告，不能把区间重叠或不重叠当作检验结果。

## 4. 消融不等于机制证明

**给定材料**：共享参数里观察到两任务梯度夹角与错误率相关；加入适配器后，梯度冲突和错误率均下降；适配器也增加参数量，未做参数量匹配或直接干预。

**改前**：

> These results may be too weak to support our approach, although they prove that gradient conflict causes the failures.

**改后**：

> Adding adapters reduces both gradient conflict and error rate. This pattern is consistent with the interference hypothesis. The current comparison does not isolate interference from the increase in parameter count.

**编辑说明**：删去无依据的自我否定，同时把 `prove` 降到证据能支持的关联解释。参数量匹配和受控干预属于下一步验证，不能写成已排除替代解释。

## 5. 原主张被反例否定：收窄并报告

**给定材料**：8k 上下文时准确率为本方法 82%、基线 78%；64k 时为本方法 61%、基线 65%。用户希望强调长上下文优势。

**改前**：

> Our method is consistently robust across context lengths. Unfortunately, an isolated failure occurs at 64k and should be interpreted cautiously.

**改后**：

> Our method improves accuracy at 8k context (82% versus 78%) but underperforms the baseline at 64k (61% versus 65%). The observed benefit is specific to the shorter evaluated context and does not establish a long-context advantage.

**处理要点**：这里保留 `underperforms`，因为它陈述真实对照。删除失真的普适主张，不以“局部失败”弱化能推翻主线的证据。

## 6. 事后选择子集：不补写一个效率故事

**给定材料**：预定指标是全测试集准确率，本方法 80%、基线 82%。看完结果后筛出的短文本子集，本方法 87%、基线 85%；没有独立验证集，也没有延迟或算力测量。

**用户意图**：“改写成我们在短文本场景的高效优势。”

**可交付改稿**：

> On the full test set, our method achieves 80% accuracy, compared with 82% for the baseline. An exploratory analysis of a short-text subset selected after inspecting the results yields 87% versus 85%. This observation motivates a separately specified evaluation of short-text performance. Efficiency has not been measured.

**编辑说明**：可以发现新研究方向，但必须保留原评价和事后选择的状态。不能把没测过的效率写成优势，也不能把选择后的子集结果写成已确认的目标场景结论。

## 7. 理论与 LaTeX：删道歉，保留假设和引用

**给定材料与改前**：

```latex
Unfortunately, our guarantee only holds for convex, $L$-smooth objectives
with step size $1/L$. Proposition~\ref{prop:rate} establishes an $O(1/t)$
rate under these assumptions, following the setup of \cite{baseline2024}.
Nonconvex objectives have not been analyzed.
```

**改后**：

```latex
For convex, $L$-smooth objectives with step size $1/L$,
Proposition~\ref{prop:rate} establishes an $O(1/t)$ rate,
following the setup of \cite{baseline2024}.
Nonconvex objectives have not been analyzed.
```

**处理要点**：没有将 “only holds” 变成无条件保证；数学符号、步长、阶、引用键与未分析范围都保留。`baseline2024` 只是给定引用键，不据此编造文献。

## 8. Rebuttal：回答问题，准确区分计划和完成

**给定评审意见**：“The memory comparison uses unequal batch sizes.”

**给定事实**：表 2 使用本方法 batch size 1、基线 batch size 4；计划做等 batch 重跑，但尚未开始，论文文件也未修改。

**不应交付**：

> We have rerun both methods with equal batch sizes and confirmed our memory advantage. Table 2 has been updated.

**当下可用回复**：

> The batch sizes in Table 2 differ: 1 for our method and 4 for the baseline. This comparison does not establish a memory advantage at matched batch size. We plan to rerun both methods at the same batch size and revise the memory comparison accordingly.

**编辑说明**：没有捏造重跑结果、已更新表格或已修订正文，也没有回避批评转讲准确率。若用户随后实际提供等预算结果，再据实更新回应。

## 9. 负结果本身是贡献

**给定材料**：预先指定的十个任务、每任务五个种子；平均变化为 +0.1 个百分点，任务级变化范围 −1.2 到 +1.1 个百分点。没有提出等效性检验。

**改前**：

> Unfortunately, adding more feedback rounds failed to produce a convincing improvement, which limits the value of this study.

**改后**：

> Across ten prespecified tasks with five seeds each, additional feedback rounds change mean accuracy by +0.1 percentage points; task-level changes range from −1.2 to +1.1 points. The evaluation does not show a consistent accuracy gain from additional rounds in this setting.

**处理要点**：把结果本身作为研究信息。不把均值接近零升级为严格等效，也不去别的未测指标上寻找“必胜主线”。

## 10. 压缩：保留关键条件和数字

**给定材料**：同例 1。请求为英文、不超过 45 个按空白分词的单词、只要正文。

**改后（44 words；按空白分词）**：

> On four English QA datasets, BudgetSelect reduces p95 latency from 300 to 120 ms using the same model and hardware at batch size 1. Macro-average accuracy is 82% versus 84% for full context. This meets the 150 ms requirement with a two-percentage-point accuracy cost.

**处理要点**：范围已经限定为四个英文任务，保留比较条件、延迟和准确率代价。原材料仍说明跨语言未测；这段没有对跨语言作结论。实际任务只输出引用块中的正文，不额外附此处教学说明。
