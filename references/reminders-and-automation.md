# Reminders and Automation (OpenClaw)

Use this when the user wants workout reminders, check-ins, or weekly recap prompts.

## Decide the Reminder Method

Choose based on user needs:

- `heartbeat` for flexible, context-aware nudges.
- `cron` for exact-time reminders.
- `off` if user does not want reminders.

## Capture These Settings During Onboarding

- Cadence (daily, weekdays, specific days, weekly)
- Preferred reminder time and timezone
- Follow-up check-in time
- Quiet hours
- Delivery target (main session or specific channel)
- Reminder style (short nudge vs detailed plan)

Store these in `FITNESS.md` under `Reminders and Automation`.

Default recommendation for proactive daily coaching:

- workout delivery at 07:00
- follow-up check-in at 11:00

## Heartbeat Method

Use when timing can be approximate and you want one place for periodic checks.

1. Add a short reminder task to `HEARTBEAT.md`.
2. Keep reminder output concise and action-first.
3. Respect quiet hours and skip non-urgent nudges.
4. On reminder trigger, read `FITNESS.md` and `fitness/program.md` before composing message.
5. If no reminder is due, do nothing.

Example `HEARTBEAT.md` tasks:

```md
- Fitbot reminder: If user has reminders enabled and a workout is due today, send one short nudge with today's top priority. Respect quiet hours.
- Fitbot follow-up: If a follow-up check-in is due today, ask for completion status, effort (1-10), and pain flags, then update `fitness/history/`.
```

## Cron Method

Use when exact schedule timing matters.

Rules:

1. Ask for explicit confirmation before creating or editing cron jobs.
2. Use stable names so jobs are idempotent:
   - `fitbot:daily-reminder`
   - `fitbot:weekly-review`
   - `fitbot:daily-follow-up`
3. Check existing jobs first and update instead of duplicating.

Command pattern:

```bash
openclaw cron list
```

Daily reminder example:

```bash
openclaw cron add \
  --name "fitbot:daily-reminder" \
  --cron "0 7 * * 1-5" \
  --tz "America/Los_Angeles" \
  --session isolated \
  --message "Send today's workout reminder based on FITNESS.md and current plan." \
  --announce
```

Weekly review example:

```bash
openclaw cron add \
  --name "fitbot:weekly-review" \
  --cron "0 18 * * 0" \
  --tz "America/Los_Angeles" \
  --session isolated \
  --message "Prompt weekly training review and update fitness/weekly/YYYY-Www.md if needed." \
  --announce
```

Daily follow-up example:

```bash
openclaw cron add \
  --name "fitbot:daily-follow-up" \
  --cron "0 11 * * 1-5" \
  --tz "America/Los_Angeles" \
  --session isolated \
  --message "Ask how today's workout went, collect effort/pain feedback, and log to fitness/history/YYYY-MM-DD.md." \
  --announce
```

If a job already exists, edit it instead of adding another.

## Safety and UX Notes

- Do not spam reminders.
- Respect quiet hours.
- Keep reminders under a few lines unless user asks for detail.
- If user opts out, disable reminders and update `FITNESS.md`.
