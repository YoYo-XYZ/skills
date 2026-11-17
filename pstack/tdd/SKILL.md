---
name: tdd
description: "Use only when the user explicitly asks for TDD, a failing test, or a regression test, OR when the bug has an obvious cheap local test target. Skip when the test path is unclear, expensive, integration-heavy, or not requested."
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



# TDD Bug Fix

When fixing a bug with a clear, cheap test path, make the broken behavior executable before changing production code. The goal is a focused regression test that fails before the fix and passes after it.

Do not force a test when it would be impractical. If the available test would require broad harness setup, brittle mocks, slow end-to-end infrastructure, production-only state, vague reproduction steps, or large unrelated fixture churn, skip adding a new test and use the closest useful verification instead.

## Workflow

1. **Understand the bug.** Identify the intended behavior, current behavior, affected path, and smallest observable reproduction.
2. **Choose the narrowest executable check.** Prefer the closest unit, component, integration, or regression test already used for that codepath. If no practical test path is obvious, do not create one from scratch just to satisfy the workflow.
3. **Write the failing test first.** Add the smallest focused test that would have caught the bug. The test should encode intended behavior, not mirror the current implementation.
4. **Run the new test before fixing.** Confirm it fails for the intended reason. If it passes or fails for an unrelated reason, correct the test or reproduction before editing the implementation.
5. **Fix the bug.** Make the smallest production change that satisfies the intended behavior while preserving nearby contracts.
6. **Rerun the regression test.** Confirm the test now passes.

## If a Failing Test Is Impractical

Use the closest executable regression check instead: a targeted script, manual reproduction command, browser automation, snapshot comparison, log assertion, or focused integration check.

Prefer no new test over a bad test. A bad test is one that mostly tests mocks, encodes current implementation details, depends on timing or unrelated global state, needs expensive infrastructure for a small fix, or would be deleted immediately after proving the fix.

## Guardrails

- Do not change tests merely to match a wrong implementation.
- Do not weaken existing assertions unless the expected behavior has genuinely changed and the reason is clear.
- Keep the regression test focused on the bug. Avoid broad fixture churn or unrelated coverage expansion.
- If the bug is flaky, make the test deterministic where possible and document the signal being locked down.
- If the bug exposes a broader class of failures, first land the focused regression path, then consider additional sibling coverage.

## Final Response

Report the evidence, not just the outcome:

- Name the failing-before test or executable check and the failure it produced.
- Name the passing-after test run and any nearby validation performed.
- If failing-before evidence could not be demonstrated, state why and describe the closest regression check used instead.
