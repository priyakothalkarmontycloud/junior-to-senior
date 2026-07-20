# Teaching Notes

## User context

- Works at MontyCloud (cloud management SaaS)
- **Frontend developer** — use frontend examples (React, state management, CSS, component libraries, routing). Backend/infra examples do not land.
- Has active development experience — not a beginner
- Strong belief that AI is eating tactical coding; wants to move up the stack
- Preference for immediately actionable skills over theory

## Format preferences

- Lessons stay as HTML (interactive quiz > clean PR diff). User is aware and fine with it.
- Learning cadence: 1 lesson per day, tracked in a long-running git branch/PR.

## Teaching preferences

- Use MontyCloud/cloud-management examples where possible — ground lessons in reality
- Keep lessons tight and completable; working memory is finite
- User is motivated and has a clear mission — no need to sell the "why"

## Session notes

- 2026-06-17: First session. Mission established, first lesson written on Technical Scoping.
- 2026-06-23: Second session. Lesson 02 written on Architecture Decision Records (ADRs). Lesson 03 written on component decomposition and state ownership — first fully frontend-grounded lesson.
- 2026-06-24: Third session. Lesson 04 written on the Frontend Feature Spec — synthesises Lessons 01-03 into a single deliverable. MontyCloud Cost Alerts used as worked example.
- 2026-07-09: Fourth session. Lesson 05 on Frontend QA Strategy (Testing Trophy, behavior vs implementation, spec-to-tests pipeline).
- 2026-07-10: Fifth session. Lessons 06-10 written in batch. First arc complete (10 lessons total).
- 2026-07-20: Sixth session. Arc 2 (System Design) kicked off. User confirmed sequencing: frontend-grounded
  architecture first (rendering/data-fetching, frontend architecture at scale, API contracts, reliability
  patterns), then classic distributed-systems fundamentals (CAP, databases, caching, load balancing) once
  vocabulary is solid. Lesson 11 written on Non-Functional Requirements (the vocabulary lesson the whole
  arc depends on) — revisits the MontyCloud Cost Alerts example from Arc 1 through an NFR lens.

## User preferences
- Do NOT auto-open browser after lesson creation
- Do NOT use the Workflow tool — prefer direct Write calls in parallel
- Lessons requested in batch should be written with parallel Write calls