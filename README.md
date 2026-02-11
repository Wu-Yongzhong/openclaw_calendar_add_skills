# 📅 openclaw-calendar-add-skill

Add events to macOS Calendar via OpenClaw. Adds events to the "工作" (Work) calendar by default.

## 📂 Repository Contents

- `SKILL.md` - Skill documentation for OpenClaw
- `calendar-add` - Main executable script (Bash + AppleScript)

## ✨ Features

- Add calendar events via natural language (through OpenClaw)
- Defaults to "工作" (Work) calendar
- Configurable title, location, description
- 1-hour duration (default)
- macOS Calendar integration

## 🔧 Requirements

- macOS with Calendar app
- OpenClaw installed
- Terminal with Calendar access permissions

### macOS Permissions

Grant Calendar access in:
```
System Settings > Privacy & Security > Calendar
→ Enable Terminal (or iTerm)
```

## 🚀 Usage

### Through OpenClaw

Just tell OpenClaw naturally:

```
"明天下午3点添加一个会议"
"安排周五上午10点的视频会议"
"下周一早上9点有项目讨论"
```

### Direct Command

```bash
# Basic: calendar-add <summary> <location> <description> <days> <hour>

# Tomorrow at 3PM
./calendar-add "团队会议" "Zoom" "讨论项目进度" 1 15

# Today at 2PM
./calendar-add "客户电话" "" "回访客户" 0 14

# Next Monday at 10AM
./calendar-add "周会" "会议室A" "周一例行会议" 7 10
```

### Parameters

| Position | Description | Example |
|----------|-------------|---------|
| 1 | Event title | "团队会议" |
| 2 | Location (optional) | "Zoom", "会议室A" |
| 3 | Description (optional) | "讨论项目进度" |
| 4 | Days from today | 1 = tomorrow, 7 = next week |
| 5 | Hour (24h format) | 14 = 2PM, 9 = 9AM |

## 📖 Installation

### Option 1: Clone to OpenClaw Skills

```bash
# Clone to your skills directory
git clone https://github.com/Wu-Yongzhong/openclaw_calendar_add_skills.git ~/openclaw/skills/calendar

# Make executable
chmod +x ~/openclaw/skills/calendar/calendar-add

# Restart OpenClaw
openclaw gateway restart
```

### Option 2: Install via Git URL

Configure in OpenClaw config:
```json
{
  "skills": {
    "load": {
      "extraDirs": ["/path/to/openclaw_calendar_add_skills"]
    }
  }
}
```

## 🔒 Security Notes

- This skill uses `osascript` to interact with Calendar
- Requires Calendar access permissions on macOS
- Events added to "工作" calendar by default
- Review permissions before use

## 📝 Examples

### Example 1: Team Meeting

```bash
./calendar-add "团队周会" "线上" "每周项目进度同步" 1 10
```
Result: Tomorrow at 10AM, 1-hour team meeting in "工作" calendar

### Example 2: Video Conference

```bash
./calendar-add "客户演示" "Zoom" "产品功能演示" 3 14
```
Result: In 3 days at 2PM, 1-hour video call

### Example 3: Simple Reminder

```bash
./calendar-add "提交报告" "" "完成季度报告" 5 16
```
Result: In 5 days at 4PM, simple reminder

## 🐛 Troubleshooting

### Event not added?

- Check Calendar permissions in System Settings
- Verify "工作" calendar exists in Calendar app
- Check Terminal/iTerm has Full Disk Access

### Wrong date/time?

- Ensure parameters are in correct order
- Hour must be 24h format (14 = 2PM, not 2)

## 📄 License

MIT License

## 👤 Author

Wu-Yongzhong
