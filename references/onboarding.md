# Onboarding Checklist

Use this on first setup or when profile data is incomplete.

## Step 1: Confirm Setup

1. Confirm `FITNESS.md` exists in workspace root.
2. Confirm `fitness/program.md` exists.
3. Confirm `fitness/history/` and `fitness/weekly/` folders exist.
4. If missing, initialize before coaching.

## Step 2: Collect User Inputs

Collect concise answers for:

- Name and timezone
- Primary goal (fat loss, strength, skill, conditioning, hybrid)
- Secondary goals
- Training age/experience
- Available days and session length
- Equipment access
- Injury history and current pain flags
- Preferred training style and disliked movements
- Preferred coaching tone (for example direct/no-cheerleading vs more motivational)
- Recovery constraints (sleep, stress, work schedule)
- Environment constraints (for example weather-dependent training, travel, limited space)
- Reminder preference (off, heartbeat nudges, or exact-time cron)
- Committed workout time/window
- Reminder cadence and preferred times
- Quiet hours / do-not-disturb window
- Preferred follow-up check-in timing after workout
- Weekly check-in/review preference (day/time/frequency)
- Program source preferences (for example Reddit Recommended Routine, existing coach plan, or custom)

## Step 3: Build Baseline Plan

1. Read `references/program-building.md`.
2. Use `references/program-template.md`.
3. Research and validate any user-requested source program before prescribing.
4. Pick frequency that fits the real schedule.
5. Define progression and deload.
6. Write full prescribed plan into `fitness/program.md`.
7. Write plan summary into `FITNESS.md`.

## Step 4: Start Tracking

1. Add first session entry in `fitness/history/YYYY-MM-DD.md`.
2. Log subjective effort and any pain notes.
3. Update `FITNESS.md` Active Adjustments if needed.
4. Add at least one fallback training option for constrained days.
5. Confirm that today's prescribed workout can be generated from `fitness/program.md`.

## Step 5: Weekly Loop

At week end:

1. Create/update `fitness/weekly/YYYY-Www.md`.
2. Summarize adherence, wins, issues, and next-week changes.

## Step 6: Configure Reminders (Optional)

1. Read `references/reminders-and-automation.md`.
2. If the user wants reminders, select Heartbeat or Cron method.
3. Confirm before creating or editing any scheduled job.
4. Propose a reminder loop anchored to the committed workout schedule:
   - workout delivery aligned to committed workout time
   - follow-up check-in at user-preferred timing after workout
   - weekly review/check-in at user-selected day/time
5. Save reminder settings in `FITNESS.md`.
