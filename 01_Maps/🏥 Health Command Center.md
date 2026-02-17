# 🏥 Health Command Center

## ⚡ 本周机能趋势

```dataview
TABLE WITHOUT ID
  link(file.link, file.name) as "📅 日期",
  sleep_hour + " h" as "💤 睡眠",
  choice(energy_level >= 80, "🟢 High (" + energy_level + ")", choice(energy_level >= 60, "🟡 Med (" + energy_level + ")", "🔴 Low (" + energy_level + ")")) as "🔋 能量",
  workout as "💪 运动",
  "¥ " + daily_spend as "💰 消费",
  choice(win_the_day, "🏆 WIN", "💀 LOSS") as "⚔️ 战果"
FROM "Daily Notes" OR #Daily
WHERE sleep_hour != null
SORT file.name DESC
LIMIT 7
```

