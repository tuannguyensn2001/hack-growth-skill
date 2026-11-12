# Write-up

## Template (`notes/<slug>.md`)

Write in the learner's language; keep the headings in English, and the industry terms in their standard (usually English) form.

```markdown
# <Post title> — <company / author>

Link: <url> · Published: YYYY-MM-DD · Read: YYYY-MM-DD

## TL;DR in industry terms
<one paragraph, with zero in-house terms: problem pattern, solution pattern, result>

## Glossary
| Their term | Industry concept | Confidence | Difference |
|------------|------------------|------------|------------|

## The story
- Context:
- Problem: <symptom> → root cause: <cause>
- Constraints:
- Options considered:
- Solution:
- Results: <numbers, as claimed>

## Patterns
- Problem: <pattern> — <one line on how it showed up here>
- Solution: <pattern(s)> — <one line on their variant>
- Novel: <what has no standard equivalent, if anything>

## Before / after
<diagram, when the post describes a system change>

## Why it worked for them
## When it wouldn't apply
## Trade-offs and what's not said

## Takeaways for you
- <lesson tied to the learner's role, stack, or goals>

## Further reading
- <canonical source for each pattern: book chapter, paper, docs>
```

## Pattern index (`patterns.md`)

One entry per pattern, accumulated across every post the learner reads, so recurring patterns become visible:

```markdown
## <Pattern name> (<problem | solution>)
<one-line definition>
- [<post title>](notes/<slug>.md) — <company> · <one line on how it appeared>
```

Before adding a pattern, check for an existing entry and append the post under it.
