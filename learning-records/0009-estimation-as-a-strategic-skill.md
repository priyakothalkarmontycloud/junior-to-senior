# Estimation as a Strategic Skill

## Session: 2026-07-10 — Lesson 09

**Core habit:** Always provide a three-part estimate (best/expected/worst) with written assumptions. Never give a single number without context.

**The planning fallacy (Kahneman):** Humans plan the best case and call it expected. The fix is reference class forecasting — "what did similar tasks actually take?" not "how long do I imagine this will take?"

**Framework: Three-part estimate + assumptions**
- **Best case**: Everything goes right — API exists, no design changes, no interruptions
- **Expected**: Based on reference class, adjusted for known differences
- **Worst case**: The most likely assumption breaks
- **Assumptions**: The conditions that, if they break, invalidate the estimate

**Key insight:** The spec's open questions (Lesson 04, section 5) become the estimate's worst-case triggers. They're the same list viewed from a different angle.

**What gap separates junior and senior estimates:** Not coding speed — the full delivery cycle. Code review wait (~1 day), revisions, testing, QA, deploy, monitoring. All invisible to gut feel; all visible in reference classes.

**Worked example:** Cost Alerts feature from Lesson 04:
- Reference class: account preferences panel took 3 days; this adds React Query (new work)
- Best: 2 days (API exists, design final), Expected: 4 days, Worst: 7 days (API not ready)
- Assumptions: /api/alerts exists by day 1; no design changes; no P0 interruptions

**The range is the information:** Sharing 2–7 days instead of just 4 opens the conversation about what would need to be true to hit the best case.

**Primary source:** "Software Estimation: Demystifying the Black Art" — Steve McConnell

**ZPD for next:** Designing for Changeability — seams and single responsibility
