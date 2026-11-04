# Bead: bob-cli-h3.2 — bob-mac-capture: Command-X toggle in the Go To picker

[Bead Pages](../README.md) / [bob-cli-h3](README.md) / bob-cli-h3.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.180](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.180.md) · **Assignee:** `bob-cli-h3.2` · **Size:** medium
**Created:** 2026-11-04 11:50:53 EST · **Closed:** 2026-11-04 13:02:26 EST
**Plan:** [202611/goto\_completed\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/goto_completed_toggle.md)

## Description

mac: route Command-X in the Go To picker to a refetch with --closed-tasks, render a trailing Completed section, degrade on older bob, and update tests and docs.

## Notes

[2026-11-04T18:00:01Z · bob-cli-h3.2--1] PROPOSED FOLLOW-UP: Refresh the Bob CLI generated decisions page — Bob Mac Capture docs-check at Bob CLI master a6c55cb passes lint but reports docs/develop/decisions.md out of date. Historical bob-cli-b6 was resolved earlier, so this appears to be recurring generated drift; regenerate the page in bob-cli and rerun docs-check.

[2026-11-04T18:02:26Z · bob-cli-h3.2--1] Verified: just portable-check passes on this Linux host (2,100 tests, 1 skipped, 0 failures); changed Swift lines have no formatter warnings, and git diff --check is clean. just docs-check passes lint but reports docs/develop/decisions.md stale in Bob CLI master a6c55cb; recorded a proposed follow-up. macOS targets remain unverified because the Mac SSH attempt timed out.

## Dependencies

- **Depends on:** [bob-cli-h3.1](bob-cli-h3.1.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h3.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h3.2.md) | [bob-cli-h3.2](bob-cli-h3.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@78df1c9`](https://github.com/bobs-org/bob-mac-capture/commit/78df1c9173a91b754949d648a9a96bbd2a8f3bd8) | feat(capture): toggle completed tasks in Go To picker | [bob-cli-h3.2](bob-cli-h3.2.md) | 2026-11-04 13:03:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h3.2--1][1] | Confirm the docs drift follow-up note is recorded before closing the verified phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h3.2.md

<!-- sase:referenced-by:end -->
