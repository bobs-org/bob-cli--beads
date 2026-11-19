# Bead: bob-cli-no.3 — Bank card weekly-import button opens the Command Mode preview

[Bead Pages](../README.md) / [bob-cli-no](README.md) / bob-cli-no.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5j.linker.w0.md) · **Assignee:** `bob-cli-no.3` · **Size:** small
**Created:** 2026-11-19 14:47:07 EST · **Closed:** 2026-11-19 17:26:47 EST
**Plan:** [202611/bank\_import\_delete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import_delete.md)

## Description

card: in bob-plugins, turn the bank queue card's static "Weekly import" footer text into a one-click chip. The chip opens the Command Mode preview of `bank import -D ~/Downloads/*.qfx` and shows a fallback notice only when Command Mode is unavailable.

## Notes

[2026-11-19T22:25:54Z · bob-cli-no.3] PROPOSED FOLLOW-UP: docs:check lint fails on clean tree — mac-capture capture-previews.md (6171 words) and keyboard.md (6027 words) exceed the 6000-word reference/ budget; unrelated to this phase

[2026-11-19T22:26:14Z · bob-cli-no.3] PROPOSED FOLLOW-UP: ms-budget perf tests flake under full-suite parallel load (event-link-times, frees/keep-moving KT1-KT8, dependencies-stage-performance); each passes in isolation with this phase applied

[2026-11-19T22:26:30Z · bob-cli-no.3] PROPOSED FOLLOW-UP: task-status-cycler vault deploy still pinned to ws15 uncommitted build 795fad3 (bytes match no commit); its owning agent must sync it — do not -F

[2026-11-19T22:26:47Z · bob-cli-no.3] Bank queue footer now renders Weekly import label + focusable chip (bob bank import -D ~/Downloads/*.qfx) that calls commandMode.preview with that exact argv; fallback Notice only when Command Mode missing/throws, silent on settled refusals. Shared commandModePreviewFor helper factored with keep-inbox. Verified: build+build:check pass, bank-cards 27/27, keep-inbox 34/34, test:perf 8/8, docs inventory current; full unit 7544/7550 with only load-flaky ms-budget perf tests (green in isolation); docs:check lint red identically on clean tree (pre-existing). Synced bob-ledger-tools to vault from landed tree; task-status-cycler left for ws15 owner.

## Dependencies

- **Depends on:** [bob-cli-no.2](bob-cli-no.2.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-no.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-no.3/README.md) | [bob-cli-no.3](bob-cli-no.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c3ca244`](https://github.com/bobs-org/bob-plugins/commit/c3ca2445a204923de58b38c5b8facec2a23f96af) | feat(bank): queue card weekly-import chip opens Command Mode preview | [bob-cli-no.3](bob-cli-no.3.md) | 2026-11-19 17:28:02 EST |
