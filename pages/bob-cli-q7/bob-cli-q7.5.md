# Bead: bob-cli-q7.5 — Mac: Go rows in the block-ID card

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.5` · **Size:** medium
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-25 22:38:43 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

mac-browse: turn the goto-eligible block-ID card into a scoped Go To browse (selectable Go rows, exact preselect, archived section, Return lands, Tab completes), update mint copy, and mirror the /route^id search key.

## Notes

[2026-11-26T01:40:18Z · bob-cli-q7.5] PROPOSED FOLLOW-UP: docs-check generated-drift gate fails identically on the clean base tree (plugin inventory stale for docs/bob-ledger-tools.md and docs/index.md, unrelated to mac-browse); needs npm-built plugin manifests or a docs:gen refresh

[2026-11-26T03:23:40Z · bob-cli-q7.5] PROPOSED FOLLOW-UP: just check (clippy, recipe line 83, exit 101) fails identically on the clean base tree — see the same entry on bob-cli-q7.2; mac-browse verification rests on just portable-check (2767 green), macOS CI run 45742615090 (green), and docs lint ok

[2026-11-26T03:36:23Z · bob-cli-q7.5--1] PROPOSED FOLLOW-UP: verify monitor p8f1wh just check exit 101 (clippy recipe line 83) reproduces on clean bob-cli tree — git status empty, zero local changes; sole error is clippy -D clippy::manual-contains in tests/cli/capture/complete_block_id.rs:292 plus pre-existing warnings; q7.5 touches only bob-mac-capture so this is outside bead scope; see q7.2 clean-master just-check entry and q5.1.1.land complete_block_id lint tracking

[2026-11-26T03:38:43Z · bob-cli-q7.5--1] mac-browse complete: scoped Go To browse in block-ID card verified by mac portable-check 2767 tests 0 failures on final tree; mac bundle + typecheck-tests and macOS CI run 45742615090 green per phase record; bob-cli just check exit 101 is clean-tree clippy failure outside scope (recorded follow-up)

## Dependencies

- **Depends on:** [bob-cli-q7.2](bob-cli-q7.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q7.4](bob-cli-q7.4.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q7.6](bob-cli-q7.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.5.md) | [bob-cli-q7.5](bob-cli-q7.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e6b22ed`](https://github.com/bobs-org/bob-mac-capture/commit/e6b22ed2709713be4444c2667dea0c1dd8652b2d) | feat(mac): turn block-ID card into scoped Go To browse | [bob-cli-q7.5](bob-cli-q7.5.md) | 2026-11-25 22:39:06 EST |
