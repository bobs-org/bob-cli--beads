# Bead: bob-cli-ac.4 — release-plz train in git\_only rehearsal mode

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Assignee:** `bob-cli-ac.4` · **Size:** medium
**Created:** 2026-10-20 18:36:53 EDT · **Closed:** 2026-10-20 22:53:57 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

## Description

train: add release-plz.toml, the tested daily guard, release.yml (plan, CI, release, preview, optional binaries), and just release-preview, and validate them with release-plz locally and a dry run on GitHub.

## Notes

[2026-10-21T02:53:57Z · bob-cli-ac.4] Train landed: release-plz.toml (git_only rehearsal, git_tag_name v{{version}}, Breaking/Added/Fixed/Performance/Reverted groups; docs+refactor skipped as non-user-visible, protect_breaking keeps docs!/refactor!), tools/release/train_guard.py + 48-test suite, release.yml (schedule/dispatch/push, plan/ci/release/preview/binaries), Cargo binstall metadata, just release-preview (pinned 0.3.173). Verified: 48 unit tests pass, actionlint clean on ci+release, release-plz scratch clones T1 clean at 0.2.0 / T2 feat+docs->0.2.1 Added no chore(release) / T3 docs-only no bump / T4 feat!->0.3.0 Breaking (0.x: breaking=minor, feat=patch), GitHub dry run https://github.com/bobs-org/bob-cli/actions/runs/39534493209 plan success + CI full green (lint/package/ubuntu/macos) + preview success with guard SKIP unarmed rehearsal and release/binaries correctly skipped, just package-check 7.79 MiB pass, epic-symbols none.

## Dependencies

- **Depends on:** [bob-cli-ac.3](bob-cli-ac.3.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ac.5](bob-cli-ac.5.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ac.6](bob-cli-ac.6.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.4/README.md) | [bob-cli-ac.4](bob-cli-ac.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`104cee9`](https://github.com/bobs-org/bob-cli/commit/104cee99cdbc8471e854b2c610413f5b941185d8) | feat(train): release-plz rehearsal train with daily guard | [bob-cli-ac.4](bob-cli-ac.4.md) | 2026-10-20 22:55:29 EDT |
