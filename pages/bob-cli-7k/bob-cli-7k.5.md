# Bead: bob-cli-7k.5 — H highlight picker layer

[Bead Pages](../README.md) / [bob-cli-7k](README.md) / bob-cli-7k.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.5` · **Size:** medium
**Created:** 2026-10-14 09:32:31 EDT · **Closed:** 2026-10-14 11:22:46 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

## Description

refs-copy-highlight-picker: drop `-c` from the inspector's ref-show fetch and add the H layer that reaches every highlight and standalone note (digits for the visible window, arrows for the rest, A for all highlights).

## Notes

[2026-10-14T15:22:30Z · bob-cli-7k.5] PROPOSED FOLLOW-UP: Mac typecheck-tests unverified — kellys-macbook-pro.tail297af1.ts.net SSH timed out; portable-check on athena compiled RefsCore (1144 tests, 0 failures) but BobMacCapture picker UI/model tests were not type-checked this turn

[2026-10-14T15:22:46Z · bob-cli-7k.5] H picker landed in bob-mac-capture: show fetch dropped -c (inspector still uses commentedHighlights); H opens a HIGHLIGHTS n layer (digits=window row, arrows, A=all highlights without own_notes, esc back to card). Athena just portable-check: 1144 tests, 0 failures. Mac typecheck-tests skipped (host SSH timed out); macOS app targets unverified.

## Dependencies

- **Depends on:** [bob-cli-7k.4](bob-cli-7k.4.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7k.6](bob-cli-7k.6.md) ◐ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.5/README.md) | [bob-cli-7k.5](bob-cli-7k.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9b70c62`](https://github.com/bobs-org/bob-mac-capture/commit/9b70c629cea5a8d138f768bbbf3e5a92ef5cd574) | feat(refs): add H highlight picker layer | [bob-cli-7k.5](bob-cli-7k.5.md) | 2026-10-14 11:24:01 EDT |
