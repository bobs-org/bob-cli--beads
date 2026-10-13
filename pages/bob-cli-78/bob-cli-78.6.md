# Bead: bob-cli-78.6 — Task Card Depends on and Schedule apply and reverse the cascade

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.6` · **Size:** medium
**Created:** 2026-10-13 03:14:28 EDT · **Closed:** 2026-10-13 04:38:25 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

nav-gestures: wire the subtree pass into every Task Card Depends on writer and, under schedule_cascade, every ^prj Schedule writer, with descendant writes, link consumption, commitment transfer, notices, and deploy.

## Notes

[2026-10-13T08:38:03Z · bob-cli-78.6] PROPOSED FOLLOW-UP: Update glossary:project-task to say sub-projects inherit ancestors blocking via parent: (memory_glossary=no auto-decision)

[2026-10-13T08:38:13Z · bob-cli-78.6] PROPOSED FOLLOW-UP: Full bob-plugins npm test still fails 4 ledger-tools-unblocked-glyph cases + decision-card rebuild-triggers + stage-ranker 16ms timing flake, all reproducing on clean origin/master (plan pre-existing bob-cli-6v/-6w/-3w class)

[2026-10-13T08:38:25Z · bob-cli-78.6] 218/219 subtree pass wired into all Task Card Depends-on writers (shared transaction, Task Link, stage batch, counted, Ctrl+D, api v3) and Schedule set/delete/counted under schedule_cascade, with descendant writes, link consumption, commitment transfer, and notices. New 13-case gestures test green; build+validate green; full npm test 2633 pass with only 6 failures that reproduce on clean master (recorded as follow-ups). Deployed nav 2.31.0 to vault (verified byte-identical) and committed db8699a. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-78.5](bob-cli-78.5.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.8](bob-cli-78.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.6/README.md) | [bob-cli-78.6](bob-cli-78.6.md) | 0 |
