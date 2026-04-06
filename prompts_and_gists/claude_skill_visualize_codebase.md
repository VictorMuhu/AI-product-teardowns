---
name: visualize-codebase
description: Generate a structured architecture brief for any codebase. Use when onboarding to a new repo, auditing structure before a refactor, or creating documentation for a technical audience.
trigger: /visualize-codebase
arguments: false
agent: explore
---

Analyze this repository and produce a structured architecture brief.

Read the following before writing anything:
- Root-level files (README, config files, package manifests)
- Top-level directory names and their contents
- Entry point files (index, main, app, server, cli)
- Any existing documentation or architecture notes
- Key source files that define the core data model or request flow

Then write the brief using this structure:

## High-Level Summary
2–3 sentences. What does this codebase do? Who uses it? What problem does it solve?

## Tech Stack
List languages, frameworks, runtimes, and key libraries. Note versions where relevant.

## Directory Map
| Directory | Purpose |
|-----------|---------|
| `dir/` | What lives here and why |

Cover every top-level directory. Be specific — "utilities" is not a purpose.

## Entry Points
Where does execution start? List the primary entry files and what triggers them (CLI, HTTP request, import, cron, etc.).

## Workflow / Request Flow
Describe the end-to-end path of a typical operation. Use plain prose or a numbered sequence. Make it concrete — pick the most common use case.

## Key Relationships
What depends on what? Note tight coupling, shared state, or modules that are load-bearing. Flag anything that would break other things if changed.

## Onboarding Guide
What does a new contributor need to know in the first 30 minutes? Include:
- How to run it locally
- Where to find the core logic
- What to read first
- Any non-obvious conventions or constraints

## Risks / Complexity Areas
What parts of the codebase are fragile, under-documented, or high-churn? What would a refactor need to account for?

## Open Questions
What is unclear from the code alone? What would require talking to a human to understand?

---
Rules:
- Be specific. File paths, function names, and module names are more useful than generalities.
- Distinguish between what the code does and what it appears to intend.
- If the repo has no code (e.g., docs-only or prompt library), adapt the brief accordingly — drop inapplicable sections and add relevant ones.
- Do not hallucinate structure. Only describe what you can observe.
