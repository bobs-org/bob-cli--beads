# Bead: bob-cli-du.9 — Migrate implements, turn it on in chezmoi, record memory, and run acceptance

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.9` · **Size:** medium
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 22:24:23 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

rollout: reverse Bryan's 14 implements links with the new rename, add complete_labels to chezmoi, make the accepted memory edits, sweep docs, and run end-to-end acceptance.

## Notes

[2026-10-29T02:24:07Z · bob-cli-du.9--3] ROLLOUT VERIFIED:
- Release `bob` built successfully; built and installed `relations rename --help` both expose `--reverse`.
- Scratch pre-migration snapshot dry-run for `implements` → `implemented by` (`--reverse`) returned 14 links, 4 notes, 12 mirror updates, 7 done links across 2 done notes; it was write-free. The migration diff changed no task checkbox status lines.
- Live migration commit: `2c963688ed09e67c480a58bc6a5753b5bfe47e60` (`bob relations rename: implements → implemented by (reversed)`). Undo: `git revert 2c963688ed09e67c480a58bc6a5753b5bfe47e60`. On a scratch clone at that commit, the revert restored the exact pre-migration tree (`610e11c1b2fbcc7b4864217b9ceed34de9d5829e`).
- Built and installed `bob relations list --all --format json` both show `implemented by` 14 and `verified by` 1 as complete labels, no `implements` row, and no warnings. Live vault sync is clean at matching local/remote SHA `c41ea49b4e23e44e4a4e62ad887094e9839ad17e`; the `verified by` edge remains.
- `bob task reconcile --dry-run`: already in sync, no changes. `cargo test --test cli relations_complete`: 29 passed, 0 failed.
- Chezmoi config commit `6a7ba1839d82c44a829635d83fab09a5a0f90b6a`; `~/.config/bob/config.yml` contains `implemented by` and `verified by`, and `chezmoi status` is clean.
- `just docs-check`: all implemented gates passed; documentation unit tests 447 passed, 1 skipped because font generation dependencies are absent. `bob plugins sync` exited 0 after source fast-forward: 0 copied, 0 skipped, 22 unchanged (already deployed).
- Confirmed `glossary:task-relation` names both cancel and complete status exceptions. No decision memory was changed.
- Remaining host rollout: install the new Bob Mac Capture build before running `chezmoi update` on the MacBook; run `chezmoi update` on the other hosts.

[2026-10-29T02:24:23Z · bob-cli-du.9--3] Verified 14-link reverse migration, exact scratch revert, config and acceptance checks; see rollout evidence note for results and host rollout order.

## Dependencies

- **Depends on:** [bob-cli-du.4](bob-cli-du.4.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-du.7](bob-cli-du.7.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-du.8](bob-cli-du.8.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.9.md) | [bob-cli-du.9](bob-cli-du.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7d3ce70`](https://github.com/bobs-org/bob-cli/commit/7d3ce705618cb9be501abda82db15f30dc14e2c0) | docs(relations): mark complete-label nav support shipped | [bob-cli-du.9](bob-cli-du.9.md) | 2026-10-28 22:25:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.9--2][1] | Need the phase scope, notes, and design file before continuing the authorized migration work | 1 |
| read-by | [agent:bob-cli-du.9--3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.9.md

<!-- sase:referenced-by:end -->
