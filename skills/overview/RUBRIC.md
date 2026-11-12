# Overview rubric

## Source-side fields

Judged on the source alone, each with a pointer into the source.

| Field | What to record |
|-------|----------------|
| Type and format | article, book, course, video, paper, docs, repo; length (words, pages, minutes, modules) |
| Topics covered | the main concepts, in the order the source teaches them |
| Depth | a level from the depth scale below |
| Quality and credibility | author's standing, whether claims are backed, errors spotted, original vs aggregated |
| Currency | publish/update date; whether the field has moved on since (deprecated APIs, superseded research) |
| Prerequisites | concepts and skills the source assumes without teaching |
| Raw time cost | estimate for an average reader at the intended level (method below) |

### Depth scale

| Level | The source… | Signals |
|-------|-------------|---------|
| Surface | names things and lists them | listicles, "top 10", no examples, no why |
| Introductory | explains concepts with simple examples | definitions plus toy examples, happy path only |
| Working | gives enough to apply it to real problems | worked examples, exercises, common pitfalls |
| Deep | explains mechanisms, trade-offs, and failure modes | the *why*, derivations or internals, edge cases, when not to use it |
| Reference | covers the topic exhaustively, for lookup | complete API or spec coverage, little narrative |

Depth can be uneven: record it per section when chapters differ ("ch. 1–3 introductory, ch. 4–6 deep").

### Time estimate method

- Text: study pace 100–200 words/min for technical material, 200–300 for narrative; halve the pace for dense math or code.
- Video: duration × 1.5–2 for pausing, notes, and rewatching.
- Exercises and projects: estimate each separately; they often outweigh the reading.
- Give a range (low–high), never a single number.

## Fit fields

Judged against the learner's profile and memory.

| Field | What to record |
|-------|----------------|
| Goal relevance | which near-term goal or north star it serves, and how directly; or none |
| Level match | too easy, in the stretch zone, or too hard, compared to the learner's Dreyfus level in the source's sub-skills |
| Overlap | what share of it the learner already knows |
| Weaknesses addressed | profile weaknesses or `insight` memories it targets |
| Prerequisite gaps | each prerequisite the learner lacks, with how to close it (a specific short resource or exercise) |
| Constraint fit | time against weekly hours and deadlines, budget, format against preferences |
| Personal time estimate | raw time adjusted for this learner (× 1.5–2 if a level below the intended reader, less where overlap is high), converted to calendar weeks at their weekly hours |
| Gains | concrete abilities after finishing ("can design a normalized schema"), not topics |

## Verdict rules

| Verdict | When |
|---------|------|
| `learn now` | serves a near-term goal, sits in the stretch zone, prerequisites met or closable within a few hours, fits current time |
| `learn later` | worth it, but blocked now by prerequisite gaps, a higher-priority goal, or no time before a hard date. Name the **trigger** that makes it `learn now` ("after finishing SQL basics", "after the 2027-01 exam") |
| `skim parts` | most of it is overlap or off-goal, but specific sections earn their time. Name the sections and extract the **key points** (below) |
| `skip` | off-goal, too shallow for the learner's level, outdated, or low quality, or a clearly better alternative exists. Say which reason |

### Key points (for `skim parts`)

The skim itself, done for the learner, so the report alone delivers most of the source's value to them:

- **Key points**: each idea the learner doesn't already know, stated in one or two sentences as the takeaway itself ("Indexes slow down writes; index only columns you filter on"), never as a topic name ("Indexes"). Each with its location in the source.
- **Watch out**: gotchas, counter-intuitive claims, claims to verify, outdated parts.

Skip points the profile shows the learner already knows. Done when every section named as worth it has yielded its points.

Confidence: `high` with full coverage and a complete profile; lower it for sampled or metadata-only coverage or a partial profile, and say why.
