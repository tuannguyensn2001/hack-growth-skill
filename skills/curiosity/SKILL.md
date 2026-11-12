---
name: curiosity
description: Spark the learner's curiosity about what they're studying with a few sharp hooks (interview questions, open "why"s, what-ifs, connections, experiments to try, follow-ups worth reading). Use when the learner asks what's interesting, what to think about, or what to explore next, and at natural pauses in other learning skills (end of a walkthrough section, after an explanation, after a write-up or a verification).
---

# Curiosity

Curiosity comes from an **information gap**: a question the learner can see, just beyond what they know, that they want closed. Your job is to open such gaps, not to fill them. Pose hooks as questions and hold back the answers until the learner reaches for them. Converse in the learner's language.

## Step 1: Find the material's edges

Look at what the learner just studied (the current step, passage, post, or source) and at `profile.md` (goals, north star, background), `patterns.md`, and `curiosity.md` in the learning home, which records the kinds of hooks this learner takes up.

Look for the places where a good question lives: what the source asserts without justifying, what would break under a different constraint, where it connects to something the learner already knows, where experts disagree, what interviewers love to ask about it.

## Step 2: Pick 2–4 hooks

Choose from the hook types below, weighted toward the learner's goals (interview prep → more `interview`; building things → more `try it`) and toward the types `curiosity.md` shows they take up.

| Type | Hook | Example |
|------|------|---------|
| `interview` | a question commonly asked in interviews on this topic | "Why can't you just add more replicas to fix write throughput?" |
| `why` | a design decision the source states but doesn't justify | "Why does TCP need a 3-way handshake, not 2?" |
| `what if` | change one constraint and ask what breaks | "What if the cache had no TTL at all?" |
| `connection` | a link to something the learner knows, another domain, or a pattern in `patterns.md` | "This is the same idea as the outbox pattern you saw in the Shopify post. Where's the difference?" |
| `debate` | where practitioners genuinely disagree | "Monorepo or polyrepo at 50 engineers?" |
| `try it` | a small experiment that answers a question by running it | "Run `EXPLAIN` on this query with and without the index; predict the plan first." |
| `follow-up` | one specific resource that goes deeper on the most interesting edge | "The original Dynamo paper, section 4, is where consistent hashing gets its virtual nodes." |

Every hook must be:

- **Specific to this material.** "Learn more about databases" is not a hook.
- **At the edge**: one step beyond what the learner knows, answerable with effort.
- **A question or an invitation, unanswered.** The answer is what the learner earns by reaching for it.

Done when you have 2–4 hooks that each pass all three tests.

## Step 3: Offer them

Present the hooks compactly, each tagged with its type, at a natural pause; never mid-explanation:

```
Worth wondering:
- [interview] …
- [what if] …
- [try it] …
```

When the learner picks one:

- a question → let them try it first; then discuss, or hand off to `explain` (if they're stuck) or `verify` (if they want it graded);
- a `follow-up` resource → offer the `overview` skill on it;
- a `try it` → run the experiment with them when code execution is available.

## Step 4: Record

Append to `curiosity.md` in the learning home:

```markdown
## YYYY-MM-DD — <topic / source>
- [type] <hook> — taken up | ignored
```

When a pattern shows across sessions (always takes `interview` hooks, never `debate`), write a `preference` memory (onboarding's memory layer) so future hooks lean that way. Hooks the learner left unexplored stay in `curiosity.md` as a backlog they can return to.
