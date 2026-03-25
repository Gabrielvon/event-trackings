# 美伊局势事件（US-Iran Security）

用于跟踪美国与伊朗及其武装代理人（特别是红海沿岸胡塞武装、伊拉克/叙利亚境内民兵）之间的驻军安全、航运打击和外交互动。

## 目录结构
- `AGENTS.md`：美伊事件专属的 Codex AI 行为规范
- `reports/`：按年月日存储的结构化每日报告
- `data/`：如果有必要，存储截图、网页快照等原始数据

## 自动化运行
由根目录的 `automations/us-iran-daily.prompt.txt` 触发，调用 `us-iran-brief` skill 执行。
