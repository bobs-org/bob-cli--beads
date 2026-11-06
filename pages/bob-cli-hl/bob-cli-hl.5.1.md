# Bead: bob-cli-hl.5.1 — Complete Bob Mac Capture merge-in bands and pickers

[Bead Pages](../README.md) / [bob-cli-hl.5](bob-cli-hl.5.md) / bob-cli-hl.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.land`
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 15:58:07 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_merge_in_mac.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:d575f7782834af6068901dba | attached via sase artifact create --bead |
| related | file:explicit:dcacd48a80543ebadfdc52ad | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md

<!-- sase:links:end -->

## Description

Bob Mac Capture safely previews and submits new-task merge-in captures with source pickers, explicit rewrites, compact landing groups, and verified macOS behavior, completing bob-cli-hl.5.

## Notes

[2026-11-06T12:45:51Z · bob-cli-hl.5.1.land] LANDING TRIAGE (bob-cli-hl.5.1.land): PROPOSED FOLLOW-UP outcomes — (1) hl.5.1.2 #1 SimilarTasksBandView .mergeIn switch: declined, epic-caused and already fixed inside the epic by 6d659eb (SimilarTasksBandView.swift:343 handles .mergeIn; Build green since). (2) hl.5.1.4 #1, hl.5.1.5 #7, #9 baseline Mac keyboard/alias XCTest failures: +1 bob-cli-h7 (pre-epic master 6f4e279 run 42161345004 failed 16; post-epic a3e533b run 42216904060 repeats 13 of them, no new deterministic failures). (3) hl.5.1.5 #1 bob-cli README contract-table snapshot: +1 bob-cli-hs (reproduced on clean bob-cli 7825a98f; epic touched no bob-cli files). (4) hl.5.1.5 #2 regenerate clip-history directive fixtures on a Mac: declined — those capture --dry-run fixtures carry no grammar field, the grammar gate never applies to them, merge-in did not change their output, and directive-fixtures-README.md records their b8688d9e provenance; no test or behavior impact. Lander discoveries: +1 bob-cli-ge with post-gate-15 stale fixture counts (51 JSON fixtures at grammar 6/12/14 now below the gate; no failing test); new flake tasks bob-cli-hu (CaptureRelatedLaneTests rapid-edit debounce) and bob-cli-hv (CaptureRelationFlipAliasTests equals rewrite timeout), both failing on a3e533b run 42216904060 and passing on the identical tree 9225615 in run 42212293089. No --epic-symbol entries for bob-cli-hl.5.1 or bob-cli-hl.5.

[2026-11-06T20:57:50Z · 19a--1] Closeout complete on bob-mac-capture SHA cbb50dc909f61f6ce4aacae86b394d11b43e02d2 and bob-cli SHA 0869f7921a19b1e9b0e7e3bd6393f279d7d0567e. Portable-check and both sequential docs-checks passed; merge-in suites and 60 required 620/760 light/dark render views passed review. CI run 42278025697 has 12/28 failures matching the pre-epic 42161345004 baseline (16/33), owned by bob-cli-h7; bundle/install gates were skipped after Test. Evidence: file:explicit:dcacd48a80543ebadfdc52ad

[2026-11-06T20:58:07Z · 19a--1] Verified on bob-mac-capture cbb50dc909f61f6ce4aacae86b394d11b43e02d2: portable-check, both sequential docs-checks, all merge-in suites, and required render matrix pass review. The 12-test/28-assertion CI failure is an exact subset of pre-epic 42161345004 (16/33), owned by bob-cli-h7; bundle/install were skipped after Test. Report: file:explicit:dcacd48a80543ebadfdc52ad.

[2026-11-06T21:02:50Z · 19a--1] Final closeout report snapshot (including the corrected parent lifecycle record): file:explicit:d575f7782834af6068901dba. The .5.1 close also closed bob-cli-hl.5 as delegated work landed; because .5 remains assigned to bob-cli-hl.5, it was restored to in_progress with that ownership noted. bob-cli-hl remains in progress.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.land.md) | [bob-cli-hl.5.1](bob-cli-hl.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e9d3ae2`](https://github.com/bobs-org/bob-mac-capture/commit/e9d3ae2fdade28d031811b458c5f18633f38e023) | feat(capture): render merge-in bands and pending states | [bob-cli-hl.5.1](bob-cli-hl.5.1.md) | 2026-11-06 09:32:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.5.1.1][1] | Need parent epic plan decisions and scope | 1 |
| read-by | [agent:bob-cli-hl.5.1.2--1][2] | Need parent epic decisions and closeout requirements for its editor phase | 1 |
| read-by | [agent:bob-cli-hl.5.1.land--4][3] | Need the assigned landing phase requirements and closeout criteria | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.land.md

<!-- sase:referenced-by:end -->
