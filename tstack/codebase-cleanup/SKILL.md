---
name: codebase-cleanup
description: Perform aggressive codebase cleanup when asked to remove dead, obsolete, redundant, and low-value code while preserving builds and core functionality.
---

Perform an aggressive codebase cleanup focused on eliminating dead, obsolete, redundant, and low-value code without compromising sound software engineering practices.. Do not use agent skills.

Delete unused files, components, functions, classes, variables, imports, dependencies, routes, assets, legacy implementations, abandoned abstractions, duplicate utilities, unreachable branches, stale compatibility code, and unnecessary wrappers.

Prefer deletion and simplification over preserving questionable code. If removing dead code requires small surgical changes to nearby code, imports, interfaces, or call sites, make those changes as well.

Do not preserve code merely because it might be useful later. Keep only code that has a clear current purpose.

After cleanup, fix resulting references and ensure the project still builds and core functionality remains intact.
