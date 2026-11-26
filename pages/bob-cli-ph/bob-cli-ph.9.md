# Bead: bob-cli-ph.9 — Reviewed migration of legacy ALL-CAPS drawers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.9

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.9` · **Size:** small
**Created:** 2026-11-22 17:36:49 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

vault-migration: confirm every host writes bold, inventory the legacy drawers, and apply Bryan's per-line rename or release decisions through a gate.

## Notes

[2026-11-26T00:11:25Z · bob-cli-ph.9] Migration prep done 2026-11-26 (apollo): writer gate passes behaviorally on all hosts (installed bob writes `- **Books to Read**` via throwaway-vault dry-run on athena/apollo/mac; all hosts pass bold-drawer-read probe; deployed plugin bundles identical on all hosts incl. bold-writes markers). Live inventory (installed bob 0.6.0, same as debug build): 10 legacy drawers (NOTES x6 in 5 notes, NOTES: x1, OPTIONS: x1, MOTIVATION x1, DONE x1), 0 duplicate identities, 1 empty bold drawer (done/sase_done.md:1420, keep), 1 trailing-colon lead (2026/20261113.md:31 **Note:**, keep as note). Census diff: plan said ~7; exact count is 10 (bob.md holds 2 NOTES; sase_art_links.md + sase_blog.md gained NOTES via bob-cli-on filing). Dry-runs clean, 0 merges: NOTES->Notes (5 notes; 9 excluded are ordinary ## NOTES headings, out of scope), NOTES:->Notes, OPTIONS:->Options, MOTIVATION->Motivation. DONE proposed for release (no bytes). Staging gate turn next for Bryan decisions.

## Dependencies

- **Blocks:** [bob-cli-ph.10](bob-cli-ph.10.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.5](bob-cli-ph.5.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.6](bob-cli-ph.6.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.7](bob-cli-ph.7.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.9.md) | [bob-cli-ph.9](bob-cli-ph.9.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:g1][1] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
