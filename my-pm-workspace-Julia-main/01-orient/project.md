# Streakly Comeback Experience — Project Brief

*Status: Draft skeleton from initial planning discussion. To be reviewed Thursday.*

## Snapshot

- **Product:** Streakly — a consumer habit + micro-learning app (languages, guitar, coding, chess) where a daily streak is the core habit loop.
- **Squad:** Engagement squad (home screen, daily lesson loop, streak mechanics, push notifications).
- **Current phase:** Discovery — no designs, no committed scope, 8 weeks from sprint kickoff.
- **Key stakeholders:** Raj (Senior Engineer), Lena (Product Designer), you (PM), Marcus (Head of Product, your manager).

## Problem Statement

Streakly is a habit + micro-learning app (languages, guitar, coding, chess) where a daily streak is the core habit loop. This brief covers the Comeback experience, owned by the Engagement squad (home screen, daily lesson loop, streak mechanics, push notifications) — a triad of Raj (engineer), Lena (designer), and the PM, reporting to Marcus (Head of Product). See [context.md](context.md) for full company and role background.

Streakly's acquisition funnel works: users install, pick a track, and finish their first lesson. The problem is what happens next. Day-7 retention has dropped from 48% to 39% since the streak redesign shipped.

The drop is sharpest among users who break their streak in week 1. Once a user misses two days in a row, roughly 80% never return.

User research suggests why: users build a good streak, miss a day because "life happens," and return to find their counter reset to zero. This feels like punishment rather than a normal setback, and there's currently no way back in. Today, after a break, the app behaves as if nothing happened — same home screen, streak back at 0, no acknowledgment of the user's prior progress. The "you lost your streak" push notification reinforces this: its tone is harsh, and tapping it just drops the user back at day zero with nothing offered — a jarring experience.

There's an open question about whether the root cause is the streak reset mechanic itself, the timing/tone of notifications (nagging users right when they're most likely to quit), or both. The team's working view is that it's likely both, but the bigger issue is the lack of any graceful response *after* a streak break.

**Working hypothesis:** Users go passive because breaking a streak feels like failure, and there's no graceful comeback. Users need to be pulled back with something specific to their own progress — not a generic "keep going!" message.

### Evidence Summary

Three independent sources of customer data now corroborate the same problem, described purely in terms of what's happening and why — not what to do about it:

- **User interviews** ([interview-synthesis.md](../02-research/interview-synthesis.md)): The anxiety that precedes churn doesn't start at the moment of a break — it starts almost immediately (as early as day 4), well before the habit has had time to form (~3 weeks). The same streak mechanic that builds commitment once it survives intact (a long-term user's account) is the same mechanic that ends engagement the moment it breaks (a churned user's account) — and a new user already dreads that outcome before it's happened to her.
- **NPS feedback** ([nps-analysis.md](../02-research/nps-analysis.md)): 7 of 10 raw comments independently raised the same issue — the streak resets to zero and punishes a single miss (the most frequent theme, 4 mentions), users want some form of recovery (3 mentions), and for several users losing the streak ended their use of the app entirely (3 mentions). Notification frequency/tone was a secondary but real complaint (2 mentions), including one user who disabled notifications entirely.
- **Competitive scan** ([competitive-matrix.md](../02-research/competitive-matrix.md)): This isn't a problem the market has solved either. Across five comparable streak/habit apps (Duolingo, Babbel, Elevate, Habitica, Streaks), streak recovery is either locked behind a paid tier, absent entirely, or reframed as a social penalty — none treat pre-lapse anxiety or post-lapse recovery as a first-class part of the free experience.

## Goals

- Align the team on the problem before moving into solution design (this document's purpose, ahead of Thursday's meeting).
- Validate and explore the hypothesis that a graceful, personalized "comeback" moment — rather than a cold reset — will reduce passivity and churn after a streak break, specifically for new users who break their streak in week 1.
- **Workstream 1 — Notification tone:** drop the guilt-based framing; replace "you lost your streak" language with something more encouraging.
- **Workstream 2 — Easy comeback experience:** design an experience that pulls users back in after they've missed X days (threshold still to be defined). Candidate elements — best-streak stat, a 60-second comeback lesson, and a one-tap streak-freeze — are on the table but not finalized; final shape to be determined during discovery.

## Non-Goals

- Building new data sources or infrastructure — the Comeback screen concept is considered technically doable with existing data; the open work is the targeting logic (who sees it) and the streak-freeze rules, not new data collection.
- Committing to final designs or scope — this work is currently in discovery.
- Extending past the discovery window — this phase is scoped to 8 weeks from sprint kickoff.

## Success Metrics

- Day-7 retention (currently 39%, down from 48% pre-redesign) is the headline metric of concern. No specific recovery target was set in this discussion — see Open Questions.
- % of lapsed users who return within 48 hours — a proxy metric to gauge whether the comeback experience is working, in addition to the Day-7 headline number.

## Assumptions

- A UX-level fix (softer notification tone and/or a comeback experience) can meaningfully reduce the ~80% non-return rate — this is treated as a solvable experience problem, not primarily a disinterest/product-fit problem.
- Existing data/instrumentation is sufficient to define a "missed X days" trigger and to track 48-hour return rate, without new data infrastructure.
- The candidate comeback-screen elements (best-streak stat, 60-second lesson, one-tap streak-freeze) are technically feasible with current systems.

## Open Questions

- What is X — the number of missed days that should trigger the comeback experience?
- What logic determines who sees the comeback experience (beyond the day-trigger)?
- What are the specific rules for the one-tap streak-freeze (e.g., frequency, limits, eligibility)?
- What is the target Day-7 retention number or recovery goal we're aiming for?
