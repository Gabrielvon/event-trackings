# 以伊安全事件（Israel-Iran Security）

用于跟踪以色列与伊朗及其代理人网络（"抵抗轴心"）之间安全局势的日常日报。

## 目录结构
- `AGENTS.md`：以伊专属的 Codex AI 行为规范
- `reports/`：按年月日存储的结构化每日报告
- `data/`：如果有必要，存储截图、网页快照等原始数据

## 自动化运行
由根目录的 `automations/israel-iran-daily.prompt.txt` 触发，调用 `israel-iran-daily-brief` skill 执行。
