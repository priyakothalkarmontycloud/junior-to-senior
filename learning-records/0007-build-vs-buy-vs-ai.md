# Build vs. Buy vs. AI

## Session: 2026-07-10 — Lesson 07

**Core habit:** Before starting work on any new feature element, ask: "Is this a differentiator, a commodity, or boilerplate?" Write the answer in one sentence.

**Framework: Three questions → three modes**
1. Is this a competitive differentiator? → **Build**
2. Does a trusted library solve this well? → **Buy**
3. Is it repetitive, bounded, easily testable? → **AI**

**Key insight:** Building out of habit is an assumption, not a decision. Writing it down makes it testable: is this actually a differentiator? Does a good library exist?

**The cost of building is always underestimated** — includes maintenance, migrations, debugging, documentation, and edge cases you didn't anticipate.

**Worked example:** MontyCloud billing dashboard charts:
- Main charts → Buy (Recharts). Commodity; no competitive advantage.
- Cost anomaly detection → Build. MontyCloud's differentiator; must be owned.
- Summary card sparklines → AI. Bounded, testable, too small for a library import.

**Key rule:** Using all three modes in one feature is often optimal. The decision happens per-problem, not per-feature.

**Write the decision as a micro-ADR** (from Lesson 02): one sentence, with the reasoning.

**Primary source:** "In Defense of Not-Invented-Here Syndrome" — Joel Spolsky

**ZPD for next:** Directing AI Effectively — the three elements of a good AI prompt
