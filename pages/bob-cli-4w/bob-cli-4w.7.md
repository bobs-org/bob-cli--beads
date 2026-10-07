# Bead: bob-cli-4w.7 — Library health and coverage rows in doctor

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.7` · **Size:** small
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 21:55:00 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

doctor: add warning-level library rows to `bob ref doctor`: index totals, diagnostics, duplicate identities, leaked mirrors, and the count of unindexed zorg-era reading records outside the ref directory.

## Notes

[2026-10-07T01:55:00Z · bob-cli-4w.7] doctor: 5 warning-level library rows live (library totals, diagnostics rollup excl. marker_mirror_excluded, identity superseded/shared, annotations mirror count, zorg coverage with mirrored subtraction). Verified: 6 new CLI tests + 4 coverage unit tests pass; existing doctor/alias/ref_library tests green; fmt clean; clippy clean for touched files; real-vault doctor exits 0 with plausible rows (594 notes, 114 mirror notes, ~424 zorg records: work_ref.md 75, nvim_ref.md 69). Fixed a multibyte-slice panic found by the real-vault run. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-4w.1](bob-cli-4w.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.11](bob-cli-4w.11.md) ◐ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.3](bob-cli-4w.3.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.7/README.md) | [bob-cli-4w.7](bob-cli-4w.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e64b2df`](https://github.com/bobs-org/bob-cli/commit/e64b2df2eacf125a30b130266e4287903ce37b44) | feat(ref-doctor): add library health rows to bob ref doctor | [bob-cli-4w.7](bob-cli-4w.7.md) | 2026-10-06 22:07:39 EDT |
