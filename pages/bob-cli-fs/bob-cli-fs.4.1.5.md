# Bead: bob-cli-fs.4.1.5 — Author generic pull-in copy and relation human output

[Bead Pages](../README.md) / [bob-cli-fs.4.1](bob-cli-fs.4.1.md) / bob-cli-fs.4.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.md) · **Assignee:** `bob-cli-fs.4.1.5` · **Size:** medium
**Created:** 2026-11-02 12:29:13 EST · **Closed:** 2026-11-02 16:17:16 EST
**Plan:** [202611/capture\_relation\_successors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_relation_successors.md)

## Description

presentation: emit ordered pull-in groups and copy for every offer kind, render relation offers and held notices through the core copy builder, and verify existing group compatibility.

## Notes

[2026-11-02T21:17:16Z · bob-cli-fs.4.1.5] Verified presentation: JSON pull-in groups+copy for every offer kind (hand_off, relation, project, project_finished, keep_moving), relation human output via copy.rs (48-char truncation, knot U+1FAA2, never unblocked), held-only notices, unavailable muted line, and pull_in_choice_required refusal reusing the same group/copy builder. cargo test --test cli -- capture::relation_presentation 13/13; relation_successors 33; keep_moving 37; successor_offers 17; project_pull_in 14; project_note_offer 27; project_close 4. just fmt, just lint, just check passed. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-fs.4.1.4](bob-cli-fs.4.1.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.4.1.6](bob-cli-fs.4.1.6.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.4.1.5/README.md) | [bob-cli-fs.4.1.5](bob-cli-fs.4.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d53756f`](https://github.com/bobs-org/bob-cli/commit/d53756fdd5b33121191130c07a1715f9d7d481e4) | feat(capture): emit ordered pull-in groups and relation human copy | [bob-cli-fs.4.1.5](bob-cli-fs.4.1.5.md) | 2026-11-02 16:18:20 EST |
