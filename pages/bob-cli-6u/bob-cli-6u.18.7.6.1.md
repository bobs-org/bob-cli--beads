# Bead: bob-cli-6u.18.7.6.1 — Reconcile PDR7 warning, exact close-path ^prj, capture output and docs fixes

[Bead Pages](../README.md) / [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) / bob-cli-6u.18.7.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.1` · **Size:** medium
**Created:** 2026-10-12 22:09:27 EDT · **Closed:** 2026-10-12 22:35:27 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

## Description

cli-fixes: restore the PDR7 warning for internal Depends-On line links, match ^prj exactly in the close paths, keep removal fields out of the nested link_guard object, test consumed @r:id human output, use the configured-open check in + rendering, restore lost PDB4/PDB6 and CRLF coverage, and correct docs/capture.md.

## Notes

[2026-10-13T02:35:13Z · bob-cli-6u.18.7.6.1] PROPOSED FOLLOW-UP: Investigate the two percent-listen failures in just check (failed_percent_listen_worker_keeps_listen_retry_guidance and percent_listen_reference_runs_existing_worker_and_installs_audio), already tracked by bob-cli-6m.

[2026-10-13T02:35:27Z · bob-cli-6u.18.7.6.1] Implemented PDR7 Depends-On line warnings with deduplication; exact prj matching in close paths; top-level-only capture cleanup fields; accurate consumed @r:id human and JSON output; configured-open project rendering; restored CRLF, PDB4, PDB6, and fenced-index coverage; and corrected docs/capture.md. Verified epic-symbols has no leftovers and git diff --check passes. just check completed formatting and clippy; 2,454 library tests and 1,414 CLI tests passed. Its only failures were the two percent-listen tests tracked by bob-cli-6m, which I recorded as a PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.6.4](bob-cli-6u.18.7.6.4.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.1/README.md) | [bob-cli-6u.18.7.6.1](bob-cli-6u.18.7.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2fcf41a`](https://github.com/bobs-org/bob-cli/commit/2fcf41a2c0bc144ce2f752d154b01f32a4cfb7e9) | fix(project-blocking): reconcile capture and close edge cases | [bob-cli-6u.18.7.6.1](bob-cli-6u.18.7.6.1.md) | 2026-10-12 22:37:03 EDT |
