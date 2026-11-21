# [project name]

[project's purpose]

[project's state]

## Coding Principles

1. Keep the implementations simple and avoiding speculative features. Adding unnecessary flexibility early on creates permanent maintenance overhead once users depend on it.

2. Simplicity First. Minimum code that solves the problem. No speculative features, no single-use abstractions, no unrequested config. If 200 lines could be 50, rewrite to prioritize maintainability.

3. Surgical Changes
Touch only what you must. Don't improve adjacent code or refactor unrelated things. Match existing style. Remove only the dead code your changes create.

## Codebase Practice
- `[folder name]`: [purpose]
- [project specific rules]
- Do not write .md files unless explicitly asked
- Do not add `#` comments in source code or internal docstrings; keep user-facing API documentation concise.