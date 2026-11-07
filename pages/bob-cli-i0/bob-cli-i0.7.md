# Bead: bob-cli-i0.7 — Docs refresh and real-terminal acceptance

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.7` · **Size:** small
**Created:** 2026-11-06 15:11:25 EST · **Closed:** 2026-11-06 17:42:19 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

docs-acceptance: rewrite docs/guides/install-everything.md around the new run, note the live line and BOB_INSTALL_VERBOSE in docs/start/install.md, pass `just docs-check`, capture real-Cargo PTY transcripts as bead attachments, and record the Mac verification and build-speed follow-ups.

## Notes

[2026-11-06T22:40:55Z · bob-cli-i0.7] Real Cargo just install PTY acceptance on Linux with TERM=xterm-256color and isolated CARGO_INSTALL_ROOT and BOB_INSTALL_STATE_DIR; exit 0. Attached transcript confirms the live status line and successful 1s incremental install.

[2026-11-06T22:40:59Z · bob-cli-i0.7] PROPOSED FOLLOW-UP: Verify install-all and Mac Capture acceptance on macOS — this Linux host cannot validate the macOS signing preflight, notification, or restart flow; capture a real Mac PTY transcript.

[2026-11-06T22:41:03Z · bob-cli-i0.7] PROPOSED FOLLOW-UP: Measure local-install build time on the supported Mac — this Linux host recorded 2m32s for the initial real Cargo build and 1s for the subsequent incremental install; compare cold and warm times on the 8 GB M1 target.

[2026-11-06T22:41:50Z · bob-cli-i0.7] WORKSPACE NOTE: A shell quoting mistake also ran just install once against the default Cargo root. It replaced the same-version binaries from this docs-only workspace; no Rust or install code changed.

[2026-11-06T22:42:05Z · bob-cli-i0.7] Real Cargo PTY acceptance on Linux, isolated install root and state; exit 0; live status line shown.

🔒 bob-cli-i0.7-cargo-pty-live.txt

[2026-11-06T22:42:19Z · bob-cli-i0.7] Updated both install docs for the pull-first digest, live status, ETA, logs, and verbose controls; just docs-check passed; attached successful real-Cargo PTY transcript and recorded macOS/build-time follow-ups.

## Attachments

- 🔒 bob-cli-i0.7-cargo-pty-live.txt · text/plain · 1.95801 KiB (private attachment)

## Dependencies

- **Depends on:** [bob-cli-i0.6](bob-cli-i0.6.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.7/README.md) | [bob-cli-i0.7](bob-cli-i0.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a435a8e`](https://github.com/bobs-org/bob-cli/commit/a435a8e134f0a92a99b3e4e45b8fa5ad6cbc763e) | docs(install): document live install flow | [bob-cli-i0.7](bob-cli-i0.7.md) | 2026-11-06 17:43:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-i0.7][1] | Verify the attached PTY transcript and phase follow-up records before closing | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.7/README.md

<!-- sase:referenced-by:end -->
