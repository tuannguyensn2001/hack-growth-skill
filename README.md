# hack-growth

A suite of agent skills for self-study. The agent gets to know the learner, then helps them decide what to study, study it, understand it, prove they understand it, and stay curious, while remembering everything across sessions.

The skills are platform-agnostic: they adapt to whatever tools the platform offers (web search, page fetching, storage) and degrade gracefully when one is missing.

## Skills

| Skill | Use when the learner… |
|-------|-----------------------|
| [`onboarding`](skills/onboarding/SKILL.md) | starts out, or their goals, level, or domain changed. Builds the profile and audits platform tools |
| [`overview`](skills/overview/SKILL.md) | has a source (file or link) and asks: is it worth studying, now or later, how deep, how long? |
| [`walkthrough`](skills/walkthrough/SKILL.md) | wants to be taught a source or topic one key idea at a time |
| [`explain`](skills/explain/SKILL.md) | is stuck on a passage, term, formula, or code snippet |
| [`engineering-blog`](skills/engineering-blog/SKILL.md) | reads an engineering blog post and wants it in industry-standard terms, with transferable lessons |
| [`verify`](skills/verify/SKILL.md) | wants to be tested, strictly, on whether they really understood |
| [`curiosity`](skills/curiosity/SKILL.md) | asks what's interesting or what to explore next. Also fired by the other skills at natural pauses |

A typical path: `onboarding` → `overview` on a source → `walkthrough` it (with `explain` on demand) → `verify`, with `curiosity` hooks along the way.

## How the skills connect

```
onboarding ──creates──▶ learning home ◀──reads/writes── every other skill

overview ──"learn now"──▶ walkthrough ──question──▶ explain
                              │                        │
                              └────────▶ verify ◀──────┘
                                           │
   curiosity ◀── called at the end of overview, explain, walkthrough,
                 engineering-blog, verify
```

Cross-skill references (the skills name each other and `walkthrough` reuses `skills/explain/SHOW.md`) assume the whole suite is installed together.

## Learning home

The one place, owned by the learner rather than any platform, where every skill reads and writes. `onboarding` picks its location (default `~/learning-home/`; a notes app or platform memory when there's no filesystem).

`<slug>` is a kebab-case name derived from the source's title, shared across folders, so everything about one source lines up by name.

| Path | Holds | Defined by |
|------|-------|------------|
| `profile.md` | who the learner is: goals, levels with evidence, strengths, weaknesses, constraints, preferences | [`onboarding/PROFILE-SCHEMA.md`](skills/onboarding/PROFILE-SCHEMA.md) |
| `capabilities.md` | what this platform can do for learning, and the gaps | [`onboarding/CAPABILITY-CHECK.md`](skills/onboarding/CAPABILITY-CHECK.md) |
| `memory/` | dated observations: insights, progress, preferences, context, mistakes | [`onboarding/MEMORY-LAYER.md`](skills/onboarding/MEMORY-LAYER.md) |
| `sources/` | triage reports, plus `index.md` as the reading list with decisions | [`overview/REPORT.md`](skills/overview/REPORT.md) |
| `walkthroughs/<slug>.md` | the step map, progress, and recap of each walkthrough | [`walkthrough/MAP.md`](skills/walkthrough/MAP.md) |
| `notes/<slug>.md` | explanations and engineering-blog write-ups, per source | [`explain/SKILL.md`](skills/explain/SKILL.md), [`engineering-blog/WRITEUP.md`](skills/engineering-blog/WRITEUP.md) |
| `patterns.md` | industry patterns, with every blog post they appeared in | [`engineering-blog/WRITEUP.md`](skills/engineering-blog/WRITEUP.md) |
| `verifications/<slug>-YYYY-MM-DD.md` | verification reports | [`verify/GRADING.md`](skills/verify/GRADING.md) |
| `curiosity.md` | hooks offered, which were taken up, the unexplored backlog | [`curiosity/SKILL.md`](skills/curiosity/SKILL.md) |

Each format is defined once, in the file named in the last column. Change it there.

## Install

### Claude Code (plugin)

This repo is both a plugin and its own marketplace. In Claude Code:

```
/plugin install hack-growth --marketplace tuannguyensn2001/hack-growth-skill
```

On Claude Code older than 2.1.275, add the marketplace first, then install:

```
/plugin marketplace add tuannguyensn2001/hack-growth-skill
/plugin install hack-growth@hack-growth
```

Update later with `/plugin marketplace update hack-growth`. Then start with `/onboarding`.

### Manual (Claude Code or any agent that reads `SKILL.md` folders)

```
git clone https://github.com/tuannguyensn2001/hack-growth-skill
cp -r hack-growth-skill/skills/* ~/.claude/skills/
```

For other agents, copy `skills/*` into that agent's skills directory instead.

### Claude.ai / Claude Desktop

Zip each folder under `skills/` separately (the zip holds the folder, with `SKILL.md` inside) and upload each one as a custom skill in the app's skills settings. Upload all seven: the skills call each other.

## Releasing a new version

Bump `version` in `.claude-plugin/plugin.json` on every release; installed copies update only when the version changes.
