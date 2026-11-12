# Show, then tell

Lead with a concrete representation: a diagram, input/output examples, a trace. Then name the rule it illustrates. Concrete first, abstraction second. This is the default for software and any technical topic, and works for most others (worked numbers in math, a timeline in history).

## Pick the representation by the shape of the idea

| The idea is about… | Show it as |
|--------------------|------------|
| A transformation: function, API, query, regex, pipeline, CLI command | **input → output examples**: a table of inputs and their outputs, or a before/after of the data |
| Step-by-step execution: loop, recursion, algorithm | **trace table**: one row per step, one column per variable; a call stack for recursion |
| Interactions over time: request lifecycle, protocol, auth flow | **sequence diagram** |
| Branching logic or a process | **flowchart** |
| States and transitions: lifecycle, UI state, connection state | **state diagram** |
| Structure and relationships: architecture, schema, class hierarchy | **box diagram**, ER diagram, or tree |
| Memory and data structures: pointers, references, linked structures | **box-and-pointer drawing** |
| Concurrency: race conditions, async ordering | **timeline with one lane per thread/task** |

## Input/output examples

Pick a small set that covers the idea:

1. A typical case.
2. An edge case: empty, zero, null, boundary.
3. A case that surprises: where intuition predicts wrong, which is often exactly what the learner is stuck on.

When code execution is `verified`, run the examples and show the real output. Never present output you haven't run as if it were run; label any hand-derived output as such.

## Diagrams

- Keep it small: about 7 nodes or fewer. Split a bigger picture into an overview plus a zoom-in.
- Label with the names the source uses, so the learner can map the diagram back onto the text.
- Render with the best tool available: Mermaid where the platform renders it, a rendered artifact or page when a rendering tool exists, ASCII in a plain terminal.

## Then tell

After the representation, state the rule in one or two sentences and point to where it appears in the example ("notice row 3: the counter resets because…").
