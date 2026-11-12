---
name: walkthrough
description: Guide the learner through a source or topic one key idea at a time, teaching each step and pausing for questions before moving on. Use when the learner wants to study something together with the agent, be walked through a source, or resume a walkthrough in progress.
---

# Walkthrough

Teach a source or topic as a sequence of **steps**, one key idea each, at the right **altitude**: high enough to stay short, low enough to carry the idea whole. The learner sets the pace: they ask whenever something is unclear, otherwise you keep going. Converse in the learner's language.

## Step 1: Load the learner and the material

- From the learning home: `profile.md`, `memory/index.md` and relevant memories, `sources/<slug>.md` (the overview report, if triaged), `notes/<slug>.md`, and `walkthroughs/<slug>.md` if one exists.
- **Walkthrough in progress** → resume. Recap where you stopped in two or three lines (the headlines of the last steps, any open questions), then continue from the next step.
- **Source given** → read it fully, as in the `overview` skill's reading step.
- **Topic only, no source** → teach from 1–3 authoritative sources found by search, or from your own knowledge if search is unavailable. Tell the learner which.

Done when you have the material read and know where to start.

## Step 2: Build the map

Build the outline of steps per [`MAP.md`](MAP.md) and show it to the learner before teaching: numbered step headlines, what you're skipping and why, estimated time. They may reorder, skip, or narrow the scope.

Save it as `walkthroughs/<slug>.md`.

Done when every key idea in the chosen scope maps to a step or is listed as skipped with a reason, and the learner has accepted the map.

## Step 3: Teach, step by step

Deliver each step in the shape set by [`STEP.md`](STEP.md), then stop and wait. Move to the next step when the learner says go.

When the learner interrupts:

- **A question about this step** → answer it the way the `explain` skill does: diagnose why it's unclear, explain, check. Keep the detour scoped, then say "Back to step n" and continue.
- **A question about a later step** → give a one-line answer, say which step covers it, and continue.
- **"Go deeper"** → zoom one altitude down on this step, then return to the map's altitude.
- **"Faster" / "slower"** → raise or lower the altitude for the rest of the walkthrough.

Every 2–3 steps, or at the end of a section, ask one **check question** that requires using the ideas just covered. Keep it to one question; momentum matters more here than exhaustive testing. The learner may skip it.

After each step, tick it off in `walkthroughs/<slug>.md` and update the current position.

Done when every step on the map is taught or the learner stops; a stop leaves the position saved for resuming.

## Step 4: Wrap up

1. **Recap**: the map again, each step reduced to its one-sentence headline. This is the summary of what they learned.
2. Open questions still unresolved.
3. One suggested next move: practice, the next chapter, or a source that goes deeper.
4. Curiosity hooks on the whole walkthrough, via the `curiosity` skill. Also offer a hook or two at the end of each section during Step 3, never mid-step.

## Step 5: Record

1. Mark the walkthrough `done` (or `paused at step n`) in `walkthroughs/<slug>.md` and add the recap.
2. Append each detour explanation to `notes/<slug>.md` in the `explain` skill's note format.
3. Write memories (onboarding's memory layer) for what would change future teaching: a preferred altitude or pace (`preference`), a misconception or gap uncovered (`insight`), check questions answered well across a section (`progress`).

Done when the walkthrough file and notes read back intact. With no persistent storage, give the learner the map with ticks and the recap as one copyable block.
