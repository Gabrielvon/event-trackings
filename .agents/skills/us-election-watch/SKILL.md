---
name: us-election-watch
description: Generate a daily Chinese-language US Election tracking report with a 5-indicator risk and momentum score.
---

# US Election Watch

## Purpose
Produce a daily, Chinese-language tracking report on the United States presidential election (and relevant downstream effects).

## Hard requirements
1. **Always verify with live sources before scoring.**
2. **Write the report in Chinese.**
3. **Every score must include both a reason and source references.**
4. **Follow the shared source policy in `shared/source-policy.md`.**

## Scoring rubric (0-2 per item)
Note: The score here measures **Volatility / Election Tension**, not necessarily who is winning.

### 1) 全国民调与支持率表
- 0 = 民调走势平稳，无显著黑天鹅
- 1 = 出现可见交叉或显著缩窄差距，引发焦虑
- 2 = 民调雪崩/急剧逆转，或选举计票存在巨大的系统性争议疑虑

### 2) 摇摆州动向表
- 0 = 摇摆州无异常变动
- 1 = 关键州局部争议（如邮寄选票、诉讼前哨战）或关键背书反转
- 2 = 决定性摇摆州爆出彻底改变选情的丑闻或计票停顿/违宪风波

### 3) 选战言论与丑闻表
- 0 = 正常的政策辩论和竞选广告
- 1 = 严重的人身攻击、候选人失言风波、初级法律诉讼
- 2 = 候选人遭遇刑事定罪重大转折、遭遇人身安全威胁或严重违宪指控

### 4) 竞选资金与动员表
- 0 = 筹款正常按进度推进
- 1 = 某方遭遇明显的超级 PAC 倒戈或筹款暴降/暴增
- 2 = 出现涉嫌严重违法的资金链断裂，或社会面出现暴力集会动员

### 5) 外部地缘/经济溢出表
- 0 = 对外经济数据（如CPI/就业）正常，地缘无干涉
- 1 = 非农/通胀意外恶化显著影响选情，或出现温和的“十月惊奇”
- 2 = 爆发重大战争/经济崩盘，或者出现实质性的外国选举干预实锤

## Total score interpretation
- 0–3 = 🟢 绿色（选情稳定按部就班）
- 4–6 = 🟡 黄色（博弈极化进入焦灼）
- 7–10 = 🔴 红色（濒临宪政危机或极端撕裂）

## File outputs
Report path: `events/us-election/reports/YYYY/YYYY-MM-DD.md`
Also update `latest.md` and `index.json` in the same directory.
