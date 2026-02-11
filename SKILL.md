---
name: calendar
description: Add events to macOS Calendar using AppleScript. Adds to "工作" (Work) calendar by default.
metadata:
  openclaw:
    emoji: "📅"
    os: ["darwin"]
    requires:
      bins: ["osascript"]
    install: []
---

# Apple Calendar Skill for OpenClaw

See **[README.md](./README.md)** for full documentation.

## Quick Start

Just tell OpenClaw naturally:

```
"明天下午3点添加一个会议"
"安排周五上午10点的视频会议"
```

## Parameters

| Position | Description | Example |
|----------|-------------|---------|
| 1 | Event title | "团队会议" |
| 2 | Location (optional) | "Zoom" |
| 3 | Description (optional) | "讨论项目进度" |
| 4 | Days from today | 1 = tomorrow |
| 5 | Hour (24h format) | 14 = 2PM |

## Notes

- Events added to "工作" (Work) calendar
- Default duration: 1 hour
- macOS Calendar must be accessible
