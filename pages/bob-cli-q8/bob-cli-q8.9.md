# Bead: bob-cli-q8.9 — Bob Mac Capture tie capsules and report rows

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.9

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.9` · **Size:** medium
**Created:** 2026-11-25 18:16:43 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

mac-tie-capsules: decode the new capture and capture-complete fields, render the tie capsules, summaries, and report rows, refresh the fixtures and docs, and watch the exact-SHA macOS CI run to green.

## Notes

[2026-11-26T02:58:07Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: bob-cli master has pre-existing docs generated drift (docs/reference/glossary.md missing the q8.3 task-relation sentence; plugin inventory stale for docs/bob-ledger-tools.md and docs/index.md), so mac-capture just docs-check fails its generated-drift stage on the clean base too; bob-docs lint passes with the q8.9 docs. Needs a bob-cli docs-gen + bob-plugins sync pass.

[2026-11-26T02:58:23Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: portable-check on athena shows 12 pre-existing drawer-casing failures (CapturePlaceMenuPresentationTests, CaptureSubBulletPresentationTests, CaptureModelTests.testCaptureSuccessDecodesDrawerObject) that reproduce identically on untouched origin/master; true-case drawer annotation vs test expectations.

[2026-11-26T03:20:57Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: macOS CI and portable-check show pre-existing drawer-casing failures (CapturePlaceMenuPresentationTests, CaptureSubBulletPresentationTests, CaptureModelTests.testCaptureSuccessDecodesDrawerObject) reproducing identically on untouched origin/master; tracked by epic bob-cli-ph.8.1 (true-case drawers), not this bead.

## Dependencies

- **Depends on:** [bob-cli-q8.3](bob-cli-q8.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q8.4](bob-cli-q8.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.9/README.md) | [bob-cli-q8.9](bob-cli-q8.9.md) | 0 |
