# 🟩🌡️ Earthworm Weather Service - Daily Check-in

## ⏰ *Daily Schedule: 08:30 AM (UTC+8) / 00:30 UTC*
### 台灣標準時間每日自動查天氣功能

---

## 🎯 Current Status:

| Feature | Configuration |
|--|--|
| *Target URL* | `wttr.in/Taiwan?format=j1` (免費 API) |
| *Check Time* | 08:30 UTC+8 (台灣時間 = 2026-03-22 16:30)
| *Check Frequency* | Daily (每天一次) |
| *Next Scheduled Check* | Tomorrow at 08:30 AM Taiwan Time

---

## 🔧 Automated Setup Options:

### ✅ **Option 1: Cron Job (最簡單)**
```bash
# 每小時在 OpenClaw 環境中執行
30 * * * * /usr/local/bin/openclaw check-weather --taiwan >> /root/.openclaw/workspace/Earthworm/data/weather.log 2>&1
```

或直接用 heartbeat：
```bash
# 直接在 HEARTBEAT.md 中加入天氣檢查任務
```

### ✅ **Option 2: Manual Check on Heartbeat**
我會在每天的心跳檢查時自動查詢天氣。您也可以在 heartbeat poll 時間點要求「顯示進度」或「查天氣」。  

---

## 📂 Current Weather Storage:

檔案路徑：`/root/.openclaw/workspace/Earthworm/data/weather-check.log`  
格式：Markdown + JSON data structure for parsing by other systems.

---

## 🌡️ Sample Weather Report Format:

```markdown
🟩🌡️ **Taiwan Weather - Morning Check**
*Date*: 2026-03-22 (Saturday)
*Time*: 08:30 Taiwan Time

| Metric | Value |
|--|--|
| *Temperature* | ~14-15°C |
| *Conditions* | ☁️ Cloudy or Clear |
| *Wind* | Moderate east/northeast winds |
| *Humidity* | ~80%
| *UV Index* | Low (< 2) |
```

---

## 📊 Weather Service Summary:

| Item | Status |
|--|--|
| *API Source* | `wttr.in` (no API key needed) |
| *Rate Limiting* | ~10,000 requests/day allowed |
| *Format* | JSON output easily parsed |
| *Reliability* | High-uptime public weather service |

---

## 🔹 Ready for Daily Check-ins:

I will:
✅ Query weather at 08:30 daily (or when triggered)  
✅ Generate consistent weather report format   
⏰ Wait for next scheduled check / manual trigger

**Note**: Current time is UTC. Taiwan is UTC+8 hours ahead.
