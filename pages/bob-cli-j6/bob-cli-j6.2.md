# Bead: bob-cli-j6.2 — Mac Capture escapes the \`&\` and \`\*\` aliases

[Bead Pages](../README.md) / [bob-cli-j6](README.md) / bob-cli-j6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aj.md) · **Assignee:** `bob-cli-j6.2` · **Size:** medium
**Created:** 2026-11-09 11:06:45 EST · **Closed:** 2026-11-09 12:46:53 EST
**Plan:** [202611/dot\_semicolon\_modifier\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/dot_semicolon_modifier_aliases.md)

## Description

mac-modifier-alias-escapes: generalize the reply-keyed equals-gesture arm to `.` → `&` and `;` → `*` (fast `..`/`;;`, pre-reply probe, Space/Escape restores on the alias-opened empty picker), with tests, Mac docs, and the glossary escape sentence.

## Notes

[2026-11-09T17:12:37Z · bob-cli-j6.2] PROPOSED FOLLOW-UP: Tighten or split the mounted Mac docs pages that keep bob-cli just docs-check red: capture-panel.md (6020→6013 words), capture-previews.md (6174, unchanged), and keyboard.md (6029→6028), citing bob-cli-h9 for the existing 6,000-word budget failure tracking.

[2026-11-09T17:46:53Z · bob-cli-j6.2--1] Mac scratch verification passed: bundle.sh, just typecheck-tests, and just format-lint. bob-cli just docs-check reproduced only the documented mounted-page budgets: capture-panel 6013, capture-previews 6174, keyboard 6028; tracked by bob-cli-h9. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-j6.1](bob-cli-j6.1.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j6.2.md) | [bob-cli-j6.2](bob-cli-j6.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3c1b645`](https://github.com/bobs-org/bob-cli/commit/3c1b6451d49ea71b24c21cb33643c42977d191e5) | docs(glossary): describe capture modifier aliases | [bob-cli-j6.2](bob-cli-j6.2.md) | 2026-11-09 12:48:11 EST |
| bob-mac-capture | [`bob-mac-capture@ef5dc4a`](https://github.com/bobs-org/bob-mac-capture/commit/ef5dc4ab02138241f3f73b83e54df67d623fd00a) | feat(capture): support modifier alias escapes | [bob-cli-j6.2](bob-cli-j6.2.md) | 2026-11-09 13:20:29 EST |
