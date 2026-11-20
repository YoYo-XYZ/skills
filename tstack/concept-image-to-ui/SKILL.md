---
name: concept-image-to-ui
description: Analyze an attached concept image and implement the matching UI in the project.
---

# Concept Image to UI

Translate a supplied visual reference into a working, maintainable UI in the current repository. Treat the image as the source of visual intent while treating the codebase as the source of architectural and product constraints.

## Analyze the reference

Extract only what affects implementation:

- Layout, alignment, spacing, and responsive behavior.
- Visual tokens: colors, typography, borders, radii, blur, shadows, and icons.
- Component hierarchy, reusable patterns, navigation, actions, and interaction states.

Reproduce the reference through actual UI components, not a screenshot or background image. For ambiguous details, use the simplest behavior consistent with the existing product.

## Implement

- Make visible controls functional and preserve basic accessibility and responsive behavior.
- Reuse existing assets and dependencies; avoid unnecessary one-off CSS or abstractions


## Verify and iterate

- Do not run relevant lint, typecheck, tests, and build checks.
- Do not compare the implementation against the reference image at target and narrow viewports, then fix meaningful visual or interaction mismatches.