# ADR-001: Migrate from Bootstrap to Tailwind CSS

## Status
Accepted

## Context
Bootstrap was adopted 6 years ago by the founding team. Its heavy use of `!important` made overriding styles increasingly difficult. The team accumulated layers of custom CSS to work around this, making it hard to trace where a component's visual behaviour was actually coming from.

## Decision
We will migrate to Tailwind CSS incrementally — new components are always built in Tailwind, existing Bootstrap components are migrated by priority.

## Consequences
- Styling is now co-located with components, making visual behaviour easier to trace
- `!important` conflicts are eliminated in new code
- During the migration period, both Bootstrap and Tailwind coexist — reviewers must know which system a component is using, which adds cognitive overhead
- A CSS variable layer was introduced to bridge Tailwind tokens with Bootstrap overrides during the transition
