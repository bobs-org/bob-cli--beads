# Bead: bob-cli-ij.1 — bob-cli nearest-note colors, grey mute, and Review time on gtd

[Bead Pages](../README.md) / [bob-cli-ij](README.md) / bob-cli-ij.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19s.md) · **Assignee:** `bob-cli-ij.1` · **Size:** medium
**Created:** 2026-11-07 17:26:27 EST · **Closed:** 2026-11-07 18:09:58 EST
**Plan:** [202611/gtd\_root\_and\_area\_colors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_root_and_area_colors.md)

## Description

cli: in bob-cli, resolve each home's hue from the nearest area or project `color:` slot (palette hue or grey), report `hue_source`, give root groups the root's own hue, mute types named after a grey top-level area, point the built-in review_time at gtd, extend the shared vectors, and update docs and memory.

## Notes

[2026-11-07T23:09:58Z · bob-cli-ij.1] cli phase done. Nearest area/project color: slot (palette hue or grey/gray, case-insensitive; blank inherits; invalid lints area_color_invalid once per path for every invalid value on the walked chain, then inherits) resolves Home.hue + new hue_source (color|muted|hash) and root_hue; root groups use root_hue; stats homes catalog adds hue_source (omitted for buckets/arealess); CLI paints muted dots dim; lint text reworded. Type hues: area map is Option<Hue>, grey area -> (null, area); note-defaults cache VERSION 2 keeps grey (null) apart from non-areas (omitted). Built-in review_time is in: [gtd]; H15 recomputed to 50m (bob is a gtd project), M10 unchanged. Vectors: homes case nearest-color-and-grey (+9 notes, 6 sessions, 2 lints), themes hue case area-grey-mutes. Docs: pomodoro-homes R7/R8/R4/R11/palette/vector table, stats.md (hue_source, grey root lanes, review_time, M10/H15), plan.md Today roots hue, task-types PT5 + example, vault-format ^gtd row, migration-notes. Memory: glossary:root-parent corrected (only authorized edit); sase memory init + just docs-gen regenerated docs/reference/glossary.md. Verified: just fmt, just lint (exit 0, no new warnings in touched code), just test (5489 lib + all integration suites pass), just docs-check passed.

## Dependencies

- **Blocks:** [bob-cli-ij.2](bob-cli-ij.2.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ij.3](bob-cli-ij.3.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ij.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ij.1/README.md) | [bob-cli-ij.1](bob-cli-ij.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d1b645d`](https://github.com/bobs-org/bob-cli/commit/d1b645d1c703927016be7edfe43bd7b61de9c5fd) | feat(homes): resolve hues from the nearest area or project color slot, add grey mute, and root review\_time at gtd | [bob-cli-ij.1](bob-cli-ij.1.md) | 2026-11-07 18:10:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ij.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ij.2][2] | Need phase 1 close notes for what landed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ij.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ij.2/README.md

<!-- sase:referenced-by:end -->
