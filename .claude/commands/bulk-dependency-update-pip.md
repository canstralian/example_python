---
name: bulk-dependency-update-pip
description: Workflow command scaffold for bulk-dependency-update-pip in example_python.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bulk-dependency-update-pip

Use this workflow when working on **bulk-dependency-update-pip** in `example_python`.

## Goal

Updates Python dependencies across multiple subproject requirements files (requirements.txt and pyproject.toml), typically via automated tooling like Dependabot.

## Common Files

- `**/requirements.txt`
- `**/pyproject.toml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify outdated dependencies across subprojects.
- Update dependency versions in requirements.txt and/or pyproject.toml files for each affected subproject.
- Commit all updated dependency files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.