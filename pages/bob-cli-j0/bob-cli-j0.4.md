# Bead: bob-cli-j0.4 — vault-sync task-loss tripwire

[Bead Pages](../README.md) / [bob-cli-j0](README.md) / bob-cli-j0.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d4.md) · **Assignee:** `bob-cli-j0.4` · **Size:** medium
**Created:** 2026-11-09 07:43:10 EST · **Closed:** 2026-11-09 08:43:47 EST
**Plan:** [202611/lost\_task\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/lost_task_guards.md)

## Description

loss_tripwire: before each commit, find task block IDs this host removed that inbound links still need, or open tasks that vanished; confirm after a settle window, then record, log, and notify without editing notes.

## Notes

[2026-11-09T13:28:01Z · bob-cli-j0.4] PROPOSED FOLLOW-UP: See existing bob-cli-it for the docs-check stale ignored mount index collision — just docs-check failed because the gitignored docs/reference/plugins/index.md exists in this reused workspace but is absent from HEAD; no new task needed.

[2026-11-09T13:43:47Z · bob-cli-j0.4] Implemented linked open-task loss detection with a 30-second settle window, persistent status/log reporting, restore guidance, dry-run coverage, and vault-sync integration tests. Verified cargo check --lib, focused vault-sync tests, just docs-gen, final just check, and git diff --check. just docs-check remains blocked by the existing bob-cli-it stale ignored mount index collision, recorded as a proposed follow-up on this bead.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.4/README.md) | [bob-cli-j0.4](bob-cli-j0.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7fe12b3`](https://github.com/bobs-org/bob-cli/commit/7fe12b33e46db7429e5d7e95d91afe57103e13f0) | feat(vault-sync): detect linked task losses | [bob-cli-j0.4](bob-cli-j0.4.md) | 2026-11-09 08:45:02 EST |
