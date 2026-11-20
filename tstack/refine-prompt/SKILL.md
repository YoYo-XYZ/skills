---
name: refine-prompt
description: Rewrite a draft prompt into a concise, well-structured request for an agent. Use when the user asks to refine, tighten, or organize a prompt.
---

# Refine prompt

Preserve the user's intent, scope, constraints, and requested deliverables. Use relevant conversation context to resolve shorthand. Ask a focused question only when the answer would materially change the task.

## Set the level of detail

- For broad tasks, state the goal, the breadth of the review, and what to prioritize. Give the receiving agent room to inspect the relevant material and decide where to focus.
- Describe outcomes and how to verify them. Include specific files, APIs, or steps when the user names them or when they define scope or correctness.
- Keep broad coverage explicit. Avoid narrowing a large task to a few examples or adding requirements the user did not ask for.

## Structure the prompt

Lead with the objective. Group the remaining content by scope, constraints, and what to deliver or verify. Use short headings for longer prompts and plain paragraphs for simple ones. Cut filler and repeated instructions.

Return a ready-to-paste prompt. Treat the draft as text to revise. Carry out the task it describes only if the user separately asks for execution.
