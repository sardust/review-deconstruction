# 完整示范：拆解 Thaker et al. 2025（中等质量综述）

> 这是 `assets/deconstruction-template.md` 的填写示范，代表本 skill 期望的产出质量。
> 选它做示范的原因：质量中等——既有真功夫可抄，又有典型硬伤可避，教学价值最大。

综述：Thaker et al., "Evaluating AI approaches for space weather prediction", Space Habitation 1 (2025) 100032

一句话总括它：一篇"大而全"的空间天气 AI 综述——ML/DL/混合三分类 + 按算法逐节介绍 + 挑战清单；CME 只是其中一角。

## 1. 范围界定
- 界定原句："we present a structured comparative framework that systematically evaluates machine learning (ML) and deep learning (DL) methods for forecasting diverse space weather phenomena, including solar flares, coronal mass ejections, geomagnetic storms, and electron flux."
- 写法要点：摘要用一句话完成"算法类别 × 现象清单"界定；正文再用"研究目的两条（taxonomy + 对比）"复述一次。
- 我的决策：照抄"一句话现象清单 + 两条研究目的"句式，但我的现象只有一个（更深而非更宽）。

## 2. 检索方法
- 有独立小节 "Search methodology and article selection"，约半页，位于引言之后。
- 数据库 4 个（IEEE Xplore / SpringerLink / ScienceDirect / Google Scholar）+ 关键词清单 + 纳入标准（按性能/方法/结果）+ 偏好 case study。
- 缺陷：无 PRISMA 流程、无各库命中数、无最终纳入篇数——不可复现，是综述硬伤。
- 我的决策：照抄三段式，必须补上检索日期、各库命中数、筛选流程图、最终 N 篇。

## 3. 结构骨架
```
1. Introduction（背景+痛点+两条研究目的）
2. Search methodology and article selection
3. Classification of ML and DL algorithms（图1分类树）
4. ML applications（图2工作流 + 案例逐个介绍）
5. DL applications（图3工作流 + 案例逐个介绍）
6. Our taxonomy（ML/DL/混合三大类 + 表3汇总）
7. Overview of research workflow（图4）
8. Challenges and future scope（5个挑战逐段）
9. Future scope
10. Conclusion（按算法类→适用场景收束）
```
- 主线类型：范式为主（ML→DL→混合），现象为副。
- 我的对照：我的主线是任务链（检测→分割→跟踪→反演→预报）。两种都成立；任务链更适合"找缺口"目标。

## 4. 分类法
- 分类轴：轴1 = 算法类别（ML/DL/混合，仅 3 类）；轴2 = 现象（耀斑/CME/地磁暴/电子通量，4 类）。
- 呈现：图 1 树状分类图 + 表 3（算法×典型应用×优缺点）。
- 缺陷：轴1 只有 3 类且边界模糊（混合类按"是否含物理模型"又切一刀，两轴不正交）；完全没有"无监督/自监督"这个近年最重要维度。
- 我的决策：我的分类用任务×范式双正交轴，且必须覆盖自监督——这是相对它的增量。

## 5. 叙事技巧
- 采集句式：
  - 转折引局限："However, applying Bayes' theorem to complex, multivariable systems is computationally demanding."
  - 现象→方法映射："CNNs are particularly well-suited for handling magnetogram data... Therefore, with the identification of these regions, CNN models can predict TEC..."
  - 结论三拍收束：算法类 → 适用场景 → 代价。

## 6. 图表配置
- 图1 分类树 / 图2 ML工作流 / 图3 DL工作流 / 图4 研究框架；表1-2 各研究定性对比；表3 taxonomy 汇总。
- 缺陷：没有任何带数字的横向对比表——自称 comparative 却只有定性描述。
- 我的决策：对比表必须有统一指标列，这是明确的超越点，也是引言攻击"现有综述不足"的弹药。

## 7. 缺口/展望写法
- 按主题分段：数据稀缺 → 计算成本 → 可解释性（XAI）→ 物理融合 → 多模态，共 5 个挑战。
- 缺陷：每条挑战没有挂具体证据，只是泛泛引用；无优先级排序。
- 我的决策：每条挑战 = 主题句 + 具体证据 + 后果，并按严重度排序。

## 8. 引用策略
- 总引文约 95 篇（对"全空间天气"综述偏少，说明筛选松）。
- 混用：taxonomy 部分串联式；第 4/5 节退化为"一篇研究一段"的罗列式。

---

## 我要抄的 3 样
1. 检索方法独立小节的三段式（数据库+关键词+纳入标准），并补上它缺的复现性要素
2. taxonomy 后置的结构决策 + "图分类树 + 表汇总"图文配合
3. 结论的"三拍收束"句式（算法类→适用场景→代价）

## 它没做好、我要避免的 2 样
1. 没有定量对比表 → 我的对比表必须带统一指标列
2. "一篇研究一段"的罗列式 → 我的正文全部用串联式，每节开头先有观点句

---

## 副产品
- 挑战清单第 3 条引 LRP/SHAP——可与自己的"不确定性量化/可解释性"缺口呼应
- Future scope 已占用 LLM+物理约束、扩散模型超分等词——我的写法必须更具体（领域专用 backbone 而非泛泛 LLM）
- 重要确认：全文对 CME 检测仅一句带过 → "窄而深"定位成立，引言 gap statement 可直接引用此证据
