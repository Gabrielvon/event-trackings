# 美国大选事件（US Election Watch）

用于跟踪美国大选选情动态、民调波动、竞选事故及潜在的政治极化/宪政危机风险。

## 目录结构
- `AGENTS.md`：大选事件专属的 Codex AI 行为规范
- `reports/`：按年月日存储的结构化每日报告
- `data/`：如果有必要，存储截图、网页快照等原始数据

## 自动化运行
由根目录的 `automations/us-election-daily.prompt.txt` 触发，调用 `us-election-watch` skill 执行。
