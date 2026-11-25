# Bead: bob-cli-q6.4 — Hide native Properties on bank.md behind the fail-open gate

[Bead Pages](../README.md) / [bob-cli-q6](README.md) / bob-cli-q6.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g2.md) · **Assignee:** `bob-cli-q6.4` · **Size:** medium
**Created:** 2026-11-25 12:49:32 EST
**Plan:** [202611/bank\_property\_card\_fold.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_property_card_fold.md)

## Description

bank-takeover: spike bank.md YAML parity in real Obsidian, add bank to the 240q coordinator, acquire and release ownership from the bank host, promote the bank-native e2e to full takeover verification, flip docs, and apply the decision-gated glossary corrections.

## Notes

[2026-11-25T23:05:48Z · bob-cli-q6.4] PROPOSED FOLLOW-UP: Resolve the unchanged docs-check budget failures: docs/reference/capture-syntax.md 6058/6000, json-outputs.md 6007/6000, bob-ledger-tools.md 6040/6000, and bob-navigation-hotkeys.md 6068/6000. These same four failures and counts reproduce on the base docs; plugin-apis.md 9279/8000 is warning-only.

[2026-11-25T23:05:55Z · bob-cli-q6.4] PROPOSED FOLLOW-UP: Investigate the 8 unrelated Navigation Hotkeys unit failures exposed after rebuilding its unchanged source fragments: six task-move history/runtime tests, the routed Alt+N due inbox-row test, and splitRequirementCarry guarded Undo. This full unit run had 9676 passes and 8 failures; the performance stage passed. Related prior carry implementation coverage is bob-cli-on.11.1.4.

## Dependencies

- **Depends on:** [bob-cli-q6.3](bob-cli-q6.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q6.6](bob-cli-q6.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q6.4.md) | [bob-cli-q6.4](bob-cli-q6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1ca74ec`](https://github.com/bobs-org/bob-cli/commit/1ca74ece68165cc6fc07af59fe4e2bedf7519f4f) | docs(bank): document evidence-gated Properties | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 18:24:50 EST |
