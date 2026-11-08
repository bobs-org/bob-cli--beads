# Bead: bob-cli-ii.3.1.2 — Paged discovery and bounded run coordination

[Bead Pages](../README.md) / [bob-cli-ii.3.1](bob-cli-ii.3.1.md) / bob-cli-ii.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.md) · **Assignee:** `bob-cli-ii.3.1.2` · **Size:** medium
**Created:** 2026-11-07 18:12:56 EST · **Closed:** 2026-11-07 19:51:59 EST
**Plan:** [202611/gmail\_sync\_filing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_filing.md)

## Description

discovery: implement ids-only discovery, per-account exclusion, and shared pacing and transient retry support, preserving dry-run and watch-only behavior.

## Notes

[2026-11-08T00:51:59Z · bob-cli-ii.3.1.2] discovery done and verified: paged ids-only discovery (dedupe, 5k cap, repeated-token guard), per-account guard on shared -r budget, paced bounded-backoff retry with auth abort; fake-gog page/per-thread/transient controls. just check green (5594 lib tests, all integration binaries, clippy, fmt); epic-symbols empty

## Dependencies

- **Depends on:** [bob-cli-ii.3.1.1](bob-cli-ii.3.1.1.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.3.1.3](bob-cli-ii.3.1.3.md) ◐ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.3.1.4](bob-cli-ii.3.1.4.md) ◐ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.1.2.md) | [bob-cli-ii.3.1.2](bob-cli-ii.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`39122cb`](https://github.com/bobs-org/bob-cli/commit/39122cb23010bb464047bcc586eacc5baf514f71) | feat(gmail): add sync discovery, guard, and retry helpers | [bob-cli-ii.3.1.2](bob-cli-ii.3.1.2.md) | 2026-11-07 20:09:20 EST |
