# Bead: bob-cli-on.10.1.2 — Writer twin, cross-plugin copies, and the offer-close scope fix

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.2` · **Size:** medium
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 17:50:25 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

req-write-twin: port the drop/restore/toggle/insert writers (RW) into the cycler and pass every RW vector, copy the twin fragments byte for byte into nav and Block ID Prompt with a drift test, re-copy offer_close vectors, and make successorOfferCloseOpenScopeCount count only real #task subtasks.

## Notes

[2026-11-21T22:50:02Z · bob-cli-on.10.1.2] PROPOSED FOLLOW-UP: bob plugins sync still cannot deploy task-status-cycler or block-id-prompt without -F (corroborates bob-cli-on.10.1.1 note #2; now also blocks Block ID Prompt) — both vault stamps are clean at 726f9a5, a rebased-away commit that no longer exists, while the deployed bytes are in landed history (git log --find-object: cycler 1.52.0 main.js in 6e0d764, BIP 1.39.0 main.js in 3956368). bob-cli origin/master deploy.rs (6b9139a6) still applies find_inclusion_proof only to dirty stamps, so the documented "Landed" recipe refuses. This phase did not force (AGENTS.md); nav 2.102.0 is synced, but cycler 1.54.0 (RW twin + the user-visible offer-close scope fix) and BIP 1.41.0 (inert RQ twin) are NOT deployed. Fix bob-cli to apply the inclusion proof to clean stamps, then sync both.

[2026-11-21T22:50:07Z · bob-cli-on.10.1.2] PROPOSED FOLLOW-UP: offer-close project scope still diverges from bob-cli on #ref rows — the cycler project path (089h successorOfferCloseOpenScopeCount) counts top-level `- [ ] #ref …` reference rows via successorKeepMovingReferenceTasks, while bob-cli open_scope_count counts only parse_tasks (#task) rows. This phase made both paths exclude every req line (nested #ref reqs included), but a top-level #ref row still adds to "its N open tasks stay open" in Obsidian and not in bob-cli. Decide the intended rule in bob-cli, add an SV vector, and align the cycler.

[2026-11-21T22:50:25Z · bob-cli-on.10.1.2] req-write-twin done in bob-plugins (uncommitted at close; committed by this turn's final declaration). New pure cycler fragment 198-task-reqs-writers-twin.js mirrors bob-cli writers.rs: taskReqDrop(contents,{lineIndex,preimage},date,reason,options) / taskReqRestore / taskReqToggle / taskReqInsert return {ok:true,updated,…RW fields} or {ok:false,code,message} with bob-cli's exact codes and copy (req_stale preimage check first; toggle adds firstReq). writes.json copied byte for byte; test-task-status-cycler-task-reqs-vectors.cjs now runs every RQ/RL/RW case through shared drivers in scripts/task-reqs-vectors.cjs plus RW refusal-copy, firstReq, reason/log, final-newline/mixed-EOL, and custom-filter tests (144/144). Differential fuzz vs a temporary (reverted, never committed) bob-cli ignored test over drop_req/restore_req/toggle_note_req/insert_reqs: 41,000 random cases across 11 seeds (CRLF, mixed endings, no final newline, frontmatter, fences, quotes, ^prj, depth>16 chains, every mark, cancel logs, drawers incl. existing NOTES), 0 mismatches, every refusal code and every success path (created/prepended logs, depth-1 moves, scoop with NOTES birth, req->note into new and existing NOTES) hit. Copies: nav 694-698 (all five twins) + 728-task-reqs-exports.js, Block ID Prompt 165-166 (RQ) + 171-task-reqs-exports.js; fixtures copied (nav all four, BIP README+vectors). New scripts/test-task-reqs-twin-copies.cjs (in test:unit): byte-identical fragments (drift detection verified by a deliberate edit), manifest order before exports, bundles carry fragments verbatim, all fixture copies identical incl. ledger-tools vectors.json and bob-cli canonical, matching exported helper sets, and every RQ vector through nav and BIP bundles plus every RL/RW vector through nav (7/7). Offer-close: offer_close vectors.json already matched bob-cli (refreshed by 909b30f); plugin README now names SV25; successorOfferCloseOpenScopeCount subtask path counts only open whole-token #task lines within child_block_end_line (spaces/tabs indent), project path excludes every req line via taskReqForest; SV25 added to the canonical-copy test plus a req/#ref/paragraph scope test — both fail on the old code, pass now. Manifests: cycler 1.54.0, nav 2.102.0, BIP 1.41.0; docs:gen. Gates: npm run build + build:check clean, docs inventory current; npm test 8490/8495 pass, sole failure the known load flake test-ledger-tools-frees-marks.cjs:481 (passes 3/3 alone; also noted on bob-cli-on.10.1.1 and bob-cli-oj.5.1.x). npm run docs:check: every plugin-docs stage passes; it fails only in bob-cli master's own tools/docs/tests/test_contracts.py (registry 55 vs pinned 54, README digest), independent of bob-plugins and already recorded on bob-cli-on. Sync: nav 2.102.0 deployed and byte-identical to the repo; cycler and BIP refuse without -F (see PROPOSED FOLLOW-UP note; not forced). epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-on.10.1.1](bob-cli-on.10.1.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10.1.5](bob-cli-on.10.1.5.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md) | [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.7][1] | Check if its PROPOSED FOLLOW-UP already covers the abandoned 726f9a5 deploy blocking block-id-prompt and task-status-cycler sync | 1 |
| read-by | [agent:bob-cli-on.10.1.1][2] | Check sibling phase status | 1 |
| read-by | [agent:bob-cli-on.10.1.2][3] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md

<!-- sase:referenced-by:end -->
