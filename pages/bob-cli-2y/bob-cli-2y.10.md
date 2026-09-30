# Bead: bob-cli-2y.10 — Mutually exclusive dash sections, GTD chores, and lane caps config

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.10` · **Size:** small
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 18:18:00 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

dash-lanes: rebuild dash.md as TODAY / PENDING / NEXT / READY with matching chips, swap the gtd_daily chores, and set max_next / max_pending in the chezmoi config.

## Notes

[2026-09-30T22:18:00Z · bob-cli-2y.10] dash-lanes done: dash.md rebuilt as TODAY/PENDING/NEXT/READY with TODAY/PENDING/NEXT/READY/BLOCKED/PLAN chips (vault commits a0d6635c + 83254268, pushed); gtd_daily NOW chores cancelled 2026-09-30, morning-review + weekly-prune chores added; chezmoi 4857fdb7 applied, workspace bob (schema v2) caps={max_next:15,max_pending:10}. Verified: headless tasks-note parses all 4 blocks error=null (TODAY 0, PENDING 52, NEXT 26, READY 186); chip JS node --check OK; ordering finding: frontmatter group-by-path + file.path/lineNumber sorts precede section sorts, so section sorts are inert tiebreakers. Note for rollout: installed ~/.cargo/bin/bob is still schema v1 until reinstall.

## Dependencies

- **Blocks:** [bob-cli-2y.12](bob-cli-2y.12.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.7](bob-cli-2y.7.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.8](bob-cli-2y.8.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.9](bob-cli-2y.9.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.10/README.md) | [bob-cli-2y.10](bob-cli-2y.10.md) | 0 |
