# Building the map

## Rules

- **One key idea per step.** The test: the learner could state the step in one sentence afterwards. Two ideas → two steps; a fragment with no idea of its own → merge it into its neighbour.
- **5–9 steps per session.** A large source gets a two-level map: sections at the top, and one section zoomed into steps per session.
- **Order by dependency**, not by source order: an idea comes after the ideas it needs. Follow the source's order where it already respects this, so the learner can read along.
- **Skip what the learner knows**, judged from the profile, memories, and earlier walkthroughs. List each skipped idea with its reason; the learner can pull it back in.
- **Mark optional depth**: ideas that enrich but aren't needed for the goal become `optional` steps the learner can take or leave.
- **Pick the map's altitude from the learner's goal and level**: a novice aiming to use a tool gets "what it does and how to use it"; a proficient learner aiming to master it gets mechanisms and trade-offs.

## `walkthroughs/<slug>.md` template

```markdown
# Walkthrough: <source or topic>

Source: <link / path / "topic only: sources used"> · Started: YYYY-MM-DD
Status: in progress (step n) | paused at step n | done
Altitude: <one line: the level of detail chosen and why>

## Map
- [x] 1. <headline: the step's idea in one sentence>
- [ ] 2. <headline>
- [ ] 3. <headline> (optional)

## Skipped
- <idea> — <reason: already known / off-goal>

## Open questions
- <question> — step n

## Recap
<added at the end: each step's headline, plus anything learned in detours>
```
