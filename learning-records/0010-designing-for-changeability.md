# Designing for Changeability

## Session: 2026-07-10 — Lesson 10

**Core habit:** Before finalizing a component design, ask: "Can I replace [the thing most likely to change] without touching [the things that should stay stable]?" If no — add a seam.

**Framework: Seams + Single Responsibility**

- **Seam** (Michael Feathers): a place where behavior can change without editing surrounding code. In React: props, callbacks, custom hooks, wrapper components.
- **Single responsibility**: one reason to change means changes are localized — only that module changes when its reason occurs.

**The changeability test:** "Can I swap X for Y without touching Z?" A no answer = Changeability failure (from Lesson 06 3Cs).

**Key insight:** Seams are cheap insurance. You don't need to know in advance what will change. If you never swap the library, the seam cost you almost nothing. If you do, it saves a week.

**Worked example:** CostTrendPanel with charting seam:

- Tightly coupled: CostTrendPanel uses Recharts directly → 12-file D3 migration
- With seam: CostTrendPanel owns data + normalisation; CostTrendChart owns Recharts → 1-file D3 migration
- Seam mechanism: neutral interface `{x: string, y: number}[]` is independent of any library

**Connections to prior lessons:**

- Spec (Lesson 04): surfaces which components are volatile (open questions = likely change points)
- ADRs (Lesson 02): documents changeability decisions ("we isolated the charting library behind CostTrendChart")
- 3Cs review (Lesson 06): Changeability failures show up as the third C — and are the most expensive

**Terminology clarification (added 2026-07-25):** "Seam" is Feathers' term, not a React-specific one — it predates components entirely and just means "a place you can alter behavior without editing surrounding code" (a callback, a config flag, a virtual method — any language). It's distinct from **compound components** (the `<Tabs><Tabs.List/></Tabs>` pattern), which is a narrower React pattern for flexible parent/child composition via shared context, not primarily about swapping implementations. In conversation with people who haven't read Feathers, the more universally understood equivalent is **"abstraction boundary."** Keep "seam" for precise personal notes; use "abstraction boundary" in ADRs/team discussion.

**This lesson closes the first arc:** Spec → ADR → Component Design → Feature Spec → QA Strategy → Due Diligence → Build/Buy/AI → AI Directing → Estimation → Changeability. All ten lessons are tools for managing change safely.

**Primary sources:**

- "Working Effectively with Legacy Code" — Michael Feathers (seam concept)
- "A Philosophy of Software Design" — John Ousterhout (modules and information hiding)

**ZPD for next arc:** System design at scale; leading architectural discussions; technical strategy documents
