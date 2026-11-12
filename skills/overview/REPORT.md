# Overview report

## Report template (`sources/<slug>.md`)

Write in the learner's language; keep the headings in English.

```markdown
# <Source title>

Link / file: <url or path> · Reviewed: YYYY-MM-DD
Coverage: full | sampled (<which parts>) | metadata only · Profile: complete | partial

## Verdict
**<learn now | learn later | skim parts | skip>** · Confidence: <high | medium | low>
<two or three sentences: the decisive reasons, tied to the learner's goals and level>
Trigger to revisit: <for learn later only>
Sections worth it: <for skim parts only>

## Key points
<!-- skim parts only -->
- <takeaway> — <location in source>

### Watch out
- <gotcha, claim to verify, outdated part> — <location>

## What you gain
- <concrete ability>

## Why not / risks
- <reasons against, gaps, outdated parts; "none significant" if so>

## Before you start
| Prerequisite | Your status | How to close it |
|--------------|-------------|-----------------|

## Time
Raw: <range> · For you: <range> ≈ <weeks> at <hours>/week

## The source
- Type and format:
- Topics:
- Depth: <level, per section if uneven>
- Quality and credibility:
- Currency:

## Alternatives
<only when suggested>

## Decision
Learner decided: <learn now | learn later | skim parts | skip> on YYYY-MM-DD
```

## Index line format (`sources/index.md`)

One line per source, newest first:

```markdown
- [<title>](<slug>.md) — <learner's decision> · <depth> · <time for learner> · YYYY-MM-DD
```

For `learn later`, append the trigger: `· after: <trigger>`.
