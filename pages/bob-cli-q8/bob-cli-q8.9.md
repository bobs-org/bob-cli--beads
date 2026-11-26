# Bead: bob-cli-q8.9 — Bob Mac Capture tie capsules and report rows

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.9` · **Size:** medium
**Created:** 2026-11-25 18:16:43 EST · **Closed:** 2026-11-25 22:53:47 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

mac-tie-capsules: decode the new capture and capture-complete fields, render the tie capsules, summaries, and report rows, refresh the fixtures and docs, and watch the exact-SHA macOS CI run to green.

## Notes

[2026-11-26T02:58:07Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: bob-cli master has pre-existing docs generated drift (docs/reference/glossary.md missing the q8.3 task-relation sentence; plugin inventory stale for docs/bob-ledger-tools.md and docs/index.md), so mac-capture just docs-check fails its generated-drift stage on the clean base too; bob-docs lint passes with the q8.9 docs. Needs a bob-cli docs-gen + bob-plugins sync pass.

[2026-11-26T02:58:23Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: portable-check on athena shows 12 pre-existing drawer-casing failures (CapturePlaceMenuPresentationTests, CaptureSubBulletPresentationTests, CaptureModelTests.testCaptureSuccessDecodesDrawerObject) that reproduce identically on untouched origin/master; true-case drawer annotation vs test expectations.

[2026-11-26T03:20:57Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: macOS CI and portable-check show pre-existing drawer-casing failures (CapturePlaceMenuPresentationTests, CaptureSubBulletPresentationTests, CaptureModelTests.testCaptureSuccessDecodesDrawerObject) reproducing identically on untouched origin/master; tracked by epic bob-cli-ph.8.1 (true-case drawers), not this bead.

[2026-11-26T03:53:17Z · bob-cli-q8.9] PROPOSED FOLLOW-UP: Mac-side convert keys in the pickers (chord/Enter conversion of tied pairs, mirroring the nav Ctrl-chord and armed-release work in bob-cli-q8.6 through q8.8) are out of scope for this phase.

[2026-11-26T03:53:47Z · bob-cli-q8.9] Tie capsules, summaries, and report rows land in 797313af. Verified: portable-check on athena (my 4 suites pass; 12 drawer failures reproduce identically on clean base, tracked by ph.8.1), macOS scratch build + typecheck-tests pass, bob-docs lint ok, macos-ci-check gate (Lint/Build green; Test fails only on the pre-existing drawer set), pushed, exact-SHA master run 45749289760 shows Lint/Build green with 169 tie-suite tests passing and only 2 pre-existing drawer-casing failures remaining. bob-cli generated drift and Mac convert keys recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-q8.3](bob-cli-q8.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q8.4](bob-cli-q8.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.9/README.md) | [bob-cli-q8.9](bob-cli-q8.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@797313a`](https://github.com/bobs-org/bob-mac-capture/commit/797313af29aea3378e83d2b56234200271e77702) | feat(mac-capture): decode tie fields and render tie capsules and report rows | [bob-cli-q8.9](bob-cli-q8.9.md) | 2026-11-25 22:29:54 EST |
