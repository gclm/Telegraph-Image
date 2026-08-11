---
name: feature-development-with-tests-and-docs
description: Workflow command scaffold for feature-development-with-tests-and-docs in Telegraph-Image.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-development-with-tests-and-docs

Use this workflow when working on **feature-development-with-tests-and-docs** in `Telegraph-Image`.

## Goal

Implements a new feature or enhancement, including backend logic, updates to the admin UI, test coverage, and documentation.

## Common Files

- `functions/*.js`
- `functions/*/*.js`
- `functions/utils/*.js`
- `admin.html`
- `admin-imgtc.html`
- `test/*.test.js`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Implement backend logic in functions (e.g., functions/upload.js, functions/file/[id].js, functions/api/manage/*)
- Update or add utility/helper modules if needed (e.g., functions/utils/*.js)
- Update admin UI files (admin.html, admin-imgtc.html) to reflect new or changed features
- Add or update automated tests (test/*.test.js, test/helpers.js)
- Update documentation in README.md and README-zh.md

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.