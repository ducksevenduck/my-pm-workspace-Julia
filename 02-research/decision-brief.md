# Decision Brief — Streak Comeback Experience

*For: Marcus, Head of Product. Prepared during discovery, drawing on interview-synthesis.md, nps-analysis.md, and competitive-matrix.md.*

## Situation

Day-7 retention dropped from 48% to 39% after the v2 streak/notification redesign, driven mainly by new users who break their streak in week 1 and never return. Three independent sources — user interviews, NPS feedback, and a competitive scan — now corroborate the same underlying problem.

## Key Findings

| # | Finding | Source |
|---|---|---|
| 1 | Streak-loss anxiety starts almost immediately (as early as day 4), well before the habit actually forms (~3 weeks) — churn risk exists before a user has even had a lapse. | Interviews |
| 2 | The punitive reset-to-zero is the single most frequent complaint in raw feedback (4 of 10 comments). | NPS |
| 3 | Losing the streak ended engagement entirely for several users (3 of 10 comments). | NPS |
| 4 | Notification tone/frequency is a secondary but real driver of disengagement — one user disabled all notifications after receiving three in one afternoon. | NPS |
| 5 | No competitor reviewed (Duolingo, Babbel, Elevate, Habitica, Streaks) offers a free, non-monetized recovery moment, and none proactively address pre-lapse anxiety. | Competitive matrix |

## Options Considered

| Option | What It Does | Primary Driver Addressed |
|---|---|---|
| **1. Notification tone fix** | Drop the guilt-based framing; replace "you lost your streak" language with something more encouraging. | Notification-driven disengagement (Finding 4) |
| **2. Reactive comeback experience** | Trigger a comeback moment after a user misses X days (threshold TBD) — candidates include a best-streak stat, a 60-second comeback lesson, and a one-tap streak-freeze. | Punitive reset / no recovery path (Findings 2–3) |
| **3. Proactive week-1 anxiety reduction** | Address streak-loss anxiety before any lapse happens, during the fragile early habit-formation window. | Pre-lapse anxiety (Finding 1) |

## Pros & Cons by Option

| Option | Pros | Cons |
|---|---|---|
| **1. Notification tone fix** | Directly answers a clear, cited complaint (notification fatigue/tone).<br>Low lift — copy/tone change on existing systems, no new infrastructure.<br>Fast to test and iterate. | Doesn't touch the punitive reset itself — the largest complaint (7 of 10 NPS comments) stays unresolved.<br>Tone alone may not retain users for whom the mechanic itself, not just the messaging, is the problem (e.g., Tom: "no way to recover it, nothing"). |
| **2. Reactive comeback experience** | Directly addresses the single biggest driver (punitive reset, no recovery path).<br>Matches what users are explicitly asking for (NPS: "why not this one," re: streak freeze) and what one long-term user credits for the habit sticking.<br>Fills a competitive gap no rival currently owns. | Key design decisions (day threshold, streak-freeze rules) are still undefined, adding scope/timeline risk within the 8-week window.<br>Reactive only — doesn't reduce anxiety that starts before a lapse even happens. |
| **3. Proactive week-1 anxiety reduction** | Targets churn risk at its earliest point — before a lapse happens at all — with the potential to prevent some breaks, not just recover from them.<br>Also unclaimed competitive white space. | Least defined option — no candidate mechanism proposed yet, meaning more upfront discovery work before it can be scoped.<br>Harder to isolate and measure — effects may take longer to surface in Day-7 retention than a reactive fix. |

## Recommended Action

> **Pursue all three options in parallel** for the remainder of the 8-week discovery phase — each is independently corroborated by a different data source and addresses a distinct driver of the retention drop.

## Why Now

| Factor | Why It Matters |
|---|---|
| **Converged evidence** | Three independent sources point to the same problem in the same discovery window — lower risk of solving the wrong thing. |
| **Compounding risk** | The issue is separate from Streakly's otherwise healthy 28% YoY MAU growth — it will keep compounding against a growing user base the longer it's unaddressed. |
| **Open competitive window** | No direct competitor has claimed this white space yet. |
