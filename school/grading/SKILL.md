---
name: grading
description: Grade an assignment or draft against the grading criteria in its repository. Use when asked to mark an assignment, estimate its score out of 10, or prioritize revisions using the rubric.
---

# Grade an assignment

## Find the submission and rubric

Locate the submission and its grading criteria in the assignment repository. Include the assignment brief when it clarifies the rubric. If the submission or rubric is missing or ambiguous, ask the user to identify it.

## Run three independent reviews

Run three subagents in parallel, one GPT Luna, one GPT Terra, and one GPT Sol, each with "medium" reasoning. Collect all three reviews before reporting.

## Shared reviewer prompt

```markdown
Act as the teacher grading this assignment.

- First, read any lecture slides in the project. Use them to establish what the course taught and what the teacher expects students to know.

- Grade the submission using the stated criteria and weights. Cite specific evidence for each criterion. Convert the rubric total to a score out of 10, or explain how you arrived at the score if the rubric gives no points. Keep the review read-only.

### Score

Give the score as X/10 and a brief breakdown by criterion.

### P0

List the changes that would recover the most rubric points.

Use 1–2 sentences per recommendation. Name the concrete change and the criterion it addresses.

### P1

List the next most valuable changes.

Use 1–2 sentences per recommendation. Name the concrete change and the criterion it addresses.
```

## Report the grades

Use only these Markdown sections, in order. Keep your report very concise, be direct, and avoid fluff

- `### Scores`. Use one table row per reviewer with columns for reviewer, score out of 10, and rubric breakdown.
- `### P0` and `### P1`. Combine overlapping recommendations. Use one bullet per change and name the rubric criterion it addresses in a single no fluff sentences.
