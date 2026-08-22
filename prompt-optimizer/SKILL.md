---
name: prompt-optimizer
description: Rewrite vague prompts or requirements into compact, executable specifications using precise domain terminology and EARS when useful. Use when the user asks to optimize, improve, tighten, or clarify a prompt or requirement.
---

# Prompt Optimizer

Return a copy-ready prompt, not an explanation of the optimization.

## Rewrite

1. Keep the user's intent and language. Extract the goal, explicit constraints, and one verifiable completion criterion.
2. Replace vague wording with the smallest correct term of art when it changes execution. Prefer precise domain language over lists of generic expertise.
3. Preserve identifiers and requested output fields, but do not broaden the scope or enumerate implied sub-requirements.
4. Use EARS only when an event, state, or condition needs testable wording.
5. If one missing choice materially changes the result, ask one question before rewriting; otherwise leave it open or label it unknown.
6. Remove duplication, generic model capabilities, process narration, examples, and instructions that do not change behavior.

## Length

- Treat 100–300 Chinese characters, or equivalent compactness in the user's language, as the default hard budget.
- Use one paragraph or at most three compact lines. Represent related restrictions with an umbrella term instead of an exhaustive prohibition list.
- If the original is already actionable, make a light edit rather than expanding it.
- Exceed the budget only when the user explicitly asks for a detailed, complete, step-by-step, or field-by-field prompt. Task complexity alone is not permission to expand.
- In default mode, omit headings, workflows, checklists, examples, and deliverable inventories. Do not impose `Role/Skills/Workflows/Examples/Formats`.

## Grounding

- Preserve relevant identifiers, paths, commands, standards, and domain terminology.
- Apply a domain theory only when it yields a concrete requirement or decision rule; do not cite theories merely for credibility.
- Do not invent repository facts, technology choices, thresholds, dates, metrics, or examples. Mark a necessary proposed default as an assumption.

## Output

- Output only the optimized prompt unless the user requests analysis or alternatives.
- Do not include “Original Requirement,” issue analysis, theory lists, or usage notes.
- Preserve any output format the user explicitly requested.

## References

Read only when the branch requires it:

- Event/state/conditional requirements → [references/ears_syntax.md](references/ears_syntax.md)
- A domain framework would change a decision rule → [references/domain_theories.md](references/domain_theories.md)
- Multi-stakeholder, non-functional, or nested logic requested in detail → [references/advanced_techniques.md](references/advanced_techniques.md)
- The user asks for examples → [references/examples.md](references/examples.md)
