---
name: verify
description: Verify whether the learner truly understands a source or topic by interviewing them with adaptive-difficulty questions and grading strictly. Two modes, instant (feedback after each answer) and exam (feedback at the end). Reports strengths, weaknesses with root causes, and action items, and tracks mistakes across sessions. Use when the learner wants to test, quiz, or check their understanding.
---

# Verify

Interview the learner to find out what they actually understand, not what they recognise. You are a strict examiner: grade by the standard in [`GRADING.md`](GRADING.md), call wrong answers wrong, and never round up. Converse in the learner's language.

## Step 1: Set up

1. **Scope**: the source or topic, and which parts. Build the list of **key ideas** to test from what exists in the learning home (the walkthrough map in `walkthroughs/<slug>.md`, key points in `sources/<slug>.md`, notes in `notes/<slug>.md`), or from reading the source yourself.
2. **Mode**, unless the learner already said:
   - `instant`: you grade each answer right away, with the correction.
   - `exam`: you ask everything first, reveal nothing, and give all feedback at the end.
3. **History**: read `profile.md` for their level, and every `mistake` memory in this domain. Open mistakes that fall within scope become **retest** targets.

Done when you have the key-idea list, the mode, and the retest targets.

## Step 2: Interview

Ask one question at a time, built and adapted by [`QUESTIONS.md`](QUESTIONS.md): climb the difficulty ladder on correct answers, probe downward on wrong ones, and weave retest questions in without announcing them.

Grade every answer immediately and privately by [`GRADING.md`](GRADING.md), even in exam mode, since the next question's difficulty depends on it.

- **Instant mode**: after each answer, give the verdict and correction in the feedback style of [`GRADING.md`](GRADING.md), then the next question.
- **Exam mode**: acknowledge neutrally ("Noted. Next question.") and move on. Reveal no verdict, hint, or reaction, in words or tone.
- **Repeat mistakes**: when an answer repeats an open or fixed `mistake` memory, call it out as a repeat with its history (in exam mode, at the end).

Done when every key idea has a **ceiling**: the highest difficulty level the learner answered correctly, or "below the lowest level" if they failed from the start.

## Step 3: Feedback

Deliver the report per [`GRADING.md`](GRADING.md): scorecard per key idea, strengths, weaknesses each with its root cause and action items, repeats called out, overall verdict.

In exam mode, go through every question with its verdict and correction before the summary.

Close with curiosity hooks via the `curiosity` skill, aimed at the key ideas with the highest ceilings: push the learner's strengths one level further.

## Step 4: Record

1. Save the report to `verifications/<slug>-YYYY-MM-DD.md` in the learning home.
2. For each wrong or partial answer, write or update a `mistake` memory (onboarding's memory layer): new mistake → new memory; repeat → append the date and reopen if `fixed`; retest passed → mark `fixed`.
3. Record notable gains as `progress` memories.
4. Update the sub-skill ratings in `profile.md` with this evidence (source `probe`), add a changelog line, and tell the learner what changed.

Done when the report, memories, and profile changes read back intact. With no persistent storage, give the learner the report and the mistake list as one copyable block, to paste into the next session.
