---
name: event-tracking-common
description: A utility skill providing shared utilities, schema generation templates, and validation logic for event-tracking reports.
---

# Event Tracking Common Skill

This is a utility skill meant to be shared across various event-tracking pipelines. Do not use this to generate a specific situational report; rely on specialized skills (like `taiwan-strait-daily-brief`) for the actual reporting rules.

## Capabilities

1. **Skeleton Generation** (Not Yet Configured): Generates basic scaffolding for a new event based on `AGENTS.md` and standard project trees.
2. **Logging standard**: Ensures that index JSON updates conform to `shared/schemas/daily_report.schema.json`.

*Note: More shared utilities will be added here as new events are tracked.*
