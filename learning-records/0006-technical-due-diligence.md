# Technical Due Diligence

## Session: 2026-07-10 — Lesson 06

**Core habit:** Before leaving any review comment, name which 3C it addresses. If you can't — reconsider whether the comment is worth making.

**Framework: The 3Cs**
- **Correctness** — bugs now (missing error states, race conditions, missing cleanup)
- **Clarity** — time debt (ambiguous names, missing context, confusing structure)
- **Changeability** — risk debt (tight coupling, magic numbers, untestable patterns)

**Key insight:** Junior developers check Correctness. Seniors check all three. Changeability failures are the most expensive — they compound silently over months and turn future features into rewrites.

**Worked example:** Applied 3Cs to AlertsPanel from Lesson 04 spec:
- Correctness: missing cleanup in useEffect, missing error state in AlertsList
- Clarity: `isModalOpen` → `isAlertFormOpen`; `ThresholdInput` → `SpendThresholdInput`
- Changeability: `window.confirm()` hardcoded = untestable, can't be replaced without rewriting logic

**What not to comment on:** Style preferences that can't be grounded in a 3C. Review signal is only as useful as it is objective.

**Primary source:** Google Engineering Practices — Code Review Guide

**ZPD for next:** Build vs. Buy vs. AI decision framework
