---
name: release-notes
description: Transform recent git commits into a stakeholder-friendly Slack update. Use after a sprint, deployment, or meaningful batch of merged work.
trigger: /release-notes
arguments: false
disable-model-invocation: true
---

Here are the most recent commits from this repository:

```
!git log -n 10 --oneline --no-merges
```

And the full diff summary of what changed:

```
!git diff HEAD~5 --stat 2>/dev/null || git log -n 5 --format="%s%n%b"
```

Transform these commits into polished release notes formatted for a Slack update to stakeholders.

Use this structure:

**What shipped:**
- Plain English bullets. One line per meaningful change. No jargon.

**Why it matters:**
- One sentence connecting the work to user or business value.

**What's next:**
- One bullet on what follows logically from this release.

Rules:
- Merge commit messages like "Merge branch X" → skip entirely
- Chore/dependency bumps → group into one line: "Dependency updates and housekeeping"
- Keep it under 150 words total
- Write for a non-technical stakeholder audience
