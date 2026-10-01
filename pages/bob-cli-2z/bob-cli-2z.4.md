# Bead: bob-cli-2z.4 — Install bob, verify end to end with dry runs, and hand Bryan the Mac steps

[Bead Pages](../README.md) / [bob-cli-2z](README.md) / bob-cli-2z.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ui](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0ui.md) · **Assignee:** `bob-cli-2z.4` · **Size:** small
**Created:** 2026-09-30 18:46:56 EDT · **Closed:** 2026-09-30 20:28:16 EDT
**Plan:** [202609/close\_work\_log\_entries.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_work_log_entries.md)

## Description

rollout: reinstall bob on this host and (best effort) on the MacBook. Verify the grammar against the live vault with dry runs only, never closing a real session, and give Bryan the checklist for installing the Mac app.

## Notes

[2026-10-01T00:27:28Z · bob-cli-2z.4] Mac checklist for Bryan: (1) on the MacBook, pull bob-cli latest and run cargo install --path . --locked; confirm with `bob capture-parse -f json -- "=x 1 wired the lexer"` showing mode pomodoro_close with log [{"index":1}]. (2) Rebuild/install Bob Mac Capture from the bob-mac-capture repo so it picks up the new pomodoro_close.log / typed_work_log fields (additive, schema v1 unchanged). (3) Smoke-test in the Mac app: type `=x 1 <text>` and confirm the index chip highlights and the close card shows the typed entry; submit only a dry run or test draft. Best-effort MacBook reinstall was NOT done from here (no MacBook reachable from this host); pending for Bryan or a Mac-side agent.

[2026-10-01T00:28:16Z · bob-cli-2z.4] Reinstalled bob (cargo install --path . --locked, exit 0). capture-parse verified against plan worked table: entries, repetition, lexical errors, incomplete dangling index, block-link rejection, prose unchanged, plain =x byte-identical. Live-vault checks dry-run only: close dry-run safely refused (no open Pomodoro), task dry-run planned ok; vault untouched. Mac checklist in bead note; MacBook reinstall pending (not reachable from here).

## Dependencies

- **Depends on:** [bob-cli-2z.3](bob-cli-2z.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-2z.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-2z.4/README.md) | [bob-cli-2z.4](bob-cli-2z.4.md) | 0 |
