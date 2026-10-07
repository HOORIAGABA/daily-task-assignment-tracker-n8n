# daily-task-assignment-tracker-n8n

n8n workflows that track daily ClickUp task assignments and report them into Google Sheets, per team.

**What it does:**
- Triggers in real time when a task is assigned in ClickUp
- Fetches full task details and formats dates in PKT (Asia/Karachi) timezone
- Writes/accumulates one row per team member per day in Google Sheets (`unique_key = memberId_date`)
- Prevents duplicate entries if the same event fires more than once
- Tracks unique daily member activity across teams

**Team variants included:**
- DevOps
- Frontend
- Backend
- AI
- QA

Part of a connected set of daily productivity trackers covering the full task lifecycle (assignment → in-progress → pending → testing → deployment → completed), used across engineering teams.

**Setup:** each workflow JSON uses placeholder ClickUp Team/List IDs and a placeholder Google Sheet ID — replace these with your own workspace and sheet, add your own ClickUp API and Google Sheets credentials in n8n, then activate.