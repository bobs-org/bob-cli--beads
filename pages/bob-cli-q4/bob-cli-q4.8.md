# Bead: bob-cli-q4.8 — Vector-pinned JS settle twin behind a ledger-tools API

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.8` · **Size:** large
**Created:** 2026-11-25 08:51:36 EST · **Closed:** 2026-11-25 14:20:05 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

settle-twin: port `settle_note` to bob-ledger-tools, pinned byte for byte by copied settle vectors. Expose it as a versioned `taskSettle` API: pure settle, editor apply with a path guard and the cursor policy, and the tier-2 pending scheduler with a global flush. Consumers degrade to reconcile-heals when the API is absent.

## Notes

[2026-11-25T19:20:49Z · bob-cli-q4.8.1.land] COMPLETE PROVIDER: bob-cli-q4.8.1 closed with frozen taskSettle v1 in bob-ledger-tools 1.161.0. Downstream consumers (q4.9 cycler, q4.10 nav, q4.11 links, q4.13 acceptance) should look up app.plugins.plugins["bob-ledger-tools"]?.api?.taskSettle and degrade to reconcile-heals when absent, too old, or throwing.

API: version 1. settleNote({path, contents, today}) -> {contents, changed, lineMap} with no I/O. applyToEditor(editor, path, options) applies synchronously; staged contents require explicit matching expected; missing/mismatched expected is idle reason "preimage" with no writes. schedulePending({editor, path, identity}) arms/rearms ~500 ms. flushPending() drains eligible work. Identity is {blockId, line, text}: supplied blockId is authoritative (unique match only); otherwise exact text at the hinted line or an unambiguous exact-text match; a line number alone is never identity. Missing/ambiguous identity drops pending work. Cursor policy is stay: own-task cursor keeps physical line; jumpTarget reports the moved task. Contract details: https://bobs-org.github.io/develop/plugins/task-settle/

Canonical copy comparison now runs in linked workspaces (walk-up lookup). All 18 vectors still pin the JS twin. Stay/jump, staged atomic gesture+settle, and measured undo ordering unchanged. Real Obsidian undo e2e passed, including staged-without-expected preimage refusal and deleted-blockId pending flush refusal.

Verification: plugin npm test 9542 pass; e2e undo pass; docs split kept ledger-tools 5994/6000 and plugin-apis 9276≤9287. docs:check and just check exposed only independently reproduced pre-existing failures (capture-syntax 6011, navigation-hotkeys 6068, capture/drawer/meetings/hooks Rust tests on e6eb52a1). just symvision unavailable. epic-symbols empty on q4.8.1 and q4.8.

Follow-up dispositions from the child lander: cycler Notes and frees-mark flakes already fixed; docs debt stays on bob-cli-jz / bob-cli-ob; capture-syntax growth on bob-cli-ph.6.1. Containing epic bob-cli-q4 remains open for WASM research and gesture-consumer wiring. Decisions unchanged: settle_cursor=stay, o_in_group=intake_end, wasm_spike=yes, memory_settle_record=no.

## Dependencies

- **Blocks:** [bob-cli-q4.10](bob-cli-q4.10.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.11](bob-cli-q4.11.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q4.3](bob-cli-q4.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.9](bob-cli-q4.9.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) | [bob-cli-q4.8](bob-cli-q4.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.8.1.2][1] | Need parent phase design and DECISIONS | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.2/README.md

<!-- sase:referenced-by:end -->
