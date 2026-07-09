# The Frontend QA Strategy

## Session: 2026-07-09 — Lesson 05

**Core habit introduced:** Before writing tests, map your spec's acceptance criteria to a test list in plain English. This separates "what should I test?" (strategic) from "how do I write it?" (tactical).

**Mental model introduced:** The Testing Trophy (Kent C. Dodds)

- **Static analysis** — TypeScript + ESLint. Free, always on.
- **Unit tests** — isolated functions/hooks. Worth it only for complex pure logic.
- **Integration tests** — the sweet spot. Render component trees, fire user events, assert visible output.
- **E2E tests** — real browser + server. Reserve for critical paths (login, billing).

**The one-sentence test:** "Does this test give me confidence the feature works for users?" If no, don't write it.

**Key rule:** Test behavior, not implementation. Query by role, label, and visible text — never by CSS class names or internal component state. Implementation details change; behavior doesn't.

**Spec → tests pipeline:** From Lesson 04's Cost Alerts spec:
- "Set a threshold via the form" → frontend integration test
- "Email sent when spend exceeds threshold" → NOT a frontend test (backend behavior)
- "Enable, edit, disable alerts" → three frontend integration tests

**What to skip:** third-party library internals, trivial pass-throughs, CSS class names, static text.

**Primary sources:**
- [Write tests. Not too many. Mostly integration. — Kent C. Dodds](https://kentcdodds.com/blog/write-tests)
- [Testing Implementation Details — Kent C. Dodds](https://kentcdodds.com/blog/testing-implementation-details)

**Zone of proximal development for next session:**
- **Technical Due Diligence** — reading and critiquing a component design you didn't write. This is the skill behind code review leadership and onboarding. Natural next step: after spec + QA strategy, you can now evaluate whether someone else's spec or component design is sound.
- **Build vs. Buy vs. AI** — strategic decision-making for new features/tooling. Directly addresses the mission success criterion: "Making build-vs-buy-vs-AI decisions confidently and with written justification."
