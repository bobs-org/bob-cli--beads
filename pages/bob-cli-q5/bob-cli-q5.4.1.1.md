# Bead: bob-cli-q5.4.1.1 — Shared JavaScript snooze row, clock, and cleanup model

[Bead Pages](../README.md) / [bob-cli-q5.4.1](bob-cli-q5.4.1.md) / bob-cli-q5.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) · **Assignee:** `bob-cli-q5.4.1.1` · **Size:** medium
**Created:** 2026-11-26 07:52:01 EST · **Closed:** 2026-11-26 08:34:50 EST
**Plan:** [202611/snooze\_plugin\_plumbing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_plugin_plumbing.md)

## Description

snooze-core: implement the pure snooze parser, injected-zone time resolver, classifier, explicit row-removal planner and state-prune planner in bob-ledger-tools; execute the canonical rows/when/live/cleanup vectors and establish verified source twins for the independently deployed gesture plugins.

## Notes

[2026-11-26T13:31:00Z · bob-cli-q5.4.1.1--1] PROPOSED FOLLOW-UP: Fix the Obsidian frontmatter takeover self-test — the clean base at 0d0a31f6 reproduces the modal visibility and focus assertions at obsidian-frontmatter-takeover-e2e-lib.cjs:1063; this phase does not modify that test or harness.

[2026-11-26T13:34:50Z · bob-cli-q5.4.1.1--1] Verified snooze-core completion: validate passed; npm test reported 9,874 passed, 4 skipped, and one failure in obsidian-frontmatter-takeover-e2e (--self-test), reproduced identically on clean base 0d0a31f6 and recorded as PROPOSED FOLLOW-UP; docs:check passed (447 passed, 1 skipped). bob plugins sync --repo <linked checkout> --no-pull copied 6 plugins; post-sync dry-run confirmed 0 copies, 0 skipped, 34 unchanged. Epic symbols: none.

[2026-11-26T13:35:58Z · bob-cli-q5.4.1.1--1] PROPOSED FOLLOW-UP: Resolve the bob-emoji vault Git tracking warning — bob plugins sync reports four tracked files under .obsidian/plugins/bob-emoji; assess the vault ignore/index cleanup across hosts before changing it.

## Dependencies

- **Blocks:** [bob-cli-q5.4.1.2](bob-cli-q5.4.1.2.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.1.md) | [bob-cli-q5.4.1.1](bob-cli-q5.4.1.1.md) | 0 |
