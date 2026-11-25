# Bead: bob-cli-q4.8.1 — Vector-pinned taskSettle provider for ledger-tools

[Bead Pages](../README.md) / [bob-cli-q4.8](bob-cli-q4.8.md) / bob-cli-q4.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) · **Assignee:** `bob-cli-q4.8.1.land`
**Created:** 2026-11-25 10:27:08 EST · **Closed:** 2026-11-25 14:20:05 EST
**Plan:** [202611/task\_settle\_twin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_settle_twin.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:985ff95df01c3b7cda7a1c8c | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q4.8 with a Rust-parity pure JS settle transform, guarded editor application, and a shared idle scheduler behind the versioned taskSettle API.

## Notes

[2026-11-25T18:49:10Z · bob-cli-q4.8.1.land] FOLLOW-UP TRIAGE COMPLETE: .1 #1 and .2 #1 (ten cycler test failures) declined as already fixed by bob-plugins abbac5ac, which updates stale NOTES expectations to the shipped bold Notes writer contract; affected files passed the lander targeted run. .1 #3 and .2 #2 (frees-mark timing flake) declined as already fixed by 84ba9d41 CPU-time measurement; targeted test passed. .1 #2, .3 #1, and .3 #2 docs proposals consolidated: corroborated existing bob-cli-jz for unchanged navigation 6068/6000 and bob-cli-ob for pre-existing plugin-apis 9287/8000 advisory. Own API growth to 9961 and ledger reference growth/integration to 6012 remain in the repair tale, not external follow-ups. The .3 #2 capture-syntax 6011/6000 finding is caused by 22fea308 and 8a1d16a6; recorded DISCOVERED ISSUE on active bob-cli-ph.6.1 for its .5 acceptance phase. No new task beads were necessary; all seven PROPOSED FOLLOW-UP entries have a disposition.

[2026-11-25T18:52:39Z · bob-cli-q4.8.1.land] LAND REVIEW: Read the epic, all three child beads and every note, the child and parent plans, relevant decisions, actual Rust and JS settle/model/grouping/editor/scheduler code, and epic commits 5c0f8160 (CLI), 824d8e49/f764a4be/c9454208/abbac5ac/84ba9d41 (plugins). Targeted settle, cycler and frees tests pass; npm run build:check passed all nine plugins. Direct cmp confirms canonical README/vectors match, but the copy test computes sase/tests instead of tests and silently skips in this linked layout. Confirmed guard defects: missing supplied blockId falls through to an arbitrary hinted line, allowing a deleted-task pending settle to write; staged contents without expected overwrite authored live text. Scratch-vault real Obsidian cursor-leave probe passed, ruling out the suspected update-listener restriction. Evidence and exact reproducer: file:explicit:985ff95df01c3b7cda7a1c8c. Post-start review through CLI e6eb52a1/plugins 84ba9d41 found no pure Rust/vector changes (08a708d3 adds a writer wrapper); concurrent drawer/property-card/settings work needs no provider wiring changes. Documentation integration remains: taskSettle API growth plus concurrent drawer reference addition exceeds budgets. A validated medium tale covers only guards, actual copy validation, own docs growth, final just check/deployment, this epic close, plan done, and normal parent phase q4.8 close. No memory edits; stay cursor preserved. Both q4.8.1 and q4.8 epic-symbol queries are empty; symvision recipe absent on reviewed tree. Epic and parent remain open pending repairs; just check has not yet run in this landing.

[2026-11-25T19:20:05Z · bob-cli-q4.8.1.land] CLOSEOUT: taskSettle identity and staged-preimage guards landed; bob-ledger-tools 1.161.0 deployed from this checkout.

Guards: supplied blockId is authoritative (unique match wins; absent or duplicate unresolved; never falls through to a line hint or text). Without blockId, exact text at the hinted line or an unambiguous exact-text match is required. A line number alone is never identity. Staged applyToEditor contents require an explicit matching expected preimage; missing or mismatched expected returns idle reason "preimage" with no cursor/scroll/history writes. Current-buffer calls that omit contents still work without expected.

Canonical fixtures: scripts/task-settle-vectors.cjs walks up to 12 parents for tests/fixtures/task_settle; a linked checkout under /sase/repos/linked/ fails if the canonical dir is missing. test-ledger-tools-task-settle-copies.cjs ran against the real canonical files (linked lookup, byte-identical, README instruction) rather than skipping.

Verification: npm test 9542 pass / 4 skip / 0 fail; test:perf 26 pass; build:check included. Identity/preimage/pending/copy suites pass. test:e2e:task-settle-undo pass with refusal {stagedApplied:false, stagedReason:"preimage", stagedUnchanged:true, pendingScheduled:true, flushApplied:false, afterFlushUnchanged:true}. Docs: ledger-tools 5994/6000; plugin-apis 9276 (≤9287 baseline, 8000 advisory warning remains); new develop/task-settle.md 733 words. docs:check with BOB_CLI_DIR=this checkout failed only on independently reproduced pre-existing budgets: capture-syntax 6011/6000 (bob-cli-ph.6.1 DISCOVERED ISSUE) and bob-navigation-hotkeys 6068/6000 (bob-cli-jz). just check on clean bob-cli e6eb52a1 failed 3 lib + 18 cli tests, all capture/drawer/meetings/hooks on unchanged Rust (catalog spelling #"REQUIREMENTS" vs #requirements, merge **REQUIREMENTS** drawer, wispr PDF word stability, capture fixture line drift, task_status_hooks open-chip count); not provider scope. justfile still has no symvision recipe. epic-symbols bob-cli-q4.8.1: none.

Integration: post-start CLI 08a708d3 writer wrapper only; later capture/snooze/docs commits do not change the pure settle algorithm. Plugin drawer/property-card/settings commits after 84ba9d41 need no new taskSettle consumers. Frozen v1 lookup app.plugins.plugins["bob-ledger-tools"]?.api?.taskSettle with settleNote/applyToEditor/schedulePending/flushPending. Decisions stay: settle_cursor=stay, o_in_group=intake_end, wasm_spike=yes, memory_settle_record=no. WASM research and gesture-consumer wiring remain on containing bob-cli-q4.

Follow-up dispositions (lander, not duplicated): .1#1/.2#1 declined (abbac5ac Notes cycler); .1#3/.2#2 declined (84ba9d41 frees-mark CPU); .1#2/.3#1/.3#2 corroborated bob-cli-jz and bob-cli-ob; capture-syntax assigned to bob-cli-ph.6.1.

Deploy: bob plugins sync --repo this linked checkout --no-pull -p bob-ledger-tools (no -F). Vault manifest/main.js/styles.css byte-identical to tested source; vault version 1.161.0.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.1.land.md) | [bob-cli-q4.8.1](bob-cli-q4.8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@01ac184`](https://github.com/bobs-org/bob-plugins/commit/01ac18405e4a8c03b848796c4d7475fb1a44dc1f) | fix(ledger-tools): make taskSettle identity and staged preimages strict | [bob-cli-q4.8.1](bob-cli-q4.8.1.md) | 2026-11-25 14:22:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.8.1.1][1] | need parent epic scope | 1 |
| read-by | [agent:bob-cli-q4.8.1.2][2] | Need parent epic DECISIONS and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.2/README.md

<!-- sase:referenced-by:end -->
