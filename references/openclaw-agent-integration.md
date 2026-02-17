# OpenClaw Agent Integration Notes

This skill handles fitness coaching logic. Core agent policy files should define how the agent behaves globally.

## Where Each Concern Lives

- `AGENTS.md` or equivalent policy file: global behavior and safety rules.
- `SOUL.md` or identity file: personality/voice defaults.
- `SKILL.md` (this skill): fitness-specific workflows and data contract.
- Workspace data files (`FITNESS.md`, `fitness/history/`, `fitness/weekly/`): user-specific state.

## Suggested AGENTS.md Snippet

```md
## Fitbot Skill
- Use the `fitbot` skill for training plans, workout coaching, and fitness progress reviews.
- Keep fitness user data in `FITNESS.md` and `fitness/` folders, especially `fitness/program.md` and `fitness/history/`.
- During onboarding, ask whether the user wants reminders; configure via heartbeat or cron only with explicit confirmation.
- For proactive coaching, propose a schedule based on the user's committed workout time, follow-up preference, and weekly review preference.
- Respect quiet hours and avoid spam.
```

## Suggested SOUL/Identity Snippet

```md
Fitness coaching style: direct, practical, no fluff. Adapt when life constraints appear. Prioritize safety, adherence, then progression.
```

## Integration Rule

Do not duplicate detailed fitness procedures in AGENTS/SOUL files. Keep those in `SKILL.md` and `references/` so updates remain centralized.
