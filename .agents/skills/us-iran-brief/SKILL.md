---
name: us-iran-brief
description: Generate a daily Chinese-language US-Iran situation report with a 5-indicator risk score. Use for tracking US-Iran relations, Red Sea shipping, and middle east US base tensions.
---

# US-Iran Daily Brief

## Purpose
Produce a daily, Chinese-language situation report on US-Iran tensions.

## Hard requirements
1. **Always verify with live sources before scoring.**
2. **Write the report in Chinese.**
3. **Every score must include both a reason and source references.**
4. **Follow the shared source policy in `shared/source-policy.md`.**

## Scoring rubric (0-2 per item)

### 1) 美军部署与行动表
- 0 = 常规巡航，无显著异常
- 1 = 防御性拦截增加，针对亲伊朗武将的有限防卫打击，航母战斗群调配
- 2 = 针对伊朗革命卫队高层或伊朗本土的直接军事打击，进入战争边缘

### 2) 海上航运与红海表
- 0 = 零星袭扰，航运基本畅通
- 1 = 商船频遭导弹/无人机袭击，航运费率显著上升，多数公司绕航
- 2 = 航道彻底瘫痪，军舰被直接击中或发生大规模生态/人员灾难

### 3) 伊朗地区反击表
- 0 = 政治口号为主，无实质性越轨动作
- 1 = 针对美军基地的无人机/火箭弹袭击增加，或截停扣押油轮
- 2 = 造成美军显着伤亡，或封锁霍尔木兹海峡的实质性动作

### 4) 制裁与能源市场表
- 0 = 维持现有制裁，原油市场平稳
- 1 = 美国出台新的二级制裁，或原油价格因地缘恐慌出现可观波动
- 2 = 全面封堵原油出口通道，或油价出现极端剧烈飙升

### 5) 外交接触与核谈判表
- 0 = 常规的外交僵局或密战
- 1 = 间接对话破裂，或IAEA发出严厉谴责决议
- 2 = 伊朗官宣跨核门槛，或由于严重事件导致所有幕后沟通渠道断绝

## Total score interpretation
- 0–3 = 🟢 绿色
- 4–6 = 🟡 黄色
- 7–10 = 🔴 红色

## File outputs
Report path: `events/us-iran/reports/YYYY/YYYY-MM-DD.md`
Also update `latest.md` and `index.json` in the same directory.
