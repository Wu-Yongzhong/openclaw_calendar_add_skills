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

# Apple Calendar Skill

Add events to macOS Calendar via AppleScript.

## Setup

- macOS only
- Grant Calendar access in System Settings > Privacy & Security

## Usage

### Add Event

```bash
# Basic
calendar-add "会议标题" "" "" 1 14

# Full
calendar-add "团队会议" "Zoom" "讨论项目进度" 1 14
```

### Parameters

| Position | Description | Example |
|----------|-------------|---------|
| 1 | Event summary/title | "团队会议" |
| 2 | Location (optional) | "Zoom", "会议室" |
| 3 | Description (optional) | "讨论项目进度" |
| 4 | Days from today | 1 = tomorrow, 0 = today |
| 5 | Hour (24h format) | 14 = 2PM |

### Examples

```bash
# Tomorrow at 9AM
calendar-add "早会" "线上" "每日站会" 1 9

# Today at 3PM
calendar-add "客户电话" "" "回访客户" 0 15

# Next Monday at 10AM
calendar-add "周会" "会议室A" "周一例行会议" 7 10
```

## Notes

- Events added to "工作" (Work) calendar
- Default duration: 1 hour
- Time format: 24-hour

## From OpenClaw

Users can request via natural language:

```
"明天下午3点开会"
"添加日历：下周一上午10点讨论项目"
"安排周五下午2点的视频会议"
```
