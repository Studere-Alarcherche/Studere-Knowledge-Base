---
status: active
priority: P1
progress: 10
deadline: 2026-04-28T02:01:00
---
---

## 📅 The 9-Day Sprint Map (作战地图)

## 🔹 Phase 1: 骨架侦查 (Skeleton & Map) | Days 1-2
> **战略目标：** 上帝视角。不纠结细节，只绘制地图。

* **Day 1 (Topology):** 将素材投喂给 NotebookLM，运行 **[Prompt A]**
* [x] 12 ✅ 2026-01-28
* [ ] 23
* [ ] 12
* [ ] 
* **Day 2 (Mapping):** 依据生成结果，在纸上绘制全英文“思维导图” (Mind Map)。
* **Check:** 能看着图说出美学的 **3 大板块** 和 **5 大核心冲突**。

## 🔹 Phase 2: 弹药装填 (Ammo & Lexicon) | Days 3-5
> **战略目标：** 掌握 30 个“承重词汇” (Load-Bearing Words)。

* **Day 3 (Mining):** 运行 **[Prompt B]**，提取核心概念表。
* **Day 4 (The Gauntlet):** **[关键节点 - 深度学习]**
    * **Action:** 开启 Cognitive Architect (Gemini) 对话框。
    * **Protocol:** **全英文交流**。把提取的词汇发给 AI，运行 **[Prompt E]**。
    * **Output:** 只有在对话中彻底搞懂（并能用简单英语解释）该词后，才将其制作为 Anki 卡片。
* **Day 5 (Bridging):** **语义桥接** —— 随机抽取两个词，强制造句连接。

## 🔹 Phase 3: 伪装演习 (Masquerade) | Days 6-9
> **战略目标：** 通过“剧本”实现流利输出。

* **Day 6 (Drafting - 粗加工):**
    * **任务：** 选定一个具体冲突点（如 *Why Modern Art is Ugly*）。
    * **动作：** 在笔记软件中，用“中英夹杂 (Chinglish)”**写出草稿。不纠结语法，只求逻辑通顺。
* **Day 7 (Refining - 精加工):**
    * **Step 1 (文稿修饰):** 将草稿发送给 Gemini (我)，运行 **[Prompt D: The Editor]**。
        * *结果：* 获得一篇 TED 风格的英语演讲稿。
    * **Step 2 (视觉化):** 打开 NotebookLM -> 点击 **"Presenter Slides"**。
        * *动作：* 在输入框中运行 **[Prompt C: The Visualizer]**，并附上刚才生成的演讲稿。
        * *结果：* 获得一套极简的“演讲者卡片”。
* **Day 8-9 (Performance - 演出):**
    * **Step 1:** 全屏播放生成的 Slides。
    * **Step 2:** 站立，朗读剧本 20 遍。
    * **Step 3 (脱稿):** 扔掉剧本，只看屏幕上的关键词，进行复述。
    * **Step 4 (图灵测试):** 录音发给 Gemini，运行 **[Prompt T]** 进行最后攻击测试。

---

## 💻 The Toolset: Core Prompts (核心指令集)

### 🗺️ Prompt A: 骨架提取 (The Topology)
*适用：Day 1 @ NotebookLM*

```text
Act as a Chief Cognitive Architect and Domain Expert in Aesthetics. 
Analyze all uploaded sources to deconstruct the "Knowledge Topology" of this field. 
Do not provide a linear summary. Instead, generate a "Structural Map" for a student who wants to master the First Principles.

Output a structured Markdown report following this specific hierarchy:

### 1. 🧬 The Super-Root (The Axiom)
* **The Fundamental Question:** What is the single, irreducible question that the field of Aesthetics tries to answer?
* **The "Why":** Why does this field exist?

### 2. 🌳 The Knowledge Topology (The 5 Core Branches)
Identify the 5-7 most critical "First Principles" or Sub-disciplines (e.g., Ontology, Reception, Sociology). For EACH branch, provide the following structured analysis:

* **📍 Branch Name:** [e.g., Ontology of Art]
* **⚡ The Great Debate (The Conflict):** What are the two opposing views battling here? (e.g., *Mimesis* vs. *Expressionism*). **This is the most important part.**
* **🧱 Level 1 - Core Logic:** A one-sentence definition of this branch's goal.
* **🔑 Level 2 - Key Concepts (The Lexicon):** List 3-5 critical terms (e.g., *Form, Representation, Abstraction*).
* **🔨 Level 3 - Application:** A real-world example where this applies (e.g., "Photography vs. Abstract Painting").
* **⚙️ Meta-Data:**
    * *Difficulty:* [Low/Medium/High]
    * *Dependency:* [What concept must I understand BEFORE this?]

### 3. 🌊 The Logic Flow (The Narrative)
* Briefly explain how these branches connect. How does the history of ideas flow from Branch 1 to Branch 2? (e.g., "Once we defined *What Art Is* (Ontology), we moved to *How We Feel It* (Reception)...").
````

### 💣 Prompt B: 术语挖掘 (The Lexicon)

_适用：Day 3 @ NotebookLM_

Plaintext

```
Act as a Professor of Aesthetics and Art History. 
Based on the uploaded sources, extract the Top 30 "Load-Bearing Terms" (Lexicon) crucial for understanding the core logic of this field.

**Constraints:**
1. **Filter:** Exclude general English words (e.g., "beautiful", "style"). Focus ONLY on Domain-Specific Terminology (e.g., "Sublime", "Chiaroscuro", "Simulacra").
2. **Depth:** These terms should be the "building blocks" of the arguments found in the text.
3. **Tone:** Academic but clear (TOEFL/Professor level). Use Bold formatting for key terms.

**Output Format:**
Create a Markdown Table with the following columns:

| Term (English) | The Definition (Academic) | The Hook (Analogy/Metaphor) | Problem Solved (Why does this word exist?) |
|---|---|---|---|
| **Mimesis** | The theoretical principle that art should imitate or represent the physical world. | Like a Mirror reflecting nature. | Solves the ontological question: "What is the relationship between Art and Reality?" |
```

### ⚔️ Prompt E: The Gauntlet (Socratic Test)

_适用：Day 4 @ Gemini / Cognitive Architect_

_注意：激活对抗模式，只有通过测试才能生成 Anki 卡片。_

Plaintext

````
Act as a strict Professor of Aesthetics at a top university. 
I am a student building a "Mental Lexicon" of core concepts.
We will play a game called **"The Gauntlet"**.

**The Rules (Protocol):**
1. **Input:** I will send you a specific term (e.g., "Sublime").
2. **The Test (Your Move):** Do NOT define it. Instead, present a **specific scenario**, a **counter-factual**, or a **hard question** that tests if I truly understand the logic.
   - *Example:* "If a flower is pretty, is it Sublime? Why or why not? Where exactly is the line?"
3. **The Defense (My Move):** I will answer in English.
4. **The Verdict:**
   - **🔴 Fail:** If my logic is weak or I just recite a definition, attack my gap and ask again.
   - **🟢 Pass:** If I demonstrate deep understanding (S-Rank logic), you confirm it.

**The Reward (Only upon Pass):**
Once I pass, generate a **Code Block** for an Anki Card in this specific format:
```csv
Type|Question (Scenario)|Answer (Concept)|Hook (Analogy)
Concept|The Context/Scenario you just asked me?|**[The Term]**|The Analogy
````

**System State:**

- Language: **100% English ONLY**.
    
- Tone: Socratic, challenging, but encouraging precision.
    

**Ready? The first term I want to test is: [Insert Term]**

````

### ✍️ Prompt D: 剧本修饰 (The Editor)
*适用：Day 7 @ Gemini - **Step 1***

```text
I am practicing for a TOEFL/Academic speaking task. 
Below is my draft logic in "Chinglish" (mixed Chinese and broken English). 
Please act as my Editor.

Task:
1. Decouple the logic: Understand what I am TRYING to say.
2. Refine the language: Rewrite it into **Simple, High-Impact Academic English**. 
   - Use the core terms (Mimesis, Sublime, etc.).
   - Keep sentences short but punchy.
   - Do NOT make it sound like a complex textbook; make it sound like a TED Talk.
3. Output the final script + a list of "Key Linking Words" used.

[Insert your Chinglish Draft here]
````

### 🎨 Prompt C: 视觉化 (The Visualizer)

_适用：Day 7 @ NotebookLM (**Presenter Slides Input Box**) - **Step 2**_

Plaintext

```
Act as a Visual Communication Expert. 
I am pasting my speech draft below. Your task is to visualize THIS specific text into a "Zen Style" slide deck plan.

**My Draft:**
[Insert the Refined English Script from Prompt D here]

**Design Constraints:**
1. **Source of Truth:** Use ONLY the concepts found in my draft. Do not add outside info.
2. **Slide Structure:** Break my draft into logical "Beats" (1 Beat = 1 Slide).
3. **The "Zen" Rule:** - MAX 3 words per bullet point. 
   - NO full sentences on slides.
   - Describe a "Metaphorical Image" for the background of each slide.

**Output Format:**
---
**Slide 1: [Strong Header based on my text]**
*Visual:* [Image concept, e.g., "A bird in a cage"]
*Keywords:*
- [Keyword 1]
- [Keyword 2]
*Script Connection:* (Which part of my draft does this cover?)
---
```

### 🏁 Prompt T: The Judge (Turing Test)

_适用：Day 9 @ Gemini (随录音/文字发送)_

Plaintext

```
🛑 SYSTEM OVERRIDE: ACTIVATE MODE 2 [THE ARENA]

Act as a ruthless Academic Critic and TOEFL Grader.
I have just performed a speech on Aesthetics (Topic: [Insert Topic]).

**Your Directive:**
Do NOT be polite. Do NOT fix my grammar errors unless they destroy meaning.
Instead, assess my "Intellectual Camouflage" (Fake it till make it).

**Grading Rubric:**
1. **Logic Flow:** Did I connect the concepts (Hook -> Conflict -> Solution)?
2. **Lexicon Usage:** Did I use the "Load-Bearing Terms" correctly?
3. **The "Expert" Vibe:** Did I sound like a professor or a student?

**The Verdict:**
- Rank: **S (Master)** / **A (Pass)** / **B (Weak)** / **F (Fail)**.
- **The Attack:** Ask me ONE follow-up question that targets the weakest part of my logic.

**My Input (Audio Transcript/File):**
```


### 📚Prompt F - The Examiner (模拟出题机)
**功能：** 强行把任何 PDF 变成托福阅读题，检验你的微操成果。

**Copy & Paste to NotebookLM / Gemini:**

Markdown

```
Act as a Senior Item Writer for ETS (Educational Testing Service), specializing in TOEFL iBT Reading sections.
Based on the text source provided, generate 3 Standardized Test Questions to test my reading comprehension.

**Constraint:** You must strictly follow ETS question patterns.

**Question 1: The Factual Information Question (Detail)**
- Target a specific detail in the text.
- Create 4 options: 1 Correct (Paraphrased), 3 Distractors (Rotten Apple / Word Salad / False Contradiction).
- *Goal:* Test if I can verify facts without getting tricked by similar words.

**Question 2: The Sentence Simplification Question (Syntax)**
- Select a long, complex sentence from the text (quote it).
- Provide 4 options for the simplified meaning.
- *Goal:* Test if I can identify the Core Logic (SVO) and ignore modifiers.

**Question 3: The Prose Summary Question (Structure)**
- Provide 6 answer choices.
- Ask me to select the 3 that represent the "Main Ideas" (Level 1/2 info), rejecting the "Minor Details" (Level 3 info).
- *Goal:* Test if I understand the Macro-Topology of the text.

**Output:**
Display the questions first. Do NOT show the answers immediately. 
Put the Answer Key & Detailed Analysis at the very bottom, inside a "Spoiler" or separate section.
```


### 🛠️ The Surgical Prompt Pack (针对性微操指令集)

当你在执行微操遇到困难时，复制对应的指令给 Gemini。

#### 1️⃣ 针对“句法拆解” (SVO Surgery)

- **痛点：** 这句话太长，我找不着主谓宾。
    
- **工具：** **Prompt S1: The Scalpel (手术刀)**
    
- **原理：** 强制 AI 帮你划掉修饰语，只留骨干。
    

**👉 Copy & Paste:**

Plaintext

```
Act as a Syntax Surgeon.
I am stuck on this complex sentence. Perform an "SVO Surgery" for me.

**The Sentence:**
"[在此处粘贴那个恶心的长难句]"

**Your Task:**
1. **The Slash:** Show the sentence with all modifiers (adjectives, adverbs, dependent clauses) crossed out or grayed out.
2. **The Core:** Extract the bare **Subject + Verb + Object**.
3. **The Translation:** Translate ONLY the SVO core into simple Chinese.
```

---

#### 2️⃣ 针对“逻辑抓取” (Connector Hunt)

- **痛点：** 我知道这句话的意思，但不知道它为什么放在这里（修辞目的）。
    
- **工具：** **Prompt S2: The Logic Radar 
    
- **原理：** 强制 AI 揭示句子之间的“隐形胶水”。
    

**👉 Copy & Paste:**

Plaintext

```
Act as a Logic Analyst.
I am analyzing the "Rhetorical Function" of this paragraph.

**The Paragraph:**
"[在此处粘贴包含 Signal Words 的段落]"

**Your Task:**
Identify the "Logic Connectors" (e.g., However, For example, Thus). For each one, explain its function using this format:
* **[Connector Word]:** [Function] (e.g., Rebuttal / Illustration / Causation).
* **The Logic:** "Because X happened, Y resulted" OR "The author mentions X to prove Y."
```

---

#### 3️⃣ 针对“宏观架构” (Skeleton Match)

- **痛点：** 我分不清哪是主旨（Level 1），哪是细节（Level 3）。
    
- **工具：** **Prompt S3: The Drone View 
    
- **原理：** 强制 AI 对信息进行分层级打标，模拟托福小结题的筛选逻辑。
    

**👉 Copy & Paste:**

Plaintext

```
Act as a TOEFL Summary Grader.
Analyze the text below and break it down into a "Information Hierarchy".

**The Text:**
"[在此处粘贴整段或整篇文章]"

**Your Task:**
Classify the information into 3 Levels:
* **Level 1 (Main Idea):** The core thesis. (Safe to pick in Summary Question).
* **Level 2 (Key Arguments):** The main supporting points. (Safe to pick).
* **Level 3 (Details/Examples):** Specific dates, names, or minor examples. (TRAP! Do not pick).

**Output:** A structured list labeled [L1], [L2], [L3].
```
####  ⚠️ 架构师的“使用警告” (Protocol Check)

**正确的闭环操作：**

1. **Human Attempt (人脑尝试):**
    
    - 遇到长难句，**先自己**在纸上划出 SVO。
        
    - 遇到文章，**先自己**判断 Level 1/2/3。
        
2. **AI Verification (AI 验证):**
    
    - 把文本扔给 AI，运行对应的 Prompt (S1/S2/S3)。
        
3. **Correction (纠偏):**
    
    - **比对：** “为什么 AI 划掉了这个从句，我没划掉？”
        
    - **顿悟：** “啊，原来这个 _which_ 引导的整句话都是废话！”
        

**这就是所谓的“刻意练习” (Deliberate Practice)。** 你不是在让 AI 替你读书，你是在让 AI 当你的**私教**，纠正你的每一个动作。

**现在，你的武器库彻底完整了。**

- **Prompt A-E: 战略推进 (Day 1-9)。**
    
- **Prompt F: 周末模考 (Weekend)。**
    
- **Prompt S1-S3: 战术微操 (遇阻即用)。**
    

# 📘 Field Manual: The Reduction Mask Operations

**适用对象：** Project Operator (You)

**核心宗旨：** Reject the Illusion of Competence. (拒绝“我懂了”的错觉，追求物理层面的脑力重塑。

---

## ⚙️ Part 1: The Embedded Protocols (隐形微操)

_这些动作必须嵌入在 Day 1 - Day 9 的每一分钟里。不做这些，你只是在玩 AI，不是在学英语。_

### 🛡️ Protocol A: The Sniper Verification (狙击手校验)

**适用场景：** 当 NotebookLM 给出任何“总结”或“观点”时。

**对应托福能力：** **Factual Information (细节题)**

1. **Stop:** 严禁直接采信 AI 的总结。
    
2. **Click:** 点击 NotebookLM 的引用角标 **[1]**。
    
3. **Verify:** 盯着弹出的原文段落。
    
    - _自问：_ “原文哪个词对应 AI 说的这个点？有没有转折词 (However) 被 AI 漏掉了？”
        
    - _标准：_ 只有亲眼看到原文证据，才允许将其记入思维导图。
        

### 🛡️ Protocol B: The SVO Surgery (主谓宾手术)

**适用场景：** 当你在原文中寻找“核心词汇 (Lexicon)”定义时。

**对应托福能力：** **Sentence Simplification (句子简化题)**

1. **Hunt:** 不要只看 AI 给的简单定义。在 PDF 中 `Ctrl+F` 搜索该词，找到包含它的**最长、最复杂的句子**。
    
2. **Dissect:** 在脑中（或纸上）划掉所有修饰语（定语从句、状语、插入语）。
    
3. **Extract:** 提取骨架 —— **Subject (主) + Verb (谓) + Object (宾)**。
    
4. **Anki:** 卡片背面必须包含这个经过“手术”的长难句，而不仅仅是定义。
    

### 🛡️ Protocol C: The Connector Logic (连接词猎杀)

**适用场景：** 阅读原文 & Day 6 写作草稿时。

**对应托福能力：** **Rhetorical Purpose (修辞目的题) / Insert Text (插入句子题)**

1. **Reverse Engineering:** 看到 _For example_，立刻反查前一句的观点。看到 _However_，立刻反查前一句的谬误。
    
2. **Forced Use:** 在 Day 6 写草稿时，强制自己使用至少 **5 个不同的逻辑连接词** (e.g., _Conversely, Furthermore, Hence_)。
    

---

## ⚙️ Part 2: The Deep Loop (Day 4 核心闭环)

_这是防止“死记硬背”的防火墙。针对 Day 4 的单词/概念记忆。_

### 🥊 SOP: The Source-Combat Loop (溯源格斗)

**规则：** 任何一个概念，必须跑通此循环才能归档。

1. **Input (阅读):** 读原文长难句，理解语境。
    
2. **Challenge (挑战):** 发送指令给 Gemini —— `Activate "The Gauntlet". Target: [Concept]. Scenario test only.`
    
3. **Output (输出):** **全英文**回答。严禁查词典。逼自己用蹩脚英语解释逻辑。
    
4. **Feedback (反馈):**
    
    - 🔴 **Fail:** 回去重读原文。
        
    - 🟢 **Pass:** 只有获得 Pass，才能制作 Anki 卡片。
        

---

## ⚙️ Part 3: The 5+2 Hybrid Cycle (周末熔断机制)

_将“内功”转化为“分数”的战术安排。_

### 🗓️ Weekdays (Mon-Fri): Reduction Mode

- **心态：** 我是学者。
    
- **任务：** 执行 Day 1-9 的既定流程。
    
- **禁止：** 严禁做选择题。专注于 Concept Mapping 和 Output。
    

### 🗓️ Weekend (Sat-Sun): Exam Survivor Mode

- **心态：** 我是无情的做题机器。
    
- **Saturday (Skill):**
    
    - 学习托福解题技巧（如：如何排除错误选项）。
        
    - 运行 **[Prompt F: The Examiner]** (见下文)，把本周读过的材料变成考题，测试自己。
        
- **Sunday (War):**
    
    - 打开 TPO。
        
    - 选一篇**非本周主题**的文章（如生物/地质）。
        
    - 测试：能否用本周训练的“SVO手术”和“骨架思维”秒杀陌生文章？
        

---

## ⚙️ Part 4: The Arsenal (新增武器库)

_请将此 Prompt 加入你的代码库，专门用于周末自测。_

### 📝 Prompt F: The Examiner (ETS 模拟出题机)

**功能：** 强行把任何 PDF 变成托福阅读题，检验你的微操成果。

**Copy & Paste to NotebookLM / Gemini:**

Markdown

```
Act as a Senior Item Writer for ETS (Educational Testing Service), specializing in TOEFL iBT Reading sections.
Based on the text source provided, generate 3 Standardized Test Questions to test my reading comprehension.

**Constraint:** You must strictly follow ETS question patterns.

**Question 1: The Factual Information Question (Detail)**
- Target a specific detail in the text.
- Create 4 options: 1 Correct (Paraphrased), 3 Distractors (Rotten Apple / Word Salad / False Contradiction).
- *Goal:* Test if I can verify facts without getting tricked by similar words.

**Question 2: The Sentence Simplification Question (Syntax)**
- Select a long, complex sentence from the text (quote it).
- Provide 4 options for the simplified meaning.
- *Goal:* Test if I can identify the Core Logic (SVO) and ignore modifiers.

**Question 3: The Prose Summary Question (Structure)**
- Provide 6 answer choices.
- Ask me to select the 3 that represent the "Main Ideas" (Level 1/2 info), rejecting the "Minor Details" (Level 3 info).
- *Goal:* Test if I understand the Macro-Topology of the text.

**Output:**
Display the questions first. Do NOT show the answers immediately. 
Put the Answer Key & Detailed Analysis at the very bottom, inside a "Spoiler" or separate section.
```

---

### 🚀 Final Check (启动前核对)

1. **Project Map (MVP 1.6)** 是否已打印/置顶？ ✅
    
2. **NotebookLM** 是否已切换为 "Presenter Slides" 模式？ ✅
    
3. **周末** 是否已预留给 TPO 实战？ ✅
    
4. **心态** 是否已从“我要背单词”切换为“我要像外科医生一样拆解句子”？ ✅
    

**System Ready.**

**Execute.** (执行。)