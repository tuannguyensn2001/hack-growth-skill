# Grading and feedback

## Strict grading

| Grade | When |
|-------|------|
| `correct` | right answer **and** right reasoning, precise enough that you'd accept it from a colleague |
| `partial` | right direction but missing a part the idea depends on, or right buzzwords without the mechanism |
| `wrong` | wrong answer, **or** right answer reached by wrong reasoning |
| `don't know` | the learner says so. Better than a bluff: say so, and grade it as a gap, not a mistake |

- Vagueness is not understanding. An answer that could be read as right or wrong is `partial` at best.
- Grade what was said, not what the learner probably meant.
- No credit for effort or for being close.

## Feedback style

Blunt and specific, in this order:

1. **Verdict first**, one word: "Wrong." / "Partial." / "Correct."
2. **What exactly was wrong**: quote the part of their answer that fails.
3. **The correct answer**, with the reasoning.
4. **Root cause** (below), one line.

Praise only what was genuinely strong, and say specifically what was strong about it.

**Repeats** are called out hard, with the record: "This is the third time: 2026-10-03, 2026-10-20, today. You still treat X as Y. This is the gap to fix before anything else." Firm and direct about the mistake; never about the person.

## Root causes and action items

Classify every `wrong` or `partial` answer:

| Cause | Signals | Action items |
|-------|---------|--------------|
| `misconception` | confident and consistently wrong; a wrong model of how it works | dismantle the model: counterexample, then the correct model (`explain` skill); retest next session |
| `common-pitfall` | the error most people make here; the source or field is counter-intuitive | name the pitfall and its trap; drill 2–3 cases where it bites |
| `prerequisite-gap` | fails the probe on the concept beneath | study the specific lower concept first (name a resource), then come back |
| `recall-gap` | understands when reminded, couldn't produce it | spaced review: flashcards or re-test in 2–3 days |
| `shallow` | can define it, can't apply it | practice problems at the apply level; build something small with it |
| `careless` | knew it (shows elsewhere), slipped here | slow down on this question type; re-read the question before answering |

Every action item names something concrete: a section to re-read, a resource, an exercise, a date to retest.

## Report template (`verifications/<slug>-YYYY-MM-DD.md`)

```markdown
# Verification: <source or topic> — YYYY-MM-DD

Mode: instant | exam · Questions: n · Overall: understood | partial | not yet

## Scorecard
| Key idea | Ceiling (Bloom) | Result |
|----------|-----------------|--------|

## Strengths
- <specific strength, with the question that showed it>

## Weaknesses
| Weakness | Cause | Why | Action items |
|----------|-------|-----|--------------|

## Repeat mistakes
- <mistake> — seen: <dates> — status: still open | now fixed

## Questions and answers
<exam mode: every question, the learner's answer, verdict, correction>
```

Overall: `understood` when every key idea reaches level 3 or higher; `not yet` when any key idea sits below level 2; `partial` otherwise.
