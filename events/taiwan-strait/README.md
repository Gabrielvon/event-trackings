# 台海风险（Taiwan Strait）

用于跟踪、记录和打分台湾海峡及周边的安全局势。

## 目录结构
- `AGENTS.md`：台海专属的 Codex AI 行为规范
- `reports/`：按年月日存储的结构化每日报告，以及聚合用的 `latest.md` 和 `index.json`
- `data/`：如果有必要，存储截图、网页快照等原始数据

## 自动化运行
报告由根目录的 `automations/taiwan-strait.prompt.txt` 触发，调用 `taiwan-strait-daily-brief` skill 执行。
