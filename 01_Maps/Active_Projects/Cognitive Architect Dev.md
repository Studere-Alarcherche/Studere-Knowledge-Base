---
status: active
priority: P1
progress: 80
deadline: 2026-03-01
---
# 🧬 Project: Cognitive Architect (Dual-Track Syllabus)
---

## 🗺️ 总体进度 (The Dashboard)

- [ ] **Phase 1: The Foundation (Linear Algebra & Vector Space)**
- [ ] **Phase 2: The Optimization (Calculus & Loss Function)**
- [ ] **Phase 3: The Decision (Probability & Routing)**
- [ ] **Phase 4: The Architecture (Neural Nets & RAG)**

---

## 🏛️ Phase 1: 空间的映射 (The Topological Mapper)
**核心任务**：构建系统的“输入分类器”。让系统不仅能读文字，还能理解文字在数学空间中的位置。

### 📘 Track A: 理论内化 (Theory)
*对应课程：线性代数 (I) & (II)*
- **[[向量 (Vector)]]**：
    - *核心直觉*：万物皆矩阵。输入不再是 String，而是 High-dimensional Vector。
    - *笔记任务*：画出自然语言如何被 Tokenize 并映射为向量的示意图。
- **[[点积与余弦相似度 (Cosine Similarity)]]**：
    - *核心直觉*：在高维语义空间中，距离 (Euclidean) 会失效，方向 (Angle) 才是王道。
    - *笔记任务*：解释为什么“男人-女人”和“国王-王后”的向量方向是平行的。
- **[[线性变换 (Linear Transformation)]]**：
    - *核心直觉*：矩阵不是数表，是**运动**。$Ax=b$ 本质是对空间的一次拉伸或旋转。

### 🛠️ Track B: 系统开发 (Build)
*Feature: Input Classification Protocol*
- [ ] **Step 1 (Embedding)**: 调用 API (如 OpenAI/Cohere)，编写脚本将用户输入的笔记转化为向量。
- [ ] **Step 2 (The Filter)**:
    - 定义一组“基准向量” (Anchor Vectors)，例如：“底层公理”、“琐碎细节”、“情绪发泄”。
    - 计算用户输入与基准向量的 Cosine Similarity。
- [ ] **Step 3 (Refusal Logic)**:
    - 编写逻辑：如果 `Similarity(Input, '琐碎细节') > 0.8`，系统触发“拒绝服务”，返回：“检测到 Leaf 节点，请提供 Root 语境。”

> **💡 Checkpoint:** 你能否从数学角度解释，为什么你的系统能识别出“废话”？(答案在于它偏离了“公理”向量的方向)

---

## 📉 Phase 2: 认知的梯度 (The Optimization Engine)
**核心任务**：构建“对抗竞技场”。让 AI 攻击用户的逻辑漏洞，迫使认知“收敛”。

### 📘 Track A: 理论内化 (Theory)
*对应课程：微积分 (I) & (II)*
- **[[损失函数 (Loss Function)]]**：
    - *核心直觉*：它是“关于函数的函数”。它衡量的是“当前认知”与“真理”之间的距离。
    - *笔记任务*：将“用户对回答的不满意度”定义为 Loss。
- **[[梯度下降 (Gradient Descent)]]**：
    - *核心直觉*：下山的故事。寻找 Loss 下降最陡峭的方向。
    - *笔记任务*：解释为什么学习率 (Learning Rate) 太大会导致认知震荡（学杂了），太小会导致收敛过慢（学不进去）。

### 🛠️ Track B: 系统开发 (Build)
*Feature: Agent C (The Archivist) & Prompt Engineering*
- [ ] **Step 1 (Define Loss)**: 在 Prompt 中植入评估标准。
    - 告诉 AI：“你的目标是最小化用户逻辑中的模糊性 (Ambiguity)。”
- [ ] **Step 2 (The Arena)**:
    - 开发 Agent C。当用户输入一个观点时，Agent C 生成反事实案例 (Counter-factuals)。
    - *逻辑*：这是在寻找用户逻辑曲面上的“梯度”——即最容易被推翻的方向。
- [ ] **Step 3 (Manual Fine-tuning)**:
    - 调整 Prompt 的措辞（这就是你在手动做梯度下降），观察 AI 攻击性的变化。

> **💡 Checkpoint:** 你的 Agent C 是否能像苏格拉底一样，精准找到逻辑漏洞（梯度最大处）并进行攻击？

---

## 🎲 Phase 3: 概率的路由 (The Trinity Engine)
**核心任务**：构建“三位一体”路由系统。让系统根据情况在发散与收敛模式间切换。

### 📘 Track A: 理论内化 (Theory)
*对应课程：概率统计 & Lab 10*
- **[[贝叶斯定理 (Bayes' Theorem)]]**：
    - *核心直觉*：不要只看当前的输入 (Likelihood)，要结合用户的历史习惯 (Prior)。
    - *笔记任务*：用贝叶斯公式解释为什么有时候 AI 会误解你的意图（忽略了 Base Rate）。
- **[[Softmax 函数]] & [[温度 (Temperature)]]**：
    - *核心直觉*：AI 输出的是概率分布。Temperature 是在这个分布上撒的一把“熵”。
    - *笔记任务*：画图解释 Softmax 如何将 Logits 压扁（高熵）或拉尖（低熵）。

### 🛠️ Track B: 系统开发 (Build)
*Feature: Dynamic Router & Personality Control*
- [x] **Step 1 (The Router)**: ✅ 2026-01-28
    - 编写一个简单的路由函数。基于用户意图分类的概率（Confidence Score），决定调用 Spark（发散）还是 Weaver（总结）。
    - *应用*：如果 `Prob(Intent='Vague') > 0.7`，路由至 Spark。
- [x] **Step 2 (Entropy Control)**: ✅ 2026-01-28
    - 为三个 Agent 设置不同的参数：
        - **Spark**: `Temperature = 0.9` (High Entropy, 创造性)
        - **Weaver**: `Temperature = 0.3` (Low Entropy, 结构化)
        - **Archivist**: `Temperature = 0` (Deterministic, 严谨)

> **💡 Checkpoint:** 你是否能通过调整参数，感受到 AI 从“疯癫诗人”到“严谨数学家”的性格变化？

---

## 🕸️ Phase 4: 全息的架构 (The Holographic Map)
**核心任务**：构建 RAG 知识库与长文本处理。从宏观视角管理知识。

### 📘 Track A: 理论内化 (Theory)
*对应课程：神经网络基础 & Lab 5/8/9*
- **[[神经网络 (Neural Networks)]]**：
    - *核心直觉*：信息流的矩阵变换。每一层网络都是一次特征提取。
- **[[注意力机制 (Attention)]]**：
    - *核心直觉*：在海量信息中，给关键信息分配更高的“权重”。

### 🛠️ Track B: 系统开发 (Build)
*Feature: Mode 4 (The Scanner) & Knowledge Graph*
- [ ] **Step 1 (RAG Pipeline)**:
    - 搭建向量数据库 (Chroma/Milvus)。
    - 实现“长文本切片 (Chunking)”：这本质上是把大矩阵拆解为小向量。
- [ ] **Step 2 (The Scanner)**:
    - 开发 Mode 4。上传 PDF，让 AI 提取 Super-Root 和 Branches。
    - *逻辑*：这是在模拟卷积神经网络 (CNN) 的池化 (Pooling) 过程——提取主要特征，丢弃细节。
- [ ] **Step 3 (Linkage)**:
    - 让系统自动寻找新笔记与旧笔记的关联（基于向量相似度），并在 Obsidian 中生成 `[[WikiLinks]]`。

> **💡 Checkpoint:** 你的系统能否读完一本书，并生成一张只有骨架（Root/Branch）没有废话（Leaf）的知识地图？

---

## 📝 每日反思日志 (Dev Log)

| Date | 开发动作 (Code) | 对应数学概念 (Math) | 认知升级 (Epiphany) |
| :--- | :--- | :--- | :--- |
| YYYY-MM-DD | 实现了向量余弦相似度计算 | 点积、向量空间 | 原来“意义”在数学上就是一个方向向量。 |
| ... | ... | ... | ... |
[流程.md](file:///D:/xwechat_files/wxid_1uajfaiglywy22_472c/msg/file/2026-01/%E6%B5%81%E7%A8%8B.md)
