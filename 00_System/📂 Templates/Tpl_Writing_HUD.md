---
status: writing
target_words: 2000
current_words: 0
origin:
  - "[[Seed_灵感来源]]"
destination: "[[02_Cathedral]]"
weights:
  volume: 0.4
  substance: 0.6
---
```dataviewjs
// 🎮 RPG HUD Engine (Final Stable)
const p = dv.current();
const t = p.target_words || 3000;

let c = 0;
try {
    let content = await dv.io.load(p.file.path);
    const anchor = "// " + "🛑 END_OF_HUD";
    const parts = content.split(anchor);
    if (parts.length > 1) {
        let body = parts[parts.length - 1];
        body = body.replace(/^[\s\n]*`{3}[\s\n]*/, "");
        c = body.trim().length;
    }
} catch (e) { c = 0; }

const score = Math.round((Math.min(c/t, 1)*100)*0.4 + (p.file.tasks?.length > 0 ? (p.file.tasks.filter(t=>t.completed).length/p.file.tasks.length)*60 : 0));

dv.paragraph(`
<div id="fusion-cockpit" style="position:fixed; top:60px; right:40px; width:360px; background:rgba(10,10,15,0.7); backdrop-filter:blur(12px); border:1px solid rgba(0,255,200,0.3); border-radius:12px; padding:12px; z-index:9999; color:white; font-family:sans-serif;">
    <div style="font-size:10px; opacity:0.6; margin-bottom:8px; display:flex; justify-content:space-between;">
        <span>⚡ ${p.origin || "Origin"}</span><span>🏰 ${p.destination || "Destination"}</span>
    </div>
    <div style="height:20px; background:rgba(0,0,0,0.5); border-radius:10px; overflow:hidden; position:relative; border:1px solid rgba(255,255,255,0.1);">
        <div style="width:${score}%; height:100%; background:linear-gradient(90deg, #00ffc8, #008f7a); transition:width 0.5s;"></div>
        <div style="position:absolute; width:100%; height:100%; top:0; left:0; display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:900;">RPG MODE ${score}%</div>
    </div>
    <div style="display:flex; justify-content:space-between; margin-top:8px; font-size:11px; font-weight:bold; color:rgba(0,255,200,0.8);">
        <div>📝 ${c} / ${t}</div><div>⚔️ ${p.file.tasks?.filter(t=>t.completed).length || 0} / ${p.file.tasks?.length || 0}</div>
    </div>
</div>
`);

// 🛑 END_OF_HUD
