# Capability check

What a platform needs for effective self-study, how to probe each capability, and the template for `capabilities.md`.

Grade each capability by a live probe, never by a tool's name alone:

- `verified`: the probe returned a real, correct result.
- `failed`: a tool exists but the probe errored, timed out, or returned junk. Record the error.
- `missing`: no tool covers it.

## Capabilities

### Essential

| Capability | Why learning needs it | Probe |
|------------|-----------------------|-------|
| Web search | finding current, high-quality resources beyond training data | search for a well-regarded resource in the learner's domain; pass if it returns real, relevant URLs |
| Page fetch / crawl | reading the full content of a resource, not just a search snippet | fetch one URL from the search probe; pass if the main text comes back readable |
| Persistent storage | keeping the profile, notes, and progress across sessions | write a small test entry, read it back, then delete it; pass if the read matches |

### Recommended

| Capability | Why learning needs it | Probe |
|------------|-----------------------|-------|
| Code execution | running exercises, checking answers, building quizzes and spaced-repetition schedules | run a one-line computation; pass if output is correct |
| Rich output (artifacts, rendered pages) | interactive quizzes, flashcards, diagrams | confirm a rendering tool exists; no output needed yet |
| Scheduling / reminders | spaced repetition and study-session nudges | list existing schedules or calendar events (read-only) |
| Document reading (PDF, slides) | studying from books, papers, course material | only probe if the learner owns such resources |

### Domain-specific

Add rows the learner's domain calls for, for example: a code sandbox for programming, audio/TTS for language pronunciation, academic search (arXiv, Semantic Scholar) for research, video-transcript fetching for video-heavy domains. Mark them `missing` when no tool covers them; don't probe what isn't there.

## Storage priority for the learning home

Choose the first one available and `verified`:

1. **Local filesystem**: a dedicated folder, default `~/learning-home/`. Plain Markdown, readable by any tool and any future platform.
2. **Connected notes or docs app** (Notion, Google Drive, Claude Docs, and similar): one page or folder named `Learning home`.
3. **Platform memory** (project knowledge, memory features): store the profile there, note that its size and portability are limited.
4. **None**: hand the learner the profile as a copyable Markdown block (see Step 4 of the skill).

## Fixing a gap

Give the fix for the platform you're actually on, naming the setting or command you know exists (e.g. connectors or MCP servers, enabling a built-in web-search toggle). When unsure of the exact path on this platform, say so and describe the kind of tool to add rather than inventing menu names.

## `capabilities.md` template

```markdown
# Platform capabilities

Checked: YYYY-MM-DD · Platform: <name / client>

| Capability | Tier | Tool | Status | Notes / error |
|------------|------|------|--------|---------------|

## Gaps and fixes
| Gap | Learning impact | Fix |
|-----|-----------------|-----|

## Learning home
Location: <path or page link> · Storage type: <filesystem | notes app | platform memory | none>
Memory: default (`memory/` in the learning home) | learner's own source: <path, page link, or database> via <tool>
```
