---
name: onboarding
description: Onboard a self-learner. Builds their learner profile (domain, level, strengths, weaknesses, goals, constraints, preferences) and audits whether this platform has the tools to learn effectively (web search, page fetching, persistent storage). Use when a learner starts self-study, when no learner profile exists yet, or when their goals, level, or domain have changed.
---

# Onboarding

Three outputs, all saved in the learner's **learning home** (the one place every skill in this suite reads from and writes to):

- `profile.md`: who the learner is, following [`PROFILE-SCHEMA.md`](PROFILE-SCHEMA.md).
- `capabilities.md`: what this platform can and cannot do for learning, following [`CAPABILITY-CHECK.md`](CAPABILITY-CHECK.md).
- `memory/`: the learner's own memory layer, following [`MEMORY-LAYER.md`](MEMORY-LAYER.md).

Converse in the learner's language. Write profile content in their language too; keep the schema headings in English so other skills can parse them.

## Step 1: Inventory and look for an existing profile

Read [`CAPABILITY-CHECK.md`](CAPABILITY-CHECK.md) and map the tools in your context onto its categories. Inventory only; live probes come in Step 3.

Then look for an existing learning home: a `profile.md` in the storage you found (filesystem, connected notes app, platform memory), or a profile the learner pasted.

- **Profile found** → update mode. Read `memory/index.md` too and fold in any memories the profile doesn't reflect yet. Show the learner a short summary, ask what has changed, and run Step 2 only on the sections that changed or are marked `unknown`. Append a changelog entry.
- **No profile** → full intake.

Done when every capability category has a candidate tool or is marked missing, and you know which mode you are in.

## Step 2: Intake interview

Fill every section of [`PROFILE-SCHEMA.md`](PROFILE-SCHEMA.md) through conversation.

- Ask 1–3 questions per turn, offering example answers or options so replying costs little.
- Chase vague answers to something concrete. "Get better at English" becomes: which skill, for what situation, by when, measured how.
- Rate level on the Dreyfus scale (novice, advanced beginner, competent, proficient, expert) per sub-skill, never per whole domain. Base each rating on **evidence**: things the learner has built, done, passed, or can explain. A self-rating is a claim, so ask for the evidence behind it.
- When the claimed level is shaky or evidence is thin, offer a **calibration probe**: 3–5 short questions or a mini-task pitched at the claimed level. Grade it, show the learner the result, adjust the rating. The learner may skip; record the rating as `self-reported`.
- Ask for only the personal data learning needs. A name or nickname is optional.
- If the learner wants to go fast, cover goals, domain, and level first, and mark the rest `unknown` for a later session.

Done when every schema field holds an answer, an evidence-backed rating, or an explicit `unknown` with the reason (declined, unsure, deferred).

## Step 3: Live capability probes

Run the probes in [`CAPABILITY-CHECK.md`](CAPABILITY-CHECK.md), using the learner's domain as the test subject so the probes double as first useful results (e.g. search for a well-regarded resource in their domain, then fetch it).

Done when every category is graded `verified`, `failed`, or `missing`.

## Step 4: Playback and save

1. Play the profile back as a compact summary: goals, levels with evidence, top strengths and weaknesses, constraints. Ask the learner to correct anything. Repeat until they confirm it.
2. Pick the learning home by the storage priority in [`CAPABILITY-CHECK.md`](CAPABILITY-CHECK.md). Propose a location and let the learner override it.
3. Write `profile.md` and `capabilities.md`.
4. Ask the learner where their memory should live: a data source of their own (a Notion workspace, Google Drive, an Obsidian vault, a specific folder, a database) or the default, `memory/` inside the learning home. For their own source, check that a tool here can reach it and run the storage probe from [`CAPABILITY-CHECK.md`](CAPABILITY-CHECK.md) on it. If it fails or no tool reaches it, tell them what is missing (e.g. the connector to add), and use the default until it's fixed. Record the choice in `capabilities.md`.
5. Create the memory per [`MEMORY-LAYER.md`](MEMORY-LAYER.md) at that location and seed it with what the intake surfaced that the profile only summarises: calibration-probe results (`progress`), past attempts and why they stalled (`insight`), stated feedback preferences (`preference`), hard dates (`context`).
6. Read everything back to confirm it saved.

Done when the learner has confirmed the profile and the profile, capabilities, and memory index all read back intact. With no persistent storage, done when the learner has received the full profile as one copyable Markdown block, with the instruction to paste it at the start of each learning session.

## Step 5: Report

End with:

- A short profile summary (3–5 lines).
- The capability table from `capabilities.md`. For each gap, state its learning impact and the fix for this platform.
- Where the learning home and the memory live.
- One suggested next step toward the learner's nearest goal.
