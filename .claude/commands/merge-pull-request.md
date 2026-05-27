---
name: merge-pull-request
description: Workflow command scaffold for merge-pull-request in jaro_winkler.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /merge-pull-request

Use this workflow when working on **merge-pull-request** in `jaro_winkler`.

## Goal

Merge a pull request, which often includes both the original changes and sometimes additional related files (like CI configs).

## Common Files

- `.github/workflows/test.yml`
- `ext/jaro_winkler/extconf.rb`
- `ext/jaro_winkler/jaro.c`
- `README.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Merge the branch into main
- Include all files changed in the PR (could be code, CI, docs, etc.)

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.