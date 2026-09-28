# Streakly Comeback Experience — Strategy

*Status: Draft, discovery phase. Companion to [project.md](project.md).*

## Hypothesis

Day-7 retention has dropped 9 points, from 48% to 39%, since the v2 streak/notification redesign. The working hypothesis is that the streak mechanic that drives the habit loop is also what's punishing users when it breaks: the counter resets to zero with no acknowledgment and no path back in. Roughly 80% of users who miss two days never return. We believe this is a solvable experience problem — not a sign that users have lost interest in the product — and that fixing how the app responds to a lapse can recover a meaningful share of that 9-point drop.

## Approach

Three workstreams, running in parallel during discovery:

- **Notification tone:** Drop the guilt-based framing in lapse notifications. Replace "you lost your streak" language with something more encouraging.
- **Easy comeback experience (reactive):** Design an experience that pulls users back in after they've missed X days (threshold still to be defined). Candidate elements — a best-streak stat, a 60-second comeback lesson, and a one-tap streak-freeze — are on the table but not finalized; the final shape will come out of discovery.
- **Week-1 anxiety reduction (proactive):** User interviews (see [interview-synthesis.md](../02-research/interview-synthesis.md)) found that streak-loss anxiety starts as early as day 4 — well before the habit forms (~3 weeks) — meaning churn risk exists before a user ever breaks a streak. This workstream addresses that pressure directly in the first week, before any lapse, rather than only softening the landing after one.

All three workstreams are scoped to use existing data and systems — no new infrastructure is assumed to be needed.

## What Success Looks Like

- Recovery of Day-7 retention toward the pre-redesign baseline (48%), though no specific target has been set yet.
- An improvement in the % of lapsed users who return within 48 hours, as a proxy signal that the comeback experience is working.

## Open Threshold

The number of missed days (X) that should trigger the comeback experience is still undefined — this is the key open question discovery needs to resolve before design can be finalized.
