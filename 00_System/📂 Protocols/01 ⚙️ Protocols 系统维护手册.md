
---

# ⚙️ Protocols: 系统维护手册 (v10.1 Curator Edition)

> **Prime Directive (最高指令):** 系统是为您服务的，而不是相反。我们不囤积信息，我们只**策展 (Curate)** 那些能引发“认知闪回”的信号。

## 🧹 1. 卫生协议 (The Hygiene Protocols)

### 每日清理 (Daily Clear)

- **触发时间:** 晚上睡前 (Evening Upload)。
    
- **对象:** `00 📥 INBOX`。
    
- **操作:**
    
    1. **任务 (Task):** `Daily Levers` 要么做完，要么划掉，要么推迟。
        
    2. **分流 (Triangulation):** 这里的杂念必须进行残酷分类：
        
        - **垃圾 (Noise):** 毫无保留地删除。
            
        - **砖块 (Brick):** 逻辑完整的想法 -> 移动到 `10 🧱 Blocks`。
            
        - **痕迹 (Engram):** 那些“很有趣但没想通”的孤儿 -> 移动到 `10 🧱 Blocks/00_Seed_Bank`。
            
    3. **清空:** `00 📥 INBOX` 必须归零。
        

### 🗓️ 每周维护 (The Sunday Summit)

- **核心逻辑:** 瓦尔堡图集重组 (Re-shuffling the Atlas)。
    
- **新增步骤 (Gardening):**
    
    1. **扫视种子库:** 打开 `00_Seed_Bank`。有没有哪颗种子现在可以发芽了？如果有，把它完善成 Brick。
        
    2. **检查图集:** 打开 `20 🌲 Atlas` 里的主要 Panel。逻辑链是否还稳固？有没有新的“蒙太奇”可以加入？
        
    3. **Anki 锻造:** 确认本周产出的 S-Rank 砖块是否已经生成 CSV 并导入 Anki。
        
编辑体验
---

## 🌲 2. 园艺协议 (The Gardening Protocols)

### 笔记的生命周期 (Life Cycle v10.1)

知识不是静态的，它是流动的。我们遵循 **Engram -> Brick -> Panel** 的进化路径。

1. **🌱 痕迹期 (Engram/Seed):**
    
    - **定义:** 一个孤立的、高价值的“直觉碎片”。它不符合当下的逻辑树，但隐含着某种模式。
        
    - **位置:** `10 🧱 Blocks/00_Seed_Bank`。
        
    - **标准:** 必须使用 **Standard B** 格式。
        
    - **标签:** `#status/seed` `#open_loop`。
        
2. **🧱 砖块期 (Insight Block):**
    
    - **定义:** 一个原子化的、逻辑自洽的知识单元。包含“公理-机制-结论”。
        
    - **位置:** `10 🧱 Blocks` 的各领域子目录。
        
    - **标准:** 必须使用 **Standard A** 格式。**必须包含 Mermaid 结构图**。
        
    - **标签:** `#status/mature`。
        
3. **🌲 图集期 (Warburg Panel):**
    
    - **定义:** 这是一个“画廊”。我们将 Block 和 Engram 钉在墙上，通过**并置 (Juxtaposition)** 产生新的意义。
        
    - **位置:** `20 🌲 Atlas/21_Themes`。
        
    - **标准:** 必须使用 **Standard C** 格式。核心是 **"The Interval" (蒙太奇张力)**。
        
    - **标签:** `#type/atlas`。
        

### 何时迭代 (When to Iterate)

- **不要强行连接:** 如果一个 Engram (种子) 找不到它的 Block，就让它待在 Bank 里。强行解释是幻觉的开始。
    
- **版本控制:** 伟大的 Insight Block 是不可变的 (Immutable)。如果你对某个概念有了颠覆性的新理解，建立 `v2` 版本，保留 `v1` 作为思维考古的证据。
    

---

## 🏗️ 3. 建筑协议 (The Structural Protocols)

### 命名规范 (Naming Convention)

_让文件名自带“类型索引”，方便 Spotlight/Alfred 快速调用。_

- **🌱 痕迹 (Engram):** `SD - [直觉关键词]` (例: `SD - 市场的分形结构`)
    
    - _注: SD = Seed/Seedling_
        
- **🧱 砖块 (Insight):** `IB - [概念名]` (例: `IB - 熵增定律`)
    
- **🌲 图集 (Atlas):** `EN - [核心议题]` (例: `EN - 反脆弱系统构建`)
    
    - _注: EN = Evergreen Note_
        
- **🎮 游戏 (SOP):** `SOP - [动作名]` (例: `SOP - 周复盘流程`)
    

### 标签体系 (Tagging)

- **#Domain:** `#topic/psychology`, `#topic/coding` (笔记的内容)
    
- **#Structure:** `#type/axiom` (公理), `#type/mechanism` (机制), `#type/montage` (蒙太奇)
    
- **#State:** `#status/seed`, `#status/growing`, `#status/mature`
    

---

## 🗑️ 4. 归档协议 (The Archive Protocols)

- **对象:** `99 🗄️ Archive`。
    
- **原则:** 这里是**博物馆**，不是垃圾场。
    
- **Anki CSV:** 每次 AI 生成的 `.csv` 文件，导入 Anki 确认无误后，移动到 `99 🗄️ Archive/CSV_Backups` (或直接删除，如果你够自信)。
    
- **Prompt:** 所有的 Prompt 迭代版本（如 `Cognitive Architect v9.2`）归档至 `100 Prompt Zone/Final`。
    

---

### 💡 落地执行 (Next Step)

1. **新建文件夹:** 在 Obsidian 里右键创建 `10 🧱 Blocks/00_Seed_Bank`。
    
2. **更新模版:** 把 AI 生成的 Standard A/B/C 三段 Markdown 代码，分别存入你的 `91 Templates` 文件夹。
    
3. **替换协议:** 用上面的内容覆盖你原来的 `00-Manual`。