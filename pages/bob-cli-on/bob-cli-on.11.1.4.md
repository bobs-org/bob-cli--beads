# Bead: bob-cli-on.11.1.4 — Apply requirement carry and drop verdicts with guarded Undo

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.4` · **Size:** medium
**Created:** 2026-11-22 14:59:31 EST · **Closed:** 2026-11-22 16:43:40 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

req_apply: build the cycler carry/drop service using the navigation carry API and existing requirement writers, preserving preimages, receipts, move maps, and one guarded Undo.

## Notes

[2026-11-22T21:43:40Z · bob-cli-on.11.1.4] Verified req_apply: cycler carry/drop apply service plus nav notice v6 Undo adapter.

Tests: npm test in bob-plugins 8773 pass / 0 fail / 4 skipped; perf 17/17. Focused RV20–RV28 exact bytes via planReqCloseWrites + injected taskSplitPlanCarryReq; carry_pulled refused without pullInPreflight (req_pull_in_unavailable); unavailable taskSplit refuses carry (split_unavailable) and never uses ordinary split; Met writes nothing; compose restores earliest-before→final-after including created inbox.md; dirty-editor/dest-change stale (req_close_stale); partial live carry reports failures and never claims the unapplied row; post-close [x] owner still carries open reqs. Twin-copy parity still only reqClose*/REQ_CLOSE_* names (198c/d stay cycler-only). Notice v6: req-only Undo, mixed Undo closes, legacy payloads unchanged.

Deploy: bob plugins sync --repo $PWD --no-pull -p task-status-cycler then -p bob-navigation-hotkeys from bob-cli_15 dirty 289c7f6. Cycler vault stamp rewritten from abandoned bob-cli_16 dirty 538d421 via clean origin sync first (bytes already matched 4d4c73c). No -F.

Apply-service seam for close_wiring:
- Cycler (not public plugin.api): planReqCloseWrites({ notes, owners, requests, today, date, sha256Hex, planCarryReq, pullInPreflight?, expectedNotes?, expectedOwnerPostimages?, inboxRoute? }) and mixin applyReqCloseWrites (same plus optional live carryReq/taskSplit/persistDrop/cache/context). Mixin is installed; not advertised on cycler.api.
- notes = post-close live snapshot; owners = frozen pre-close forest from reqCloseCollectOwners. Carry bottom-to-top then drops. Met writes nothing.
- Live carry uses nav api.taskSplit.carryReq({ notePath, line (1-based), expectedLine, expectedOwnerPreimage, today? }); never ordinary split. carry_pulled refused until pullInPreflight (req_delivery).
- Success: { ok: true, req_outcomes/outcomes, met, postimages, restores, notes, jump }. restores { path, before, after, created } composed earliest-before→final-after, including created notes.
- Refusal: { ok: false, code, message } with req_close_stale, split_unavailable, req_pull_in_unavailable. Live persist may also { ok: false, failures: [{ key, code, message, path }] }.
- Nav notice v6: model req_outcomes / req_met plus undo.restores and __noticePlugin. Feature-detect api.notice?.version >= 6. 654 restoreGuardedSnapshots refuses if any postimage changed; created files delete on undo. Keep owner Done on card-verdict undo.

## Dependencies

- **Depends on:** [bob-cli-on.11.1.1](bob-cli-on.11.1.1.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-on.11.1.2](bob-cli-on.11.1.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.11.1.5](bob-cli-on.11.1.5.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md) | [bob-cli-on.11.1.4](bob-cli-on.11.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.4][1] | Confirm phase closed before final declaration | 10 |
| read-by | [agent:bob-cli-on.11.1.5][2] | need req_apply completion evidence and published seam for req_delivery | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.5/README.md

<!-- sase:referenced-by:end -->
