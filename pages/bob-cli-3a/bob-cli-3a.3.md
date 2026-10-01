# Bead: bob-cli-3a.3 — Release, docs, deploy, and live-verify gate

[Bead Pages](../README.md) / [bob-cli-3a](README.md) / bob-cli-3a.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3y.md) · **Assignee:** `bob-cli-3a.3` · **Size:** small
**Created:** 2026-10-01 11:19:39 EDT · **Closed:** 2026-10-01 12:09:09 EDT
**Plan:** [202610/fresh\_mark.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/fresh_mark.md)

## Description

mark-rollout: bump bob-ledger-tools to 1.10.0, update both READMEs, the Surfaces table, and the vault snippet comment, run the full plugin suite and manifest validation, deploy with bob plugins sync, and record the live-verify checklist Bryan runs in Obsidian.

## Notes

[2026-10-01T16:08:56Z · bob-cli-3a.3] PROPOSED FOLLOW-UP: just lint fails identically on the clean base tree (clippy unnecessary_to_owned error in tests, bob-cli test target); pre-existing, unrelated to mark-rollout docs-only change

[2026-10-01T16:09:09Z · bob-cli-3a.3] Rollout done: manifest 1.10.0, READMEs + Surfaces row + snippet comment updated, live-verify checklist in docs/freshness.md §11. npm test 1066 pass, validate 6/6, bob plugins sync deployed ledger-tools (3 copied). just lint fails identically on clean base (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-3a.2](bob-cli-3a.2.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3a.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3a.3/README.md) | [bob-cli-3a.3](bob-cli-3a.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d2aae45`](https://github.com/bobs-org/bob-cli/commit/d2aae45e51949431d47b9a64dc29b94fc36ac3fa) | docs(freshness): land mark rollout surfaces and live-verification checklist | [bob-cli-3a.3](bob-cli-3a.3.md) | 2026-10-01 12:11:26 EDT |
| bob-plugins | [`bob-plugins@0d018c7`](https://github.com/bobs-org/bob-plugins/commit/0d018c70156e7d9ed124e2103b8ba2b699982a77) | feat(ledger-tools): mark rollout v1.10.0 with docs and manifest | [bob-cli-3a.3](bob-cli-3a.3.md) | 2026-10-01 12:12:00 EDT |
