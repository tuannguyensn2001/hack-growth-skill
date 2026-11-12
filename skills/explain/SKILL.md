---
name: explain
description: Explain a point the learner is stuck on while studying a source. Diagnoses why it is confusing (unfamiliar concept, convoluted writing, missing context, prerequisite gap, misconception) before explaining, then checks understanding. Use when the learner is stuck on a passage, term, formula, diagram, or code snippet.
---

# Explain

**Diagnose before you explain.** The same confusion has different cures: a missing definition, a rewrite of bad prose, a skipped step, a prerequisite, or a wrong mental model to dismantle. An explanation aimed at the wrong cause is wasted. Converse in the learner's language.

## Step 1: Gather the passage and the learner

- Get the exact passage the learner is stuck on, plus the text around it: what comes before (what the source thinks it already established) and after (what it's building toward). If the learner only names the topic, ask for the passage or locate it in the source yourself.
- Read from the learning home: `profile.md` (level, background, preferred formats), `memory/index.md` and the memories relevant to this domain (past misconceptions, explanations that clicked), and `sources/<slug>.md` if this source was triaged.

No learning home → explain anyway; skip the profile-dependent choices and ask the learner's level in one question.

Done when you have the passage, its surroundings, and the learner's level in this topic.

## Step 2: Diagnose

Classify the confusion using the causes and signals in [`DIAGNOSIS.md`](DIAGNOSIS.md). More than one cause can apply; name each.

Read the passage yourself first: convoluted writing and missing context often show in the text alone. When the text doesn't settle it, ask the learner one targeted question:

- "Which word or sentence is the point where you lose it?"
- "In your own words, what do you think it's saying?" (a **teach-back**: their answer exposes gaps and misconceptions directly)
- One quick prerequisite check, when a gap is suspected.

Done when you can name the cause and point to the evidence for it (a phrase in the passage, a gap in the learner's answer). Tell the learner the diagnosis in one sentence before explaining ("The source skips the step where…", "This relies on X, which we haven't covered…").

## Step 3: Explain

Apply the strategy for each diagnosed cause in [`DIAGNOSIS.md`](DIAGNOSIS.md).

- **Show, then tell**: open with a concrete representation (a diagram, input/output examples, a trace table) and state the rule after it. Pick the representation by the shape of the idea, per [`SHOW.md`](SHOW.md). For software and technical topics, this is the default.
- Pitch at one step above the learner's level. Build analogies from their background and domains in `profile.md`, and lean toward the formats it lists as working for them.
- Start short. Offer more depth rather than front-loading it.
- End by reconnecting to the passage: re-read it with the learner, showing how it now parses.

## Step 4: Check understanding

Ask one **check question** that requires using the idea, not recognising it: predict an outcome, apply it to a new case, spot the error, or explain it back. "Does that make sense?" is not a check.

- Correct → done. Offer one curiosity hook on the idea just understood, via the `curiosity` skill.
- Wrong or shaky → re-diagnose from their answer (it is new evidence) and explain again with a different strategy. After two failed rounds, suspect a deeper prerequisite gap and check for it.

Done when the learner answers a check question correctly, or chooses to move on (record that the point is still open).

## Step 5: Record

1. Append the explanation to `notes/<slug>.md` in the learning home:

   ```markdown
   ## <short title> — YYYY-MM-DD
   Passage: <location in source, short quote>
   Diagnosis: <cause(s)>
   Explanation: <the core of the explanation that worked, in a few lines>
   Check: <the question and whether it was answered>  <!-- or "open" -->
   ```

2. Write a memory (onboarding's memory layer) when the episode reveals something durable: a misconception or prerequisite gap (`insight`), an explanation style that clicked or failed (`insight`), the learner closing a gap (`progress`).
3. If the diagnosis was convoluted writing or missing context, note it in `sources/<slug>.md` under "Why not / risks", so the source's report stays honest.

Done when the note is saved and read back. With no persistent storage, skip recording and say so.
