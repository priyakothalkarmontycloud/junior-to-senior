# The Frontend Feature Spec

## Session: 2026-06-24 — Lesson 04

**Core habit introduced:** Before writing any code for a feature ticket, write a one-page spec in ~30 minutes. The spec surfaces ambiguity while it is still cheap to resolve.

**Five sections taught:**

1. **Why** — the business reason (1–2 sentences). If you can't state it, you shouldn't build it.
2. **What (scope)** — explicit in-scope and out-of-scope list. The out-of-scope list is as important as the in-scope list; it closes the door on scope creep.
3. **Component tree sketch** — hierarchy from Lesson 03. Shows structure and identifies whether existing components can be reused.
4. **State decisions** — applies the Lesson 03 ownership rule: state in the lowest common ancestor that needs it. Server state → React Query; component-local state → useState; contested cross-feature state → decide here.
5. **Open questions** — unknowns that must be resolved before or during the build. Each question has an owner and a deadline; ownerless questions don't get answered.

**Worked example:** Cost Alerts panel for MontyCloud billing dashboard. The spec surfaced a critical ambiguity — the ticket said "per account" but the data model only had user-level budgets — before any component was scaffolded.

**Connection to prior lessons:**
- Synthesises Lessons 01–03: scoping (01) + architectural thinking (02) + component design (03) into a single deliverable.
- State decisions in the spec are micro-ADRs. Full ADRs (Lesson 02) are only warranted when a decision is non-obvious, hard to reverse, or contested — not for routine applications of known rules.

**Primary source:** [Painless Functional Specifications — Joel Spolsky](https://www.joelonsoftware.com/2000/10/02/painless-functional-specifications-part-1-why-bother/) (4 parts)

**Zone of proximal development for next session:**
- **QA strategy for frontend** — what to test, what not to test, and how to decide. Directly addresses the mission success criterion: "running a QA strategy that tests the right things, not just the obvious things." Natural next step after the spec (specs define acceptance criteria; QA strategy defines how to verify them).
- **Technical due diligence** — reading and critiquing a component design you didn't write. Useful for code review leadership and onboarding.
