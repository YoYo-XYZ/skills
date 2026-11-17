---
name: architect
description: "Sketch types, signatures, and module structure before code, then stay in the loop while implementation fills in. Use for /architect, 'architect this', 'design this', or non-trivial work where jumping to code would lock in the wrong shape."
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



# Architect

Before writing code, trace every system the change touches, then sketch two different shapes for it (types, signatures, module boundaries) and pick the one where each piece of state has one owner, each task has one way to do it, and callers need to know least. Redesign instead of patching if workarounds repeat.

For a large or contested design, run the **arena** skill instead of sketching alone.
