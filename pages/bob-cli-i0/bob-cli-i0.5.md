# Bead: bob-cli-i0.5 — Route builds and plugin sync through the live line

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.5` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 17:00:58 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

quiet-builds: run the bob-cli Cargo build (in `just install`) and the Mac Capture install (after a TTY signing preflight) through the live runner with a started-file fallback. Quiet the plugin sync per DECISIONS plugin_diffs, add install-all -v/--verbose and BOB_INSTALL_VERBOSE, make Ctrl-C stop the run cleanly, and extend the end-to-end tests.

## Notes

[2026-11-06T22:00:58Z · bob-cli-i0.5] Implemented live Cargo and SwiftPM routing, verbose passthrough, logged plugin sync, TTY signing preflight, interrupt handling, and timed sync/restart history. Verified with 21 install-all tests, 16 live-runner tests, 7 portability tests, bash -n, Justfile help forwarding, and git diff --check; epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-i0.3](bob-cli-i0.3.md) ✓ · ⧖ 2026-11-06
- **Depends on:** [bob-cli-i0.4](bob-cli-i0.4.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.6](bob-cli-i0.6.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.5/README.md) | [bob-cli-i0.5](bob-cli-i0.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d5e49b1`](https://github.com/bobs-org/bob-cli/commit/d5e49b172c9299ec6bbb60cc866aa29025e426f5) | feat(install): route builds through the live runner | [bob-cli-i0.5](bob-cli-i0.5.md) | 2026-11-06 17:02:10 EST |
