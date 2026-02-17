/* --- 📜 Razor Codex v9.7: The Structural Clarity --- */
#nice {
    color: #050505; 
    font-family: "Optima", "Georgia", "Songti SC", "Source Han Serif CN", serif;
    font-size: 16px;
    line-height: 1.75; 
    padding: 30px 20px;
    text-align: justify;
    background-color: #FDF6E3;
    background-image: linear-gradient(#E8DCC8 1px, transparent 0);
    background-size: 100% 35px;
}

/* --- 🖼️ 插画卡片 --- */
#nice figure.plate {
    margin: 20px 0 40px 0; padding: 10px; background-color: #FFF;
    border: 1px solid #C0A080; box-shadow: 4px 6px 16px rgba(0,0,0,0.15);
    transform: rotate(-1deg);
}
#nice figure.plate img { width: 100%; display: block; filter: sepia(15%) contrast(110%); }
#nice figure.plate figcaption {
    font-family: "Didot", serif; font-size: 13px; color: #5D4037;
    margin-top: 8px; text-align: center; font-style: italic; font-weight: bold;
}

/* --- 🏛️ 一级标题 (Book/Chapter) --- */
#nice h1 {
    text-align: center; font-size: 15px; letter-spacing: 2px; color: #3E2723;
    border-bottom: 3px double #5D4037; margin-bottom: 30px; padding-bottom: 10px;
}
/* --- 🏛️ 二级标题 (The Specimen) --- */
#nice h2 {
    text-align: center; font-size: 20px; color: #000; margin: 45px 0 25px 0; font-weight: 900;
    background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="40" height="5"><path d="M0,2 L40,2" stroke="%235D4037" stroke-width="1"/></svg>') bottom center no-repeat;
    padding-bottom: 12px;
}

/* --- 🔴 核心改动：三级标题 (目录/书架) --- */
/* 专门用于 "Logic Anchors", "Lexicon" 这些小标题 */
#nice h3 {
    /* 颜色：改为深咖啡色，与正文红字区分开 */
    color: #4E342E; 
    
    /* 大小：稍微放大，建立层级 */
    font-size: 18px; 
    font-weight: 900;
    
    /* 装饰：底部加一条虚线，像书架的隔板 */
    border-bottom: 1px dashed #A1887F; 
    padding-bottom: 5px;
    
    /* 间距：上宽下窄 */
    margin-top: 35px;
    margin-bottom: 15px;
    
    /* 字体：使用衬线体，增加学术感 */
    font-family: "Didot", "Georgia", serif;
}

/* --- 📖 标本卡片 --- */
#nice section.specimen {
    background-color: rgba(255, 255, 255, 0.95);
    border-left: 6px solid #8B4513; border-right: 1px solid #E0E0E0; border-bottom: 1px solid #E0E0E0;
    padding: 22px; margin: 30px 0; font-family: "Times New Roman", serif; font-size: 17px; color: #000;
}

/* --- 🛠️ 列表与圆点 (v9.6保留) --- */
#nice li {
    list-style: none; margin-bottom: 18px; padding-left: 28px;
    position: relative; color: #111; font-size: 16px;
}
/* 柔焦圆点 */
#nice li::before {
    content: ""; position: absolute; left: 2px; top: 10px; width: 8px; height: 8px;
    border-radius: 50%; background-color: #BA8F95; /* 干枯玫瑰粉 */
    box-shadow: 0 0 4px rgba(186, 143, 149, 0.7); 
}

/* --- 🖍️ 重点高亮 (依然是酒红) --- */
#nice strong {
    color: #800000; /* 仅保留深红色文字 */
    font-weight: 900;
}

/* --- ⚓ The Void: 极简纯享版 --- */
#nice section.void {
    background-color: #1F2A38; color: #E8DCC8; border-top: 3px solid #D6A668;
    padding: 35px 30px; margin: 60px 0; position: relative;
    box-shadow: 0 10px 30px rgba(0,0,0,0.4);
}
#nice section.void::before {
    content: "🕯"; font-size: 22px; display: block; position: absolute;
    top: -14px; left: 50%; transform: translateX(-50%);
    background-color: #1F2A38; padding: 0 10px; color: #D6A668;
}
#nice section.void p {
    font-family: "Georgia", "Songti SC", serif; font-size: 17px; line-height: 1.6;
    text-align: justify; font-style: italic; margin: 0; opacity: 1;
    letter-spacing: 0.02em; text-shadow: 0 1px 2px rgba(0,0,0,0.5);
}

/* --- ⛪ 结尾符 --- */
#nice hr.tower::after { content: "⛪"; font-size: 40px; color: #3E2723; display: block; text-align: center; margin: 60px 0; }


---

### 📝 Razor Codex: Day 1 完整写作模具 (v9.7)

请直接复制以下内容。注意 `###` 的使用，这是“颜色分层”的关键。

Markdown

```
# [Book Name] | [Chapter Name]

<figure class="plate">
  <img src="https://mmbiz.qpic.cn/...">
  <figcaption>Fig.1 The Memory of Martinville</figcaption>
</figure>

## The Specimen

<section class="specimen">
"[在此填入英文长难句... The realization of seismic resilience...]"
<br>
<em>— [Cite: Journal Name, Year]</em>
</section>

### Logic Anchors:

* **Rarely has... (Inversion):** Used to emphasize the unprecedented nature of a current event.
* **Not only does...:** Expands the impact of a phenomenon across multiple domains.

### Lexicon & Chunks:

* **Ontological categories:** Basic classifications of what exists and the nature of being.
* **Substrate-independent:** The idea that a process can function on different types of physical matter.

## ⚔️ The Friction (4-Tier Drill)

<section class="friction">

* **Tier 1 (Recognition):** Identify the **Main Subject**...
* **Tier 2 (Deconstruction):** Analyze the **[Logic Name]**...
* **Tier 3 (Translation):** Paraphrase into **Natural Human Chinese**...
* **Tier 4 (The Reverse Bridge):** Reconstruct the logic...

</section>

<br><br>

<section class="void">
If subjectivity is merely a "variable of computational density," what specific ethical "buffer" is destroyed when an AI reaches a certain parameter count?
</section>

<br>
```

