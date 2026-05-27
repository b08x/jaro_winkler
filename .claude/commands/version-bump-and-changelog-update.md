---
name: version-bump-and-changelog-update
description: Workflow command scaffold for version-bump-and-changelog-update in jaro_winkler.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /version-bump-and-changelog-update

Use this workflow when working on **version-bump-and-changelog-update** in `jaro_winkler`.

## Goal

Bump the gem version and update the changelog after a feature or fix is merged.

## Common Files

- `lib/jaro_winkler/version.rb`
- `CHANGELOG.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the version number in lib/jaro_winkler/version.rb
- Add or update the relevant entry in CHANGELOG.md

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.