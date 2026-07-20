# Directing AI Effectively

## Session: 2026-07-10 — Lesson 08

**Core habit:** Before prompting AI to write code, write Context, Constraint, and Criterion first. Prompt only after all three are written.

**Framework: Context + Constraint + Criterion**
- **Context**: What system is this part of? What libraries, conventions, parent components?
- **Constraint**: What must the output NOT do? No new dependencies. Local state only. Follow existing patterns.
- **Criterion**: How will you know it's correct? The acceptance criteria from the spec — numbered, specific, verifiable.

**Key insight:** Most prompts only have Context. Adding Constraints and Criteria is the leverage that separates directed code from guessed code.

**Critical connection to Lesson 04:** The Criterion IS the spec's acceptance criteria, translated for an AI audience. The spec and the prompt are the same document for two different audiences.

**Worked example:** AlertFormModal prompt for MontyCloud:
- Context: MontyCloud, React + TypeScript, React Hook Form, Tailwind, existing component library
- Constraint: No new dependencies, local state only, follow src/features/billing/ structure
- Criterion: (5 numbered items from the spec's in-scope list)

**Verification step:** Walk through each Criterion item before committing. Most common failure: no loading state and no error state (these must be in the Criterion explicitly — AI won't invent them).

**What NOT to delegate to AI:** Architectural decisions — they require judgment about the system's history and future direction that can't be verified against a spec.

**Primary source:** Simon Willison — "What I've learned about AI-assisted development"

**ZPD for next:** Estimation as a Strategic Skill
