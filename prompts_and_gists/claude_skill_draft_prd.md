---
name: draft-prd
description: Generate a concise, executive-friendly PRD from a feature name or short brief. Use when starting a new feature, scoping a problem, or aligning stakeholders before build begins.
trigger: /draft-prd
arguments: true
---

Draft a concise, well-structured PRD for: $ARGUMENTS

Use this format exactly:

## Objective
One sentence. What are we shipping and why now?

## User Problem
What is the user experiencing today that makes this worth solving? Be specific about the pain, not the solution.

## Target User
Who is the primary user? Name the persona, role, or segment. One sentence.

## Jobs To Be Done
When [situation], I want to [motivation], so I can [expected outcome].
Write 2–3 JTBD statements.

## User Story
As a [user type], I want to [action] so that [outcome].
Write 1 primary story. Add 1–2 edge-case stories if relevant.

## Scope
### In Scope
- Bullet list of what this initiative covers.

### Out of Scope
- Explicit exclusions to prevent scope creep.

## Functional Requirements
List the specific behaviors the product must support. Use "must", "should", "must not" language. Group by user-facing vs. system behavior if helpful.

## UX / Experience Notes
Key constraints or principles for how this should feel. Not a design spec — just the non-negotiables and anything that could get lost in translation.

## Success Metrics
2–3 measurable KPIs. Format: Metric — target — timeframe.

## Risks / Edge Cases
What could go wrong? What assumptions are we making that might not hold?

## Open Questions
Unresolved decisions that need alignment before build starts.

---
Rules:
- No corporate filler. Write like a senior PM who respects the reader's time.
- Be specific. Vague requirements are not requirements.
- If $ARGUMENTS is thin, make reasonable assumptions and flag them in Open Questions.
- Keep total output under 600 words unless complexity demands more.
