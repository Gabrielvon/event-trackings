# Event Trackings

自动化国际事件跟踪与风险日报生成系统。基于 Codex Skills + Automations 实现每日定时运行。

## 项目结构

```
event-trackings/
├─ .agents/skills/          # Codex Skills（执行方法）
├─ .codex/                  # Codex 配置
├─ automations/             # Automation 触发提示词
├─ events/                  # 各事件的产物目录
│  └─ <event-name>/
│     ├─ AGENTS.md          # 事件专属规则
│     ├─ reports/           # 日报产物
│     ├─ data/              # 快照与衍生数据
│     └─ README.md          # 事件说明
└─ shared/                  # 跨事件共享资源
```

## 组织原则

| 层级 | 职责 |
|------|------|
| 根目录 `AGENTS.md` | 平台通用规则 |
| `events/<name>/AGENTS.md` | 领域专属规则 |
| `.agents/skills/` | 执行方法 |
| `automations/` | 触发频率与提示词 |
| `events/<name>/reports/` | 产物存储 |

## 当前跟踪事件

| 事件 | Skill | 状态 |
|------|-------|------|
| 台海风险 | `taiwan-strait-daily-brief` | ✅ 就绪 |

## 快速开始

1. 在 Codex app 中打开本项目
2. 为目标事件创建 Automation，使用 `automations/<event>.prompt.txt` 中的提示词
3. 确保 `.codex/config.toml` 中的 `writable_roots` 指向本项目实际路径
4. 确保 `network_access = true`（日报需要联网抓取来源）
