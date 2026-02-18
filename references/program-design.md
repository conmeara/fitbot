# Program Design Guide

Read this when building or revising a program. Don't generate a generic template — build something a real coach would hand a client.

## Needs Analysis First

Before writing a single exercise, understand: training age, movement quality, injury history, equipment, schedule constraints, recovery capacity (sleep, stress, nutrition). The program flows from this assessment — it's not a template with goals pasted on top.

## Research the Method

If the user wants a specific method (RR, 5/3/1, GZCLP, Supple Leopard, whatever), deep research the actual current source material and understand it before prescribing. If they don't have a preference, choose one that fits their needs analysis and explain why.

## Design Principles

**Adherence is the foundation.** A 3-day program they do beats a 6-day program they abandon. Fit the schedule they have, not the one you wish they had. This overrides everything below.

**Train across fitness qualities, not just strength or hypertrophy.** Galpin's nine adaptations: skill, speed, power, strength, hypertrophy, muscular endurance, anaerobic capacity, VO2max, long-duration endurance. Most people need at minimum: resistance training (3x/week) + Zone 2 cardio (150-200 min/week) + one HIIT or VO2max session per week. Adaptations closer together on that list are more compatible; those further apart can interfere — but the interference effect between strength and endurance is overblown. Zone 2 at conversational pace has almost no ability to block hypertrophy.

**Exercises don't determine adaptation — execution does.** The same exercise trains strength, power, or hypertrophy depending on load, intent, rest, and volume. Program the parameters, not just the exercises.

**Match protocols to the goal:**
- **Strength/Power:** Galpin's 3-5 rule — 3-5 exercises, 3-5 sets of 3-5 reps, 3-5 min rest, 70%+ 1RM. No need to train to failure.
- **Hypertrophy:** 10-20 sets/muscle/week, 8-15 reps (range of 4-30 works), ~2 min rest, stop ~2 reps short of failure. Volume is the primary driver.
- **Zone 2 endurance:** 30-75 min continuous at conversational/nasal-breathing pace. If they must mouth-breathe, they should slow down.
- **HIIT/anaerobic:** 4-8 intervals of 20-90 sec max effort, 1-2x/week. Target ~5-6 total minutes at max HR per week. Rest until nasal breathing returns between intervals.

**Mesocycles have shape — flat programs are not programs.** Structure each mesocycle as 3-5 weeks of accumulation + 1 week deload. Start volume at MEV (~6-10 hard sets/muscle/week), add 1-3 sets/week, approach MRV by the final week, then deload back to maintenance volume. Intensity progresses from conservative (3-4 RIR in week 1) to challenging (0-1 RIR in the final week). If every week looks the same, it's a list of exercises, not a program.

**Use RIR, not fixed percentages** (for intermediates+). Prescribe "4x6 @ RPE 8" not "4x6 @ 80%." This autoregulates for daily readiness. For beginners who can't gauge RIR yet, use simple rep targets: "add weight when you get all reps across all sets."

**Progressive overload has six levers — not just "add weight."** Load, volume (sets/reps), density (shorter rest), range of motion, tempo (slow eccentrics, pauses), and complexity (bilateral → unilateral, stable → unstable). Use them in roughly that priority order. When load stalls, progress through the others.

**Select exercises by movement pattern, not by name.** Horizontal push, vertical push, horizontal pull, vertical pull, hip hinge, squat/knee-dominant, carry/loaded locomotion. Balance all patterns across the week. For bodyweight: include horizontal and vertical planes for both push and pull. Every pattern needs a substitution chain.

**Sequence intelligently.** Compounds before isolation. Most fatiguing movements first in the session. Don't stack competing recovery demands on consecutive days (e.g., heavy squats Monday and heavy deadlifts Tuesday share hip/back recovery).

**Choose the right periodization model.** Beginners: linear (simple, works). Intermediates training 3-4x/week with no competition date: daily undulating (vary rep ranges across the week). Advanced with peaking needs: block periodization. Don't default to linear for everyone.

**Recovery is half the equation.** Stress + Recovery = Adaptation. Without recovery, there is no adaptation. If you program hard training, you must also account for recovery capacity. Watch for overreaching signs: declining performance across sessions, elevated resting HR, persistent soreness, disrupted sleep. When 2+ co-occur, deload immediately.

**Deload is not optional.** Every 3-6 weeks, or immediately when overreaching signs appear. Deload = maintenance volume at 50-60% working loads. Maintain movement patterns, cut intensity and volume.

## A Complete Program Includes

- **The Why** — rationale for the approach
- **Weekly schedule** with environment adaptations (rain plan, travel plan, no-gym plan)
- **Daily non-negotiables** — skill practice, mobility, things that happen regardless of the main workout
- **Full workout templates** — warm-up through finisher, with exact exercises, sets, reps, rest, RIR targets
- **Progression ladders for every exercise** — specific levels with clear criteria to advance. For bodyweight: progression through leverage and difficulty, each step spelled out.
- **Deload protocol** — what it looks like, triggers for unscheduled deloads
- **Substitution chains** organized by movement pattern
- **Alternative workouts** for constrained environments (home, hotel, rain day)
- **Rehab/prehab prescriptions** for issues relevant to the user
- **Benchmarks** — what to test and how often
- **Week 1 checklist** — clear first steps

Write the full program to `fitness/program.md`. It should be complete enough that the user could follow it without you — like a printed program from a real coach. Update `FITNESS.md` with the summary.
