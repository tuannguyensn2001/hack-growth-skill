# Memory layer

The learner's own memory, kept where the learner chooses (by default in the learning home) and owned by this suite rather than by any one platform, so it survives switching tools. Every skill in the suite reads it at the start of a session and writes to it when it learns something durable.

## Profile vs memory

- `profile.md` is the **current state**: a curated summary, rewritten as things change.
- `memory/` is the **evidence trail**: dated observations, appended as they happen.

When memories pile up that contradict the profile (a weakness overcome, a level clearly higher), update the profile and cite the memories in its changelog.

## Location

The learner chooses during onboarding: a data source of their own, or the default, `memory/` inside the learning home. The choice is recorded in `capabilities.md`.

When the memory lives in the learner's own source, still create `memory/index.md` in the learning home holding a single pointer line, so every skill that opens it is redirected:

```markdown
Memory lives at: <path, page link, or database> (<tool used to reach it>)
```

Follow the pointer and apply everything below at that location.

## Layout

```
memory/
  index.md          one line per memory; the only file read every session
  <slug>.md         one memory per file
```

`index.md` line format:

```markdown
- [<title>](<slug>.md) — <type> · YYYY-MM-DD · <one-line hook>
```

Memory file format:

```markdown
---
type: insight | progress | preference | context | mistake
date: YYYY-MM-DD
domain: <domain name, or "general">
---

<the observation, with its evidence: what happened, in which session or exercise>
```

A `mistake` memory adds tracking fields to the frontmatter, so repeats can be counted:

```markdown
---
type: mistake
date: YYYY-MM-DD            # first seen
domain: <domain>
cause: misconception | common-pitfall | prerequisite-gap | recall-gap | shallow | careless
status: open | fixed
occurrences: [YYYY-MM-DD, YYYY-MM-DD]
---

<the wrong answer or belief, the correct one, and the action item given>
```

Mark a mistake `fixed` when the learner gets it right in a later session. If it recurs after that, set it back to `open` and append the date.

On a notes app, the folder becomes a `memory` page with one child page per memory. Where many files or pages are impractical (platform memory, copy-paste mode), keep a single `memory.md` holding the index lines, each followed by its body.

## Types

| Type | Records | Example |
|------|---------|---------|
| insight | how this learner learns: misconceptions, what clicks, recurring errors | "Confuses `let` scoping with closures; a timeline diagram fixed it." |
| progress | milestones and level changes, with evidence | "Passed 4/5 on recursion probe, up from 1/5 on 2026-10-01." |
| preference | corrections and confirmed approaches from the learner | "Wants the answer first, then the explanation." |
| context | life events that affect study | "Exam moved to 2027-01-15; can only study weekends in December." |
| mistake | a specific error caught in a verification, with its cause and repeat history | "Says `HashMap` lookup is always O(1); ignores collisions. Seen twice." |

## Writing rules

- Write a memory when an observation would change how a future session teaches. Leave out what only mattered in the moment.
- Before writing, check `index.md` for an existing memory on the same point and update it rather than adding a duplicate.
- Delete memories that turned out wrong.
- Use absolute dates.
