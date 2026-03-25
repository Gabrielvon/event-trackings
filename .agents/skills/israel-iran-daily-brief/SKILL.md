---
name: israel-iran-daily-brief
description: Generate a daily Chinese-language Israel-Iran situation report with a 5-indicator risk score, reasons for each score, trend versus the previous run, and cited live sources. Use for recurring daily Middle East briefings involving Israel and Iran.
---

# Israel-Iran Daily Brief

## Purpose
Produce a daily, Chinese-language situation report on the Israel-Iran conflict that is concise, source-driven, and easy to compare day to day.

## Hard requirements
1. **Always verify with live sources before scoring.**
2. **Write the report in Chinese.**
3. **Every score must include both a reason and source references.**
4. **Use concrete dates, not vague words like “今天” without dates.**
5. **Follow the shared source policy in `shared/source-policy.md`.**

## Scoring rubric (0-2 per item)

### 1) 直接军事冲突表
- 0 = 无直接打击或轻微越境试探
- 1 = 针对单一人员/设施的外科手术打击或高烈度报复
- 2 = 针对本土的大规模导弹/无人机袭击、本土宣战或防空网全面交火

### 2) 代理人战线表
- 0 = 常规炮击/火箭弹袭扰
- 1 = 代理人（真主党/胡塞等）发起超常规模攻击或引发严重伤亡/停工
- 2 = 多线代理人协同发动瘫痪性打击或进入全面战争动员状态

### 3) 战略威慑/核博弈表
- 0 = 常规政治修辞
- 1 = 提升核浓缩等级、高级军官发出明确的毁灭性威胁或防备升级
- 2 = 退出核协定底线、开始核武冲刺或部署战略核载具/防空网进入最高战备

### 4) 国际干预/调停表
- 0 = 国际停火呼吁或例行谴责
- 1 = 联合国/美/俄出台实质性施压决议，或美军进行区域协防部署调整
- 2 = 域外大国直接卷入战事，或全面切断外交与军事联系

### 5) 国内政治/动员表
- 0 = 国内政局稳定，无异常动员
- 1 = 战时内阁/最高领袖释放强硬信号，局部征召预备役
- 2 = 全国紧急状态，全面战争动员或面临重大国内政变/撕裂

## Total score interpretation
- 0–3 = 🟢 绿色
- 4–6 = 🟡 黄色
- 7–10 = 🔴 红色

## Output requirements
See standard format in automation prompt.

## File outputs
Report path: `events/israel-iran/reports/YYYY/YYYY-MM-DD.md`
Also update `latest.md` and `index.json` in the same directory.
