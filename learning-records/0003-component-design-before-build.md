# Component Design: Sketch the Tree Before You Write the Code

## Session: 2026-06-23 — Lesson 03

**Core habit introduced:** Before writing any component, sketch the hierarchy and label who owns which state. The sketch surfaces structure and ownership decisions while they are cheap to change.

**Two skills taught:**

1. **Component decomposition** — break UI into a hierarchy based on single responsibility. Each component does one thing. If it does two, split it.

2. **State ownership** — state lives in the lowest common ancestor of all components that need it. Three categories:
   - Only one component needs it → local (`useState`)
   - A few nearby components need it → lift to their common parent, pass as props
   - Many unrelated components need it, or it's server data → global store or React Query/SWR

**Worked example:** Filter bar + resource list on a cloud dashboard. Filter state lives in `DashboardPage` (not `FilterBar`) because `ResourceList` also needs it.

**Common mistake covered:** Jumping to global state (Zustand/Redux) for state that only two adjacent components need. Global state has a cost — use it only when prop drilling would span many unrelated layers.

**Connection to prior lessons:** Sketching the component tree surfaces forks (decisions between two reasonable approaches) — those forks are where ADRs (Lesson 02) belong.

**Primary source:** [Thinking in React — React Docs](https://react.dev/learn/thinking-in-react)

**Zone of proximal development for next session:**
- The next natural step is either:
  - **Reading a component design you didn't write** — how to navigate and critique an unfamiliar codebase (the strategic skill of technical due diligence)
  - **Writing a technical spec for a frontend feature** — applying Lesson 01 (scoping) in frontend terms: component tree + state plan + open questions, before a single line of code
  - **QA strategy for frontend** — what to test, what not to test, and how to decide (from the mission: "testing the right things, not just the obvious things")
