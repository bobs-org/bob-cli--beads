# Bead: bob-cli-87.11 — Corpus gate on athena and long-tail fixes

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.11` · **Size:** medium
**Created:** 2026-10-16 07:13:19 EDT · **Closed:** 2026-10-16 18:50:19 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

corpus-gate: add a dev script that renders every area/project note to scratch with -o and dry-runs every vault note. Require zero failures, missing glyphs, and Type 3 body fonts. Visually review representative pages and fix the long tail.

## Notes

[2026-10-16T22:50:19Z · bob-cli-87.11--3] Verified 2026-10-16: cargo build and the athena note snapshot corpus gate passed (101 renders, 5,054 dry runs, zero failures, missing glyphs, overfull warnings, or Type 3 fonts; vault git status unchanged). Reviewed all 279 render warnings and 9,873 explained dry-run warning entries; no TODOs occur in explanations. Visually inspected sase_dyn_agent_fam, sase_blog, cash, bob, sase, inbox, gtd, two small projects, and a done project. just check-scripts, cargo test note_snapshot (146 passed), and git diff --check passed; recorded gate metrics in docs/highlights-create.md. epic-symbols had no entries.

## Dependencies

- **Blocks:** [bob-cli-87.12](bob-cli-87.12.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.6](bob-cli-87.6.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.7](bob-cli-87.7.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.11.md) | [bob-cli-87.11](bob-cli-87.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d114c56`](https://github.com/bobs-org/bob-cli/commit/d114c56288be765a2010de755ea9f4d966192847) | fix(note-snapshot): harden corpus rendering edge cases | [bob-cli-87.11](bob-cli-87.11.md) | 2026-10-16 18:51:18 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.11--3][1] | Check whether prior phase work left notes or unresolved work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.11.md

<!-- sase:referenced-by:end -->
