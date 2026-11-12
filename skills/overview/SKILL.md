---
name: overview
description: Triage a learning source (file or link) against the learner's profile. Judges whether to study it now, save it for later, or skip it; how deep it goes; how long it takes; what it requires first; what the learner gains. Use when the learner shares a resource and asks whether it is worth studying, or wants to triage a reading list.
---

# Overview

Produce a **verdict** on one source for this learner: `learn now`, `learn later`, `skim parts`, or `skip`, backed by what the source actually contains and by the learner's profile. Converse in the learner's language.

A verdict is only as good as what you read. Every report states its **coverage**: how much of the source you actually read.

## Step 1: Load the learner

Read from the learning home: `profile.md`, `memory/index.md` (and any memories relevant to this source's domain), `capabilities.md`.

No learning home found → offer to run the `onboarding` skill first. If the learner declines, ask the three questions the verdict needs most (goal, current level in this topic, weekly study time) and mark the report `profile: partial`.

Done when you know the learner's goals, their level in the source's domain, and their weekly time.

## Step 2: Read the source

Get the full content with the best tool available: read the file, fetch the page, pull the video transcript, open the repo README and structure.

- **Long sources** (books, multi-hour courses, large docs): read the table of contents, the introduction, one chapter from the middle, and the conclusion or final module. Sample more where the depth looks uneven.
- **Blocked** (paywall, login, fetch failed, no transcript): say what blocked you and ask the learner to paste or upload the content. Fall back to metadata (title, author, TOC, reviews) only if they can't, and lower your confidence.

Record coverage as `full`, `sampled (<which parts>)`, or `metadata only`.

Done when you have read enough to fill every source-side field of the rubric, or have recorded why a field can't be filled.

## Step 3: Judge the source on its own

Fill the source-side fields of [`RUBRIC.md`](RUBRIC.md): what it is, topics covered, depth, quality and credibility, currency, prerequisites, raw time cost. Judge it independently of this learner: a deep source is deep whoever reads it.

Back each judgement with a concrete pointer into the source (a section, a quote, an example it gives or skips).

Done when every source-side field holds a judgement with its pointer.

## Step 4: Judge the fit for this learner

Fill the fit fields of [`RUBRIC.md`](RUBRIC.md): goal relevance, level match, overlap with what they know, weaknesses it addresses, prerequisite gaps, constraint fit, personal time estimate.

Then decide the verdict by the rules in [`RUBRIC.md`](RUBRIC.md). For `skip` or `learn later` because of a level mismatch, search for one or two better-fitting alternatives when web search is available, and name them.

For `skim parts`, extract the key points from the sections worth it, per [`RUBRIC.md`](RUBRIC.md).

Done when the verdict follows from the fit fields, every prerequisite gap has a way to close it, and a `skim parts` verdict carries its key points.

## Step 5: Report and record

1. Present the report following [`REPORT.md`](REPORT.md), verdict first. For `learn now`, add 2–3 questions to keep in mind while studying it, via the `curiosity` skill.
2. Ask the learner for their decision; they may overrule you.
3. Save the report to `sources/<slug>.md` in the learning home and add or update its line in `sources/index.md`, with the learner's decision.
4. If the learner overruled the verdict for a reason that would change future triage ("I learn best from long courses even when slow"), write a `preference` memory per the onboarding skill's memory layer.

Done when the learner has decided and the report and index line read back intact. With no persistent storage, done when the learner has the report as one copyable Markdown block.

## Several sources at once

Run Steps 2–4 per source, then present a ranked table (verdict, fit, time) before the individual reports, and recommend one to start with.
