---
name: taiwan-strait-daily-brief
description: Generate a daily Chinese-language Taiwan Strait situation report with a 5-indicator risk score, reasons for each score, trend versus the previous run, and cited live sources. Use for recurring daily cross-strait briefings or whenever the user asks to score Taiwan Strait risk.
---

# Taiwan Strait Daily Brief

## Purpose
Produce a daily, Chinese-language situation report on the Taiwan Strait that is concise, source-driven, and easy to compare day to day.

## When to use this skill
Use this skill when:
- the user asks for a Taiwan Strait daily brief
- the user asks for a Taiwan Strait risk scorecard
- the task is a recurring or scheduled briefing about cross-strait developments
- the task should assess whether the situation is cooling, stable, or heating up

Do not use this skill for:
- deep historical essays without a daily risk-scoring need
- generic China or Indo-Pacific news that is unrelated to Taiwan Strait risk
- tasks that explicitly forbid live web verification

## Hard requirements
1. **Always verify with live sources before scoring.**
2. **Write the report in Chinese.**
3. **Every score must include both a reason and source references.**
4. **Use concrete dates, not vague words like “today” or “recently” without dates.**
5. **If fresh sourcing is unavailable because the environment has no network access, say so clearly and do not pretend to know the latest situation.**
6. **If there are no meaningful changes, still produce a short daily report and mark the trend as stable.**
7. **Never invent military counts, deployments, or statements.**

## Preferred source order
Use the freshest and most authoritative sources available. Prefer these, in roughly this order:

### Tier 1: official / primary
- Taiwan Ministry of National Defense (MND)
- PLA Eastern Theater Command / PRC Ministry of National Defense
- China Coast Guard / China Maritime Safety Administration if directly relevant
- U.S. Department of Defense / INDOPACOM / State Department
- Japan Ministry of Defense / Ministry of Foreign Affairs
- Official statements by Taiwan Presidential Office, Executive Yuan, or Mainland Affairs Council when directly relevant

### Tier 2: high-quality reporting
- Reuters
- Associated Press
- Financial Times
- Wall Street Journal
- Nikkei Asia
- BBC
- major reputable regional outlets with clear sourcing

### Tier 3: analytical support
- ISW/CTP, think tanks, defense analysis shops, or specialist researchers
Use these to support interpretation, not as the only basis for major factual claims.

## Time window
Default to the last 24 hours.
If the last 24 hours is too thin, extend to the last 72 hours and say that you did so.

## Scoring rubric
Score each item from 0 to 2.

### 1) 军事压力表
- 0 = 常态噪音；无显著异常舰机活动
- 1 = 明显升温；舰机活动高于常态或连续高位
- 2 = 危险信号；持续高压、多方向动作、东部外海/巴士海峡/关键节点明显升级

### 2) 封控/演训表
- 0 = 无新的封控或显著升级演训
- 1 = 联合战备警巡、实弹演训、封控色彩增强
- 2 = 明显接近或进入准封锁/要域夺控/长时段禁限航演练

### 3) 灰区/执法表
- 0 = 无新增实质动作
- 1 = 海警、无人机、执法、法律战、网络/通信干扰等灰区压力增强
- 2 = 实质性登检、逼近、外岛/航路/海缆/通信链路干扰升级

### 4) 外援/盟友表
- 0 = 美日等主要外援口径与部署平稳
- 1 = 表态趋强或出现有限协调/部署变化
- 2 = 美日等同步显著升温，出现更明显的联动部署或危机确认信号

### 5) 能源/认知表
- 0 = 常规宣传，无明显新外溢
- 1 = 能源、供应链、金融、航运或“美国顾不过来”叙事增强
- 2 = 经济与认知压力同步放大，形成对台或对盟友的实质性外溢压力

## Total score interpretation
- 0–3 = 🟢 绿色
- 4–6 = 🟡 黄色
- 7–10 = 🔴 红色

## Output requirements
Return the report in this structure exactly:

# 台海风险评分（YYYY-MM-DD）

## 一、总分
- 总分：X / 10
- 等级：🟢 绿色 / 🟡 黄色 / 🔴 红色

## 二、分项评分
### 1. 军事压力表：X / 2
- 打分理由：
  - ...
- 参考来源：
  - ...

### 2. 封控/演训表：X / 2
- 打分理由：
  - ...
- 参考来源：
  - ...

### 3. 灰区/执法表：X / 2
- 打分理由：
  - ...
- 参考来源：
  - ...

### 4. 外援/盟友表：X / 2
- 打分理由：
  - ...
- 参考来源：
  - ...

### 5. 能源/认知表：X / 2
- 打分理由：
  - ...
- 参考来源：
  - ...

## 三、综合判断
- 一句话结论：
- 与上一期相比：⬆️ 升温 / ➡️ 持平 / ⬇️ 降温
- 是否接近“准封锁”测试：是 / 否
- 今日最重要的 2–3 个观察点：
  1. ...
  2. ...
  3. ...

## 四、来源总表
- 列出本次使用的全部来源，优先写标题 + 机构 + 日期

## 五、不确定性
- 说明哪些判断证据较强，哪些只是早期信号或仍待确认

## File outputs
After drafting the report, save it to:
- `events/taiwan-strait/reports/YYYY/YYYY-MM-DD.md`

Also maintain:
- `events/taiwan-strait/reports/latest.md` as a copy of the newest report
- `events/taiwan-strait/reports/index.json` as a simple append-only log with:
  - date
  - total_score
  - level
  - trend_vs_previous
  - key_points (array of short strings)

If the folder does not exist, create it.

## How to compare with the previous run
1. Read `events/taiwan-strait/reports/latest.md` or the previous dated report if it exists.
2. Compare:
   - total score
   - whether any indicator moved by 1 or more
   - whether new indicators crossed from 0→1, 1→2, or reversed
3. Summarize the comparison in one short line.

If no previous report exists, say:
- 与上一期相比：N/A（首期报告）

## Quality bar
- Prefer 4+ fresh sources when possible.
- If a claim is especially significant (for example, blockade-style drills, direct vessel inspections, major U.S.-Japan force posture changes), try to confirm it with more than one source.
- Keep the report decision-oriented, not essay-like.
- Avoid jargon unless it improves precision.
- Be explicit about uncertainty.
