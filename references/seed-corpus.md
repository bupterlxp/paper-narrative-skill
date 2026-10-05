# 用户提供的 35 篇论文种子语料

这张表只保存用户在原稿中提供的索引，供“找相似叙事”“对照范式”和“练习复盘”使用。论文名称、会议、奖项、数字和归因在正式写作或对外引用前必须回到原论文、会议页面或官方公告核验；不能把这张表当作独立事实来源。范式列是本技能的暂定标注，不是论文作者的自称。

## CVPR / ECCV / ICLR / ICML

| 论文（原稿写法） | 用户稿中标注 | 暂定主范式 | 叙事线索 |
|---|---|---|---|
| D4RT | CVPR Best Paper | 极简统一 / 反直觉 | 用一个时空查询接口统一动态场景的深度、点云与相机问题 |
| HKTex | ECCV Best Paper | 反直觉重构 | 抛弃 UV 展开，把高斯定义到网格流形上以处理纹理畸变 |
| Transformers are Succinct | ICLR Outstanding | 理论照亮经验 | 用参数表达能力比较解释 Transformer 的简洁性 |
| LLMs Get Lost | ICLR Outstanding | 新基准暴露失效 | 把多轮状态丢失量化为可靠性问题并拆出错误结构 |
| The Flexibility Trap | ICML Outstanding | 根因手术刀 / 反直觉 | 将扩散语言模型的任意序生成优势重述为推理风险来源 |
| High-Accuracy Sampling | ICML Outstanding | 理论照亮经验 | 以对数凹分布的形式化采样误差控制替代经验调参 |

## AAAI

| 论文（原稿写法） | 用户稿中标注 | 暂定主范式 | 叙事线索 |
|---|---|---|---|
| Align w/ Global Opinion | Best (AI Align) | 社会价值 / 新基准 | 把价值判断中的地域偏见变成可分析的评测问题 |
| Model Change | Outstanding | 理论照亮经验 | 形式化描述逻辑本体更新的算子与复杂度 |
| CaDyT | Outstanding | 根因手术刀 / 理论 | 用因果发现与 MDL 评分解释时序动态系统 |
| ReconVLA | Outstanding | 极简统一 | 用重建观测辅助学习三维场景表征并连接语言与动作 |
| High-Pass/Sheaflet | Outstanding | 理论 / 极简统一 | 抓住超图信号高通分量以解释并抑制过平滑 |
| LLM2CLIP | Outstanding | 极简统一 | 用 LLM 长描述蒸馏更细粒度的跨模态文本表征 |
| PlantTraitNet | Best (Social) | 社会价值 | 从公民科学图像服务全球尺度植物性状检索与生态保护 |
| Slum/GRAM | Best (Social) | 社会价值 / 极简统一 | 用区域路由的解耦表征支持跨城市棚户区监测 |

## ACL

| 论文（原稿写法） | 用户稿中标注 | 暂定主范式 | 叙事线索 |
|---|---|---|---|
| Imperfective Paradox | Best | 理论 / 新基准 | 用形式语义探针定位 LLM 推理局限 |
| Resource-Rational Encoding | Best | 理论照亮经验 | 用工作记忆约束建模并预测人类阅读行为 |
| Local Attention Exp. | Best | 理论照亮经验 | 形式证明局部注意力引入新的时序表达能力 |
| MauBERT | Outstanding | 根因 / 反直觉 | 用语音归纳偏置支持少样本声学单元发现 |
| Evo. Guided Decoding | Outstanding | 根因 / 极简统一 | 让价值函数迭代成为进化式解码的统一控制量 |
| Beyond Final Actor | Outstanding | 新基准暴露失效 | 区分生成者与编辑者，细化 AI 生成检测对象 |
| Lying with Truths | Outstanding | 新基准 / 根因 | 研究多智能体如何拼接真事实形成欺骗 |
| Lychee-FD | Outstanding | 根因手术刀 | 以梯度冲突解释全双工 SLM 的声学—语义干扰 |
| Mind the (DH) Gap | Outstanding | 新基准 / 社会价值 | 对比推理与对话 LLM 的风险决策差异 |
| MediEval | Outstanding | 新基准暴露失效 | 用知识扎根与上下文一致四象限测医学幻觉 |
| PALU | Outstanding | 根因手术刀 | 用前缀感知局部遗忘减少适应性遗忘并保留通用能力 |
| GeoRA | Outstanding | 根因 / 极简统一 | 以 RLVR 更新几何结构初始化低秩适配 |
| CURE | Outstanding | 根因 / 极简统一 | 用批评驱动统一强化学习与测试时自改进 |
| Forms-Meanings | Outstanding | 理论照亮经验 | 以形式—意义可学性度量解释高效交际 |
| STEER | Outstanding | 根因 / 理论 | 以熵变化视角统一 RLVR 熵干预并给出可计算调节 |
| GISP | Outstanding | 极简统一 | 用全局结构化剪枝支持一次剪枝、多种部署 |
| PolyGloss | Outstanding | 极简统一 | 联合切分与语际注释，重写多语言词汇处理接口 |
| CAR-bench | Outstanding | 新基准暴露失效 | 用模拟用户、真实工具和动态环境评估车载智能体一致性 |
| ViLL-E | Outstanding | 极简统一 | 把视频 LLM 表示嵌入化以服务检索任务 |
| CxMP | Outstanding | 新基准暴露失效 | 用构式理解最小对构造可诊断基准 |
| CIG | Outstanding | 新基准 / 根因 | 用会话信息增益评估语义记忆的动态价值 |

## 使用这张表的方式

- 需要复盘时，先按“叙事线索”而非方法名找近邻；
- 只借用问题结构（例如“先量化失效，再提出方法”），不要把别人的方法或数字当作自己的证据；
- 如果用户要求“官方原因”“完整数字”或文献引用，暂停类比，先要求原文/链接或进行可核验检索；
- 对相似论文做反例分析：它们的主张是否由干预、定理、基准或真实约束支撑，而不是只由奖项标签支撑。

