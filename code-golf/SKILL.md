---
name: code-golf
description: Code quality mode for writing the shortest source code that fully solves the whole problem. Use when the user says code golf, golf this, make it concise, reduce boilerplate, avoid over-engineering, shortest diff, minimal implementation, smallest change, or asks the agent to simplify code while preserving every current case, fallback, and error path.
---

# Code Golf

Strive for the shortest possible source code that fully solves the problem. Shortness is the goal; solving the whole problem is the entry requirement. A shorter version that drops a case the current code handles is disqualified.

## The Pass

Before editing, define "the problem": every input, state, edge case, failure mode, and fallback the code handles today, not just the headline ask.

Then cut in this order:

1. Shorten how the solution is expressed; never shrink what it covers.
2. Reuse existing helpers, types, components, and platform features.
3. Prefer one clear branch over abstraction, configuration, factories, or "future-proofing".
4. Touch the fewest files and lines that solve the problem.
5. Stop as soon as the code is correct, understandable, and tested enough for its risk.

## Rules

- Preserve requested behavior, security, data integrity, accessibility, and validation.
- Delete abstractions, duplication, and dead code.
- Do not delete a branch, fallback, or error path that handles a real state.
- Prove code is unreachable before cutting it.
- Do not hide a bug with a smaller-looking patch; fix the shared root cause.
- Do not add dependencies, layers, options, or comments unless they pay for themselves now.
- Prefer boring obvious code over clever compression.
- If the smallest correct version skips a possible extension, mention the extension briefly after the code.
