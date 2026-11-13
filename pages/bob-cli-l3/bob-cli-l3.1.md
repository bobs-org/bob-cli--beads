# Bead: bob-cli-l3.1 — Migrate the record-surface tests off the retired records config (bob-cli)

[Bead Pages](../README.md) / [bob-cli-l3](README.md) / bob-cli-l3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.dp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.dp.md) · **Assignee:** `bob-cli-l3.1` · **Size:** medium
**Created:** 2026-11-12 16:11:26 EST · **Closed:** 2026-11-12 17:41:29 EST
**Plan:** [202611/record\_capture\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_capture_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-l9][1] | The phase requested macOS collision verification; its fixture migration is separate from these older filesystem assumptions |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-l9/README.md

<!-- sase:links:end -->

## Description

cli-tests: port the RecordVault and sibling fixtures from the retired records: config to real album notes across capture_complete, capture_parse, capture_related, capture album_index, albums registry, bank import_run, and the CLI suite, and refresh the stale root-help snapshot, so the 45 lib and 2 CLI failures at b04120b0 go green without product changes.

## Notes

[2026-11-12T22:19:58Z · bob-cli-l3.1] PROPOSED FOLLOW-UP: gcal sync_args_read_last_n_days_aliases failure persists (tracked by bob-cli-l2) — record in phase notes

[2026-11-12T22:21:41Z · bob-cli-l3.1] PROPOSED FOLLOW-UP: lib suite green except pre-existing gcal sync_args failure also failing on clean base (tracked by bob-cli-l2); subprocess flake passed this run -r Recording pre-existing failure as follow-up per phase instructions

[2026-11-12T22:41:29Z · bob-cli-l3.1] cli-tests done: record fixtures ported to real album notes (tests-only, no product/version/changelog/docs changes). cargo test --lib: 6821 passed, only pre-existing gcal sync_args failure remains (also fails on clean base; tracked by bob-cli-l2; PROPOSED FOLLOW-UP noted). cargo test --test cli: 3642 passed. cargo fmt clean, just lint gate clean, epic-symbols clean. Notes: macOS-only stale_plan collision test passes on Linux here; exact-SHA CI on ubuntu+macos still needs the land step (no commit made per policy).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-l3.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-l3.1/README.md) | [bob-cli-l3.1](bob-cli-l3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b7f74b5`](https://github.com/bobs-org/bob-cli/commit/b7f74b584481453d4e1446d032072cff1405479c) | test(record-capture): migrate record fixtures off retired records config | [bob-cli-l3.1](bob-cli-l3.1.md) | 2026-11-12 17:44:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l3.1][1] | Need full notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-l3.1/README.md

<!-- sase:referenced-by:end -->
