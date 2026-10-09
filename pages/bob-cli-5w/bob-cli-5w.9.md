# Bead: bob-cli-5w.9 — Read-time 🔓 hand-off glyph in today's ledger

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.9` · **Size:** small
**Created:** 2026-10-09 11:54:16 EDT · **Closed:** 2026-10-09 12:41:28 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

ledger_glyph: in bob-ledger-tools, draw a faint read-time 🔓 after a live Task Link under today's open Pomodoros whose task had a prerequisite completed today, with a tooltip naming it. It is derived from the Tasks cache and never stored. Ships tests, a version bump, a README update, and a sync.

## Notes

[2026-10-09T16:41:08Z · bob-cli-5w.9] PROPOSED FOLLOW-UP: decisions strand closed-task-hands-slot-to-successors skipped per epic auto-decision (decision_record=no); land agent to triage

[2026-10-09T16:41:13Z · bob-cli-5w.9] PROPOSED FOLLOW-UP: glossary strand successor-link skipped per epic auto-decision (glossary_term=no); land agent to triage

[2026-10-09T16:41:17Z · bob-cli-5w.9] PROPOSED FOLLOW-UP: test-navigation-roll-decay.cjs has 2 failures (picker-single P2 roll, [?] vs [ ]) reproducing identically on the clean base tree; date-sensitive, unrelated to ledger_glyph

[2026-10-09T16:41:28Z · bob-cli-5w.9] ledger_glyph shipped: read-time unlock glyph in bob-ledger-tools 1.37.0 (Live Preview + Reading, Tasks-derived, tooltip names prereq, +N for several). Verified: 19/19 new tests green, ledger/cycler/build suites 754/754 green, build:check + validate green, plugins sync deployed. Full suite has 2 pre-existing nav roll-decay failures confirmed identical on clean base (noted as follow-up).

## Dependencies

- **Blocks:** [bob-cli-5w.11](bob-cli-5w.11.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5w.2](bob-cli-5w.2.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.9/README.md) | [bob-cli-5w.9](bob-cli-5w.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a06b403`](https://github.com/bobs-org/bob-plugins/commit/a06b403d80c0695bce9ed4a44b858916aea8a0b4) | feat(ledger-tools): read-time unblocked hand-off glyph in today's ledger | [bob-cli-5w.9](bob-cli-5w.9.md) | 2026-10-09 12:44:27 EDT |
