---
name: engineering-blog
description: Break down an engineering blog post (from a company or an engineer) into industry-standard concepts. Translates the author's in-house terms and system names into common patterns, retells the story (problem, constraints, solution, results), and extracts transferable lessons and when they don't apply. Use when the learner reads an engineering blog, postmortem, or tech talk write-up and wants to understand it or learn from it.
---

# Engineering blog

An engineering blog tells one team's story in that team's language: internal system names, home-grown terms, their scale, their constraints. The learner wants what **transfers**. Your job is to **translate** the post into the industry's shared vocabulary, so the lesson outlives the post. Converse in the learner's language.

## Step 1: Load the learner and read the post

- From the learning home: `profile.md` (their role, stack, level, goals), `memory/index.md` and relevant memories, `patterns.md` if it exists.
- Read the post fully. When it builds on earlier posts in a series or a talk it references, and the story doesn't make sense without them, read those too.

Done when you can retell the post's story without looking back at it.

## Step 2: Extract the story and the jargon

1. Lay out the **story arc**: context → problem (symptom, then root cause) → constraints → options considered → solution → results → lessons the authors claim.
2. List every **in-house term**: internal system and service names, coined terms, home-grown metrics, team names used as concepts.

Done when every arc stage is filled from the post or marked "not stated", and every in-house term is listed.

## Step 3: Translate

Map the post onto industry vocabulary per [`TRANSLATE.md`](TRANSLATE.md):

- each in-house term → the standard concept it is an instance of;
- the problem → its canonical **problem pattern**; the solution → its **solution pattern(s)**.

When something has no standard equivalent, say so: a genuinely novel idea is often the real insight of the post.

Done when every in-house term and both the problem and solution carry a translation or an explicit "novel", each with a confidence level.

## Step 4: Judge what transfers

- **Why it worked for them**: the scale, constraints, and context that made this the right call.
- **When it wouldn't apply**: the conditions under which a reader should choose differently.
- **Trade-offs and omissions**: costs they accepted, alternatives they dismissed too quickly, what a postmortem or a competitor's post would add. Engineering blogs are partly recruiting and marketing; read them the way a reviewer would.
- **Takeaways for this learner**: tie the lessons to their role, stack, and goals in `profile.md`. Pitch to their level: for a novice, name the patterns and offer the `explain` skill on any that are new; for a proficient learner, focus on what is novel or debatable.

Done when every lesson the authors claim has been judged as transferable, conditional, or specific to them.

## Step 5: Present and record

1. Present the write-up following [`WRITEUP.md`](WRITEUP.md), translated TL;DR first. Include a before/after diagram of the architecture or flow when the post describes a system change.
2. Offer curiosity hooks via the `curiosity` skill (a "where in your own system would this pattern show up?" reflection fits here), then next moves: walk through it step by step (`walkthrough` skill) or explain a pattern (`explain` skill).
3. Save the write-up to `notes/<slug>.md` in the learning home, and add each pattern to `patterns.md` per [`WRITEUP.md`](WRITEUP.md).
4. Write a memory (onboarding's memory layer) when the post reveals something durable about the learner: a pattern they met for the first time and grasped (`progress`), a gap in their systems knowledge (`insight`).

Done when the write-up and pattern index read back intact. With no persistent storage, give the write-up as one copyable block.
