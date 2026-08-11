---
name: documentation-update-dual-language
description: Workflow command scaffold for documentation-update-dual-language in Telegraph-Image.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /documentation-update-dual-language

Use this workflow when working on **documentation-update-dual-language** in `Telegraph-Image`.

## Goal

Keeps both English and Chinese READMEs in sync with new features, usage instructions, and changelogs.

## Common Files

- `README.md`
- `README-zh.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit README.md to add or update documentation
- Edit README-zh.md to mirror changes in Chinese
- Ensure both files are in sync in terms of structure and content

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.