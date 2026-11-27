# Bead: bob-cli-q5.6 — Alt+Z Snooze Card and Task Card z

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.6` · **Size:** large
**Created:** 2026-11-25 10:22:53 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

snooze-card: the Alt+Z command and Task Card z opening a Snooze Card with ranked time suggestions, a consequence footer, retime/Wake now/Unsnooze on snoozed tasks, teaching refusals for Event and Blocked tasks, and a pure JS planner pinned to the shared vectors.

## Notes

[2026-11-27T13:54:37Z · bob-cli-q5.6.1.land--1] CLOSEOUT STATUS (2026-11-27): implementation source bases: bob-cli eef6cc07 (docs/snooze.md modified) and bob-plugins 56baeb9 (Snooze changes in working tree), with upstream at 852b1c69. Verification: plugin build:check and docs:inventory:check pass; docs:check passes (447 tests, 1 expected skip). Earlier Snooze checks: 43 focused tests, 26 performance checks, and live Obsidian E2E 56 assertions pass; report and all 8 inspected screenshots are attached to bob-cli-q5.6.1 note #3. Broad npm test remains red from existing /tmp ENOSPC self-test fixtures and two timing-sensitive thresholds. This turn just check exits 101 on the known unrelated native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words kicker-width assertion (bob-cli-q9 triage). symvision is not listed as a Just recipe. Deployment: prior bob-navigation-hotkeys copy is preserved; full dry-run reports 0 copies, 31 unchanged, 1 refusal. bob-ledger-tools 1.172.5 remains protected from workspace 11 at 56baeb9; fetched upstream has no commit with the exact deployed bundle bytes. No force was used. Earlier land triage is recorded and resolved in bob-cli-q5.6.1 note #2. Closeout is pending a decision on the unlanded protected ledger build.

## Dependencies

- **Depends on:** [bob-cli-q5.5](bob-cli-q5.5.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.9](bob-cli-q5.9.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.md) | [bob-cli-q5.6](bob-cli-q5.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.6.1.land][1] | Need the parent phase scope for the landing tale closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.1.land.md

<!-- sase:referenced-by:end -->
