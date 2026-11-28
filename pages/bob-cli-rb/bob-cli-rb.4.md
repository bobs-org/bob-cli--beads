# Bead: bob-cli-rb.4 — Mac inserts the lead undoably, peels it with one Backspace, skips it on ⌘↩

[Bead Pages](../README.md) / [bob-cli-rb](README.md) / bob-cli-rb.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.4` · **Size:** medium
**Created:** 2026-11-27 15:03:21 EST · **Closed:** 2026-11-27 20:33:08 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

## Description

mac_lead_accept: apply a lead-bearing accept as two native undo groups bound to the response snapshot, arm a one-key Backspace peel, skip the lead on Control/Command- Return, update keyboard and panel docs, add hosted tests, and watch macOS CI green.

## Notes

[2026-11-28T01:33:08Z · bob-cli-rb.4--4] Verified two-step native lead accept: applying a lead-bearing accept inserts the type-lead marker and the lead as two native undo groups bound to the response snapshot. TypeLeadPeel Backspace peels the lead in one key. Control-Return and Command-Return skip the lead. Hosted tests cover accept, peel, skip-lead, and the undo-group split. closeUndoGroupAfter runs on the marker edit only, so marker, lead, and peel are separate ⌘Z steps without leaving an empty group that eats undo.

Gates: just portable-check 2925 passed / 1 skipped / 0 failures; just docs-check under the 6000-word cap; Mac scratch bundle.sh plus just typecheck-tests on the Swift sources.

Meeting-notes flake: testOutOfOrderPreviewCannotReplaceNewEventSelection now asserts an order-independent Set of event tokens {old#^event, new#^event}; the generation guard still holds.

macos-ci-check green on snapshot SHA 15c7423d628b65702e61c81f1a5fa06f6ae63c06 (identical tree to bob-mac-capture HEAD 6c545f23). Workflow https://github.com/bobs-org/bob-mac-capture/actions/runs/46091145714: Lint, Build, Test, Bundle, Verify plist and signature, Launch smoke test, Install and reinstall all passed. Parent epic bob-cli-rb stays open.

## Dependencies

- **Depends on:** [bob-cli-rb.3](bob-cli-rb.3.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rb.5](bob-cli-rb.5.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.4.md) | [bob-cli-rb.4](bob-cli-rb.4.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e83e9c`](https://github.com/bobs-org/bob-mac-capture/commit/1e83e9ce1bc1482648ed761af26175880b3c52b6) | feat(capture): insert task type leads as two native undo groups | [bob-cli-rb.4](bob-cli-rb.4.md) | 2026-11-27 18:23:44 EST |
| bob-mac-capture | [`bob-mac-capture@4192581`](https://github.com/bobs-org/bob-mac-capture/commit/4192581edaa73d079bf081a2d82c806b852cb3df) | feat(capture): insert task type leads as two native undo groups | [bob-cli-rb.4](bob-cli-rb.4.md) | 2026-11-27 19:01:25 EST |
| bob-mac-capture | [`bob-mac-capture@de954c5`](https://github.com/bobs-org/bob-mac-capture/commit/de954c51e3d38d7363e776f2bc409f9aadcc4bbe) | feat(capture): insert task type leads as two native undo groups | [bob-cli-rb.4](bob-cli-rb.4.md) | 2026-11-27 19:35:20 EST |
| bob-mac-capture | [`bob-mac-capture@6c545f2`](https://github.com/bobs-org/bob-mac-capture/commit/6c545f23be23ab47d2546d7aab419da231533fce) | test(meetings): ignore preview request order in out-of-order selection | [bob-cli-rb.4](bob-cli-rb.4.md) | 2026-11-27 20:02:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rb.4--1][1] | Need the phase scope, notes, and design after CI Test failure | 2 |
| read-by | [agent:bob-cli-rb.4--2][1] | Need phase bead status, notes, and follow-up before fixing CI | 1 |
| read-by | [agent:bob-cli-rb.4--3][1] | Need phase bead status, notes, and remaining work after macos-ci-check failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.4.md

<!-- sase:referenced-by:end -->
