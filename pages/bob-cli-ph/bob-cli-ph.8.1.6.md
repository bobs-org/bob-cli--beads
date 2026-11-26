# Bead: bob-cli-ph.8.1.6 — Mac drawer acceptance, screenshots, and documentation

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.6` · **Size:** small
**Created:** 2026-11-25 20:56:01 EST · **Closed:** 2026-11-26 03:20:54 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

mac-acceptance: verify the integrated feature on exact-SHA macOS CI, publish the drawer render screenshots, reconcile Mac and bob-cli docs with what shipped, and run every repo gate.

## Notes

[2026-11-26T08:19:42Z · bob-cli-ph.8.1.6--1] --list

[2026-11-26T08:20:33Z · bob-cli-ph.8.1.6--1] PROPOSED FOLLOW-UP: migrate remaining drawer test goldens to ph.10 bold-only behavior (just check red on clean master: ~25 lib + 55 cli failures, e.g. REQUIREMENTS vs Requirements, __AGENDA__ vs AGENDA; ph.10 commits 9573ff86/46aba677 changed behavior, c3a9bdd9 migrated only task-requirements vectors; master CI runs 45758122303 45763997268 45755965376 45752393102 all failure) -r "Acceptance gate just check fails on the clean base tree; needs a ci-type task bead"

[2026-11-26T08:20:42Z · bob-cli-ph.8.1.6--1] PROPOSED FOLLOW-UP: finish mac-acceptance remainder blocked by red gate (Mac commit a2e79f65 unpushed: 4-word model-binding test fix + draft-paint docs; push master, watch exact-SHA macOS run green, download render-fixtures artifact, inspect drawer PNGs, publish via sase artifact create, attach refs to bob-cli-ph.8.1.6 and bob-cli-ph.8) -r "Push was gated on both acceptance gates passing; just check failed so no push per phase instructions"

[2026-11-26T08:20:54Z · bob-cli-ph.8.1.6--1] Acceptance docs landed (631a49d5 docs-only; Mac a2e79f65 committed unpushed). just check on clean tree fails in -p bob-obsidian lib (~25) + cli (55) drawer goldens caused by ph.10 9573ff86/46aba677, pre-existing vs 8.1.6 base (recorded as PROPOSED FOLLOW-UP); master CI runs 45758122303/45763997268/45755965376/45752393102 failure corroborate. epic-symbols clean. Mac push+screenshots recorded as PROPOSED FOLLOW-UP, push gated on green gates.

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.6.md) | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`631a49d`](https://github.com/bobs-org/bob-cli/commit/631a49d5d55f18ea6b343ce778f6148e457e1bf1) | docs(drawers): reconcile Mac Capture section with shipped true-case behavior | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 2026-11-26 03:03:30 EST |
| bob-mac-capture | [`bob-mac-capture@a2e79f6`](https://github.com/bobs-org/bob-mac-capture/commit/a2e79f65cbf56c09c3a6c734a902d23b477f44e0) | fix(mac-capture): bind drawer pipeline test models; document draft drawer paint | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 2026-11-26 03:04:43 EST |
