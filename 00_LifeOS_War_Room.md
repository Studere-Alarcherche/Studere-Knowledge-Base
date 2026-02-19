---
title: LifeOS War Room
---

# ⚔️ LifeOS War Room
> "Audit the Flow. Feed the Database. Update the Save File."

## 🔴 活跃战线 (The Forge)
*当前正在燃烧算力的项目。完成一项，将状态改为 `done`，并将残骸移入 99_Archive，结晶并入 01_Maps。*

```dataview
TABLE WITHOUT ID
  link(file.name) AS "🔥 战线 (Active Project)",
  priority AS "优先级", 
  "<progress value='" + progress + "' max='100'></progress> " + progress + "%" AS "推进进度",
  deadline AS "死线"
FROM "02_Active_Projects"
WHERE status = "active"
SORT priority ASC, deadline ASC
````

---

## 📊 算力与状态结算 (The Flow Audit)

_自动抓取 `04_Journal` 中过去 7 天的物理与认知引擎数据。_

Code snippet

``` dataview
TABLE WITHOUT ID
  link(file.name) AS "📅 日期",
  focus_hours + " h" AS "深度算力 (Focus)",
  energy_level AS "MP状态",
  choice(win_the_day, "🏆 胜利", "⚠️ 漂移") AS "系统判定",
  workout AS "肉体锻造",
  sleep_hour + " h" AS "休眠"
FROM "04_Journal"
WHERE date >= date(today) - dur(7 days)
SORT date DESC
```


---

## 🚦 物理引擎法则 (The Energy Standard)

_日常喂给 Chronos (AI) 的标准参数，时刻保持对熵增的警惕。_

- **🚀 DeepWork (1.5x)**: 逆向工程、构建概念、核心输出 (高阻力)。
    
- **🌱 Growth (1.0x)**: 摄入、阅读、普鲁斯特精读。
    
- **⚙️ Work (0.8x)**: 系统维护、日常杂务、排版配置。
    
- **⚠️ Entropy (-1.0x)**: 刷手机、无意义消耗、认知泄漏。
    
- **🎯 目标**: 28 - 30 pts / day | **漂移警告**: DeepWork < 20%
    

---

## 🔗 项目同步日志 (Project Sync)

_(每天在此处粘贴 AI 提示词生成的 `Part 3: Project Sync`，作为手动勾选和核对的备忘录。核对完毕即可删除，保持清爽。)_

```

***

### ⚙️ 它是如何完美运转的？（你的全新飞轮）

这个面板一旦建立，你的“每日操作系统”就彻底闭环了，而且**你几乎不需要在这里手动打字**：

1. **自动化战线管理**：
   你不需要在这个面板里手动添加项目。只要你在 `02_Active_Projects` 文件夹里建了一个新文件，写上属性 `status: active` 和 `progress: 10`。你一打开这个 War Room，表格里就会**自动长出一条带有进度条的战况记录**。
2. **自动化算力追踪**：
   每天晚上，你把日记丢给你的 `LifeOS Kernel v2.2` 提示词。AI 会生成一段带有 `focus_hours::` 和 `win_the_day::` 的数据代码（Part 2）。你把它粘贴回今天的日记底部。
   **神奇的魔法来了**：War Room 里的第二个 Dataview 表格，会自动把这段数据吸过来，生成一张记录你过去 7 天生命能量和深加工时长的“结算报表”。
3. **手动收尾（唯一的动作）**：
   把 AI 生成的 `Part 3 (Project Sync)` 粘贴到最下面的区域，提醒自己去对应的文件里打个勾 `[x]`。

**现在，物理引擎已经恢复，指挥中枢已经上线。**
你随时可以在 Obsidian 里点开这个页面，看看进度条和报表有没有正常显示。如果 Dataview 报错或者没抓到数据，你截个图给我，我帮你微调！
```