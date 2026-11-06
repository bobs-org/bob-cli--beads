# Bead: bob-cli-i0.4 — Pull everything first, print the digest, end with a signal

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.4` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 16:09:11 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

pull-first-run: restructure scripts/install_all to pull all three repos up front, show aligned pull rows in the header, carry full SHAs across the self-re-exec (with the legacy upgrade path), print the digest, and advance sibling watermarks. It also drops the nested INSTALL banner and adds the bell and macOS completion banner. Includes an end-to-end sandbox harness.

## Notes

[2026-11-06T21:09:11Z · bob-cli-i0.4] pull-first-run landed: header pulls all repos with aligned rows, protocol-2 re-exec with full SHAs plus legacy DETAIL fallback, digest with record, sibling watermarks, BOB_INSTALL_ALL=1 handling in just install, bell plus quiet macOS banner. Verified: 12 new sandbox tests in tests/test_install_all.py pass; just check-scripts fully green (99 install_ui tests OK); sase bead epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-i0.2](bob-cli-i0.2.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.5](bob-cli-i0.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.4/README.md) | [bob-cli-i0.4](bob-cli-i0.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ade2d6`](https://github.com/bobs-org/bob-cli/commit/9ade2d64ac64a5935512501890d550224f592940) | feat(install): pull everything first, print the digest, end with a signal | [bob-cli-i0.4](bob-cli-i0.4.md) | 2026-11-06 16:10:16 EST |
