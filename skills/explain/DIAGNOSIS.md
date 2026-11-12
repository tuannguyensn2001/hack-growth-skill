# Diagnosis

Each cause, how to recognise it, and the strategy that cures it.

## Unfamiliar concept

The idea itself is new or rarely met: jargon, a niche term, a notation the learner hasn't seen.

**Signals**: the learner stops at one term or symbol; the rest of the sentence is fine once it's defined; the term isn't defined in the source or was defined long ago.

**Strategy**:
1. Plain-words definition, one sentence.
2. The problem it exists to solve: why anyone needed this idea.
3. One concrete example and one non-example (something close that isn't it).
4. An anchor to something the learner already knows, from their background or another domain.
5. Back to the passage.

## Convoluted writing

The idea is within reach, but the source expresses it badly: long tangled sentences, ambiguous pronouns, inconsistent terms, buried point, or an outright error.

**Signals**: you have to re-read it too; the same idea elsewhere is clear; terms shift meaning mid-passage.

**Strategy**:
1. Rewrite the passage in plain language, sentence by sentence where it helps the learner map one onto the other.
2. Name what made it hard ("'it' in sentence 3 refers to the cache, not the request"), so the learner can parse the next such passage alone.
3. If the source is wrong, say so plainly and show the evidence: a counterexample, a run of the code, or an authoritative source found by search.

## Missing context

The source assumes something it never provides: a skipped derivation step, a reference to an earlier chapter or another paper, an unstated assumption, an unexplained setup.

**Signals**: a jump the learner can't bridge ("therefore…" with no visible reason); references to things outside the passage; a step obvious only to an expert.

**Strategy**:
1. Supply the missing piece directly: the skipped step, the assumption, the background. Fetch the referenced material when it's reachable.
2. Show where it slots into the passage's chain of reasoning.
3. If the gap is large, note what the source assumes so the learner expects more of it.

## Prerequisite gap

The passage is fine; the learner lacks foundational knowledge it rightly builds on.

**Signals**: the learner's teach-back breaks below the passage's level; the quick prerequisite check fails; several terms are unfamiliar, not one; the profile shows a level below the source's intended reader.

**Strategy**:
1. Trace the minimal prerequisite chain: the fewest concepts needed to understand this passage, not the whole foundation.
2. If the chain is short, teach just enough of it, just in time, then return to the passage.
3. If it's long, say so honestly, recommend pausing this source, and name a specific resource to close the gap. Suggest re-running the `overview` skill on the source if its verdict looks wrong now.

## Misconception

The learner holds a wrong mental model that the passage collides with. Often feels like "this makes no sense" rather than "I don't know".

**Signals**: the teach-back is confident but wrong; the learner's objection rests on a false premise; an `insight` memory records a related misconception.

**Strategy**:
1. Surface the learner's model explicitly ("It sounds like you're picturing X as…").
2. Show where it breaks: a counterexample, a prediction that fails, a run of the code.
3. Replace it with the correct model, then show why the old one seemed right (it usually holds in a narrower case).
