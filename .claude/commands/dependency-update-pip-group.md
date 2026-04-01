---
name: dependency-update-pip-group
description: Workflow command scaffold for dependency-update-pip-group in example_python.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update-pip-group

Use this workflow when working on **dependency-update-pip-group** in `example_python`.

## Goal

Batch updating Python dependencies (pip group) across multiple subproject directories, typically via automated tooling like Dependabot.

## Common Files

- `**/requirements.txt`
- `**/pyproject.toml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify outdated dependencies in multiple subproject directories.
- Update the relevant dependency versions in requirements.txt and/or pyproject.toml files.
- Commit all updated files in a single commit, often with a detailed changelog in the commit message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.