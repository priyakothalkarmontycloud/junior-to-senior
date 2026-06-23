# ADRs: Decisions Have Context That Code Cannot Capture

## Session: 2026-06-23 — Lesson 02

**Core insight acquired:** Code shows *what* was built; ADRs show *why*. Without the why, future engineers reverse-engineer intent from implementation — slowly, and often wrongly.

**Key lessons:**

1. ADRs are immutable history — even superseded decisions are preserved in the record. Understanding the sequence of reasoning matters as much as the final state.

2. The four required fields are: Title (imperative), Status, Context (the world that made the decision necessary), Decision (one active sentence), Consequences (benefits *and* trade-offs accepted). Consequences that list only upsides are either obvious or dishonest.

3. Status vocabulary: Proposed → Accepted → Deprecated (no replacement yet) or Superseded by ADR-XXX (replaced by a later decision).

4. The threshold for writing one: meaningful alternatives existed, trade-offs are non-obvious, decision affects multiple engineers, and/or it's hard to reverse.

5. Timing matters: write the ADR when the decision is made, not later. Context is clearest at the decision point.

**Grounding example used:** MontyCloud choosing AWS SQS over Celery+Redis for async task dispatch — a real architectural fork with legitimate trade-offs on both sides (operational simplicity vs. local dev friction, payload limits).

**Zone of proximal development for next session:**
- Technical Scoping (Lesson 01) + ADRs (Lesson 02) establishes the *document before you build* reflex.
- Natural next step: **System Design vocabulary** — understanding the design decisions that most commonly need ADRs (data models, API contracts, consistency trade-offs, decomposition boundaries). Or: **running an architectural discussion** — how to facilitate and document a team decision rather than making it alone.
