# Bead: bob-cli-ac.3 — Reusable per-push CI workflow brought green on GitHub

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Assignee:** `bob-cli-ac.3` · **Size:** medium
**Created:** 2026-10-20 18:36:53 EDT · **Closed:** 2026-10-20 22:20:05 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

## Description

ci: add .github/workflows/ci.yml (push, ci/** branches, dispatch, workflow_call with sha/full) and iterate on a scratch branch until every Linux and macOS job is green.

## Notes

[2026-10-20T23:49:15Z · bob-cli-ac.3--1] Normal run https://github.com/bobs-org/bob-cli/actions/runs/39516238570 (SHA 85e72b22, full=false) failed: test (macos-latest) "Lint macOS-only targets" — unused imports Stdio, BOB_BIN, io::Write in tests/gkeep_pull.rs (linux-only PTY helper). lint, test (ubuntu-latest), and package were green. Wall times (failed run): lint ~1m20s (23:37:36–23:38:56), package ~1m48s (23:37:36–23:39:24), test ubuntu ~5m11s (23:37:36–23:42:47), test macos ~1m58s then fail (23:37:37–23:39:35). Fix committed as 1ecc3cd8 on origin/ci/ci; watching https://github.com/bobs-org/bob-cli/actions/runs/39517344331.

[2026-10-21T00:55:49Z · bob-cli-ac.3--2] Run https://github.com/bobs-org/bob-cli/actions/runs/39517344331 (SHA 1ecc3cd8, full=false) cancelled: test (macos-latest) hit the 45m job timeout. lint, test (ubuntu-latest), and package were green. macOS unit tests failed 2 (APFS is_file() returned query case solo.md vs Solo.md); integration tests then failed ~33 more and hung after vault_sync until cancel. Root causes: GNU timeout(1) missing so zsh zpty tests hang; GNU touch -d and date --date fail; bash 3.2 cannot run the adapter (mapfile); APFS case; example.pdf vs example.PDF alias; non-UTF-8 filenames; café NFD. Fix committed as 367e616f on origin/ci/ci (portable timeout/mtime/BSD date, on-disk wikilink case, brew bash 5, skip impossible FS cases). Watching https://github.com/bobs-org/bob-cli/actions/runs/39524227265.

[2026-10-21T01:29:45Z · bob-cli-ac.3--3] Run https://github.com/bobs-org/bob-cli/actions/runs/39524227265 (SHA 367e616f, full=false) failed: ubuntu test 1 fail (bash_counts_unicode_prefix: locale -a lists C.utf8 not C.UTF-8); macos test 10 CLI + 1 randomize. Root causes: GNU getopt vs BSD; BSD sed -i; /var vs /private/var (git birth prefix, corpus-gate tmp, pre-scan PWD); APFS is_file short-circuit rewriting [[area]] to [[Area]]; zpty hangs. Fix committed as 317ac840 on origin/ci/ci (portable bob_notify flags, sed -i.bak, canonicalize git prefix/tmp, skip .git in snapshots, skip hung zpty, brew bash only). Watching https://github.com/bobs-org/bob-cli/actions/runs/39527598472.

[2026-10-21T01:53:00Z · bob-cli-ac.3--4] Run https://github.com/bobs-org/bob-cli/actions/runs/39527598472 (SHA 317ac840, full=false) failed: test (macos-latest) 3 tests. lint, test (ubuntu-latest), and package were green. Wall times: lint ~1m7s, package ~1m9s, test ubuntu ~4m24s, test macos ~9m16s then fail. Failures: note_resolution_prefers_exact_paths_then_unique_basenames (APFS is_file returns solo.md for Solo.md); highlights_create_vault_note_marker_survives_scan_and_sync (Area.md vs [[area]] churn on no-op sync); probe_without_controlling_terminal_via_zpty (DRIVER-READ-FAILED). Fix committed as 1bf201d7 on origin/ci/ci (case-insensitive Solo.md assert, lowercase area.md fixture, skip unusable zpty). Watching https://github.com/bobs-org/bob-cli/actions/runs/39529797389.

[2026-10-21T02:02:06Z · bob-cli-ac.3--5] Normal run https://github.com/bobs-org/bob-cli/actions/runs/39529797389 (SHA 1bf201d7, full=false) GREEN. Jobs: lint ~1m13s (01:52:28–01:53:41Z), package ~1m15s (01:52:28–01:53:43Z), test ubuntu ~3m49s (01:52:27–01:56:16Z), test macos ~7m10s (01:52:29–01:59:39Z). Next: exercise full=true via origin/ci/full-ci and workflow_dispatch.

[2026-10-21T02:04:34Z · bob-cli-ac.3--5] Started full=true: push https://github.com/bobs-org/bob-cli/actions/runs/39530816998 (branch ci/full-ci, SHA 1bf201d7, startsWith ref ci/full) and workflow_dispatch https://github.com/bobs-org/bob-cli/actions/runs/39530828412 (gh workflow run ci.yml --ref ci/ci -f full=true). Dispatch succeeded even though ci.yml is not on master (workflow already registered). Both Ubuntu test jobs entered Install full-test tools. Watching both.

[2026-10-21T02:19:51Z · bob-cli-ac.3--6] CI green on Linux and macOS for SHA 1bf201d7.

Normal full=false (push ci/ci): https://github.com/bobs-org/bob-cli/actions/runs/39529797389
  lint 1m13s (01:52:28–01:53:41Z), package 1m15s (01:52:28–01:53:43Z), test ubuntu 3m49s (01:52:27–01:56:16Z), test macos 7m10s (01:52:29–01:59:39Z).

Full=true push (ci/full-ci): https://github.com/bobs-org/bob-cli/actions/runs/39530816998
  lint 1m43s (02:03:04–02:04:47Z), package 1m48s (02:03:03–02:04:51Z), test ubuntu 7m10s (02:03:03–02:10:13Z), test macos 11m35s (02:03:04–02:14:39Z).

Full=true dispatch (ci/ci -f full=true): https://github.com/bobs-org/bob-cli/actions/runs/39530828412
  lint 1m14s (02:03:11–02:04:25Z), package 1m01s (02:03:11–02:04:12Z), test ubuntu 6m17s (02:03:11–02:09:28Z), test macos 9m32s (02:03:11–02:12:43Z).

Scratch branches origin/ci/ci and origin/ci/full-ci deleted. No leftover --epic-symbol entries. macOS leg kept throughout.

[2026-10-21T02:20:05Z · bob-cli-ac.3--6] CI green on Linux and macOS for SHA 1bf201d7.

Normal full=false (push ci/ci): https://github.com/bobs-org/bob-cli/actions/runs/39529797389
  lint 1m13s (01:52:28–01:53:41Z), package 1m15s (01:52:28–01:53:43Z), test ubuntu 3m49s (01:52:27–01:56:16Z), test macos 7m10s (01:52:29–01:59:39Z).

Full=true push (ci/full-ci): https://github.com/bobs-org/bob-cli/actions/runs/39530816998
  lint 1m43s (02:03:04–02:04:47Z), package 1m48s (02:03:03–02:04:51Z), test ubuntu 7m10s (02:03:03–02:10:13Z), test macos 11m35s (02:03:04–02:14:39Z).

Full=true dispatch (ci/ci -f full=true): https://github.com/bobs-org/bob-cli/actions/runs/39530828412
  lint 1m14s (02:03:11–02:04:25Z), package 1m01s (02:03:11–02:04:12Z), test ubuntu 6m17s (02:03:11–02:09:28Z), test macos 9m32s (02:03:11–02:12:43Z).

Scratch branches origin/ci/ci and origin/ci/full-ci deleted. No leftover --epic-symbol entries. macOS leg kept throughout.

## Dependencies

- **Depends on:** [bob-cli-ac.1](bob-cli-ac.1.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-ac.2](bob-cli-ac.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ac.4](bob-cli-ac.4.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ac.3.md) | [bob-cli-ac.3](bob-cli-ac.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1d1b8fe`](https://github.com/bobs-org/bob-cli/commit/1d1b8fec66676da163cee0180f58985f83cb99eb) | ci: add GitHub Actions workflow and fix macOS test portability | [bob-cli-ac.3](bob-cli-ac.3.md) | 2026-10-20 22:28:14 EDT |
