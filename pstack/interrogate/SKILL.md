---
name: interrogate
description: "Use for \"interrogate\", \"adversarial review\", \"multi-model review\", \"challenge this\", \"stress test this code\", \"find blind spots\", or \"tear this apart\". Adversaries try to break a change or design, and only findings proven by a run survive."
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



# Interrogate

Adversaries try to break a change or a design. A finding survives only when a run proves it. Report the findings. Do not apply fixes.

## Frame

The scope is what the user names. Otherwise it is the branch diff from its merge base with the base branch, through the working tree. State the intent with the **in-your-own-words** skill, from the user's message, the commits, and the PR description. Ask the user when the intent is unclear.

## Fan out

Run Phase A steps 3 and 4 and Phase B of the **arena** skill, with four changes. Read the `interrogate reviewers` line in place of `arena runners`. Copy the scope's uncommitted changes into each worktree. Spawn each adversary as `generalPurpose`. In place of the arena task and rationale, give each adversary the scope, the intent, and this brief:

> Break this change. Prove each finding with a run against the real code, such as a failing test, a repro script, or command output that shows the wrong behavior. For a design or plan, run a prototype or probe the current tree. Keep repros in your own worktree. Report each finding with a title, the exact command, the output it printed, and the output the intent requires. Leave out anything you did not run. That covers style, naming, structure, and risks that need a future change to matter. No findings is a valid result.

## Verify

Verify each finding per arena Phase F by rerunning its command. Keep a finding when the output shows the failure and the failure breaks the intent. Drop the rest. Merge findings that share a root cause.

Skip arena Phases C, D, and E. Adversaries find different failures, so the verdict keeps every verified finding, not one adversary's list.

## Output

- **Intent**: the restatement.
- **Findings**: for each verified finding, the command, its output, how it breaks the intent, and the adversaries that found it. Say "no verified findings" when none survive.
- **Dropped**: for each adversary, the count of dropped findings and why.
