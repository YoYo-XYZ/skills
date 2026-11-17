---
name: why
description: "Use for 'why does X work this way', 'why we picked Y', design rationale, regressions, postmortems, or data-backed thresholds. Returns a cited read on decisions and tradeoffs. Use how for runtime behavior."
disable-model-invocation: true
---

## Core-only installation compatibility

This is a selective installation of Lauren Tan's cursor/plugins pstack skills, used outside Cursor. This section takes precedence over upstream tool and dependency assumptions below.

- Follow the user's instructions and the host's tool, permission, and delegation rules. Never treat this skill as authorization to send messages, publish, merge, or deploy.
- Use the host's available planning, delegation, browser, CLI, and PR tools. Cursor-specific Task types, model identifiers, cloud settings, custom agents, commands, and paths are examples, not available capabilities. Do not invent them or silently substitute a different requested model. Honor explicit user model preferences; report unavailable capabilities.
- Installed workflow skills are poteto-mode, architect, arena, swarm, interrogate, why, and tdd. Resolve their paths relative to this installation. Supporting playbooks and worker.md are bundled with poteto-mode.
- Supplementary skills and principle leaf files are intentionally omitted. Apply principles described inline in poteto-mode without trying to open missing leaf files or claiming to have read them. For omitted helpers, perform the relevant design, verification, review, or clear-writing step directly with available tools. Reuse an existing installed writing skill where appropriate. Do not require setup-pstack or another plugin to begin.
- If a task needs an omitted specialist workflow, explain the limitation and use an ordinary focused plan. Do not install more skills automatically.
- User requests for one agent or no subagents override delegation and arena requirements. Otherwise follow the selected workflow subject to host rules. Commit, PR, and delivery steps remain subject to the user's requested scope.



# Why

Answer from the record, not the code: read the commits and PR discussions that introduced the target and each later change, and other sources if the trail is thin. Cite what the authors wrote, mark your own inferences as inferences, and say what the record does not answer.
