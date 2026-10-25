# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.3 — Decide and implement bob ref doctor for id and duplicate checks

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.3` · **Size:** medium
**Created:** 2026-10-25 10:04:06 EDT · **Closed:** 2026-10-25 10:34:42 EDT
**Plan:** [202610/backlog\_batch10\_port\_help\_doctor\_mermaid\_startpending.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md)

## Description

ref-doctor-identity: resolve bob-cli-b8 by making a local implement or decline decision first, then flagging id/stem mismatches and duplicate ids with live-vault repair or closing as canceled with the decision recorded.

## Notes

[2026-10-25T14:34:19Z · bob-cli-an.6.6.6.5.6.5.5.6.6.3] Decision: IMPLEMENT (not decline). b8 doctor scope is warranted: creation-time fix (9885bde1) stopped new bad ids but live vault still carries exactly the reported 1 duplicate id + 3 stem mismatches; rename already supports same-stem id repair (id_updated), so only the diagnostics were missing.

[2026-10-25T14:34:24Z · bob-cli-an.6.6.6.5.6.5.5.6.6.3] Baseline (read-only live scan): duplicate id BryanBugyi_CV_extended x2 notes; mismatches ref/papers/harness_engineering.md (id harness_engineering_2), ref/chat/obsidian_sync_footprint_audit_bob-cli-1l.md, ref/papers/BryanBugyi_CV_extended_v2.md. Matches b8 description exactly.

[2026-10-25T14:34:27Z · bob-cli-an.6.6.6.5.6.5.5.6.6.3] Fix: ref index now emits id_stem_mismatch + duplicate_ref_id diagnostics (notes without ids exempt); doctor prints a reference ids warn row naming the bob ref rename repair; docs/highlights-ref-sync.md documents the row. Repair verified on temp vaults: scan -w + rename <REF> <stem> yields id_updated and a clean doctor row (mismatch and duplicate cases). No live-vault edits made; b8 left open for the lander to run the live repairs and close.

[2026-10-25T14:34:31Z · bob-cli-an.6.6.6.5.6.5.5.6.6.3] Verification: 3 new doctor_library tests (ok/warn/repair) pass; full doctor_library (15), ref_library lib (88) + cli (132) suites green; just check exit 0; just docs-check passed. Live repair of the 4 real notes NOT done here per no-live-vault-edits rule.

[2026-10-25T14:34:42Z · bob-cli-an.6.6.6.5.6.5.5.6.6.3] Implemented bob ref doctor reference-id diagnostics: index emits id_stem_mismatch and duplicate_ref_id, doctor prints a reference ids warn row naming the bob ref rename repair. Verified: 3 new doctor_library tests pass, ref_library suites green (88+132), just check exit 0, docs-check passed, read-only live scan confirms the exact b8 scope (1 duplicate id + 3 mismatches). No live-vault edits; b8 live repair + close left for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8994514`](https://github.com/bobs-org/bob-cli/commit/89945148d2ed4f051e6d969cfc0f4bd6d66ed40d) | feat(ref-doctor): flag id/stem mismatches and duplicate ids with rename repair | [bob-cli-an.6.6.6.5.6.5.5.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.3.md) | 2026-10-25 10:35:51 EDT |
