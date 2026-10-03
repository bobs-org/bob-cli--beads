# Bead: bob-cli-3n.12.9.2 — Fix the nav dependency writer bugs the landing audit confirmed

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.land.md) · **Assignee:** `bob-cli-3n.12.9.2` · **Size:** medium
**Created:** 2026-10-03 01:27:48 EDT · **Closed:** 2026-10-03 01:38:49 EDT
**Plan:** [202610/task\_dep\_links\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_fixes.md)

## Description

nav-writer-bugs: reject blockquoted Depends-On lines in nav (DP29), fix the kept-link field id lookup and the dropped same-note target id write, make counted add/remove one transaction, stop whole-vault reads on every writer call, and give the hand-edit clear path vault-snapshot recovery.

## Notes

[2026-10-03T05:38:49Z · bob-cli-3n.12.9.2] nav-writer-bugs done: DP29 blockquote refusal (reader not-a-line + gesture guards), kept-link id by line position with length-mismatch refusal, pendingTargetLine one-transaction commit, counted vault one-transaction batch with refuse-before-write, gated vault snapshots (adds/blocked-gated), hand-edit clear vault-snapshot recovery. Tests: npm test 1338 pass, validate 6/6, nav 1.60.0 deployed via bob plugins sync.

[2026-10-03T05:48:06Z · bob-cli-3n.12.9.2--1] PROPOSED FOLLOW-UP: completion::vault plugins_come_from_the_repo_checkout and task_sections_offer_exact_titles failed once under parallel just-run (empty stdout) then passed in isolation and on full just test rerun — possible test-parallelism flake worth a look

## Dependencies

- **Blocks:** [bob-cli-3n.12.9.3](bob-cli-3n.12.9.3.md) ◐ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3n.12.9.5](bob-cli-3n.12.9.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.2.md) | [bob-cli-3n.12.9.2](bob-cli-3n.12.9.2.md) | 0 |
