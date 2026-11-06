# Bead: bob-cli-hl.5 — Bob Mac Capture merge-in band and pickers

[Bead Pages](../README.md) / [bob-cli-hl](README.md) / bob-cli-hl.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.190](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.190.md) · **Assignee:** `bob-cli-hl.5` · **Size:** large
**Created:** 2026-11-05 18:05:40 EST · **Closed:** 2026-11-06 16:29:30 EST
**Plan:** [202611/capture\_merge\_in\_arrow.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_arrow.md)

## Previously Closed

> ↺ Closed 2026-11-06T20:58:07Z · done
>
> delegated work landed
>
> Reopened 2026-11-06T20:59:52Z by `sase bead open`

## Description

mac: render the Merging-in band inside the new-task card, pending and refusal states with rewrite buttons, merge-in pickers, folded landing groups, submit/status/notification/VoiceOver copy, and raise the grammar gate.

## Notes

[2026-11-06T06:46:07Z · bob-cli-hl.5] Planning audit: bob-cli 248a2bfa already contains the CLI merge-in implementation and dependency phases are closed. Linked bob-mac-capture 6f4e279 is clean, has transfer infrastructure but no merge_in support, and still gates at grammar 5. No earlier phase notes or epic-symbol exemptions were present. Authored and validated a five-phase medium-sized child epic covering wire fixtures, editor pickers/rewrites, bands/copy, landing folds, and gate/docs/integration; its land agent owns closing bob-cli-hl.5 after verification. No product or memory files changed.

[2026-11-06T21:01:01Z · 19a--1] Restored after the .5.1 close automatically closed this parent. Parent lifecycle remains assigned to bob-cli-hl.5 per the approved closeout instruction; its lander should decide closure.

[2026-11-06T21:29:30Z · bob-cli-hl.land] Verified by the bob-cli-hl land agent: the whole mac phase was delegated to child epic bob-cli-hl.5.1, which is closed with all five phases closed (wire decode/fixtures, pickers and rewrite buttons, band and copy, origin folds, grammar gate). bob-mac-capture origin/master cbb50dc contains CaptureCore/CaptureMergeInPresentation.swift (band header 'Merging in N', footer 'Capture & merge N', VoiceOver/notification copy), BobMacCapture/CaptureMergeInBandView.swift rendered from CapturePanelView, and CaptureGrammarGate.minimumRevision = 15 with blockedMessage 'Update bob to merge tasks with <'. Exact-SHA evidence (file:explicit:dcacd48a80543ebadfdc52ad, file:explicit:d575f7782834af6068901dba): CI run 42278025697 passed Build and every merge-in suite; its 12 failing tests are an exact subset of pre-epic baseline run 42161345004 owned by bob-cli-h7; portable-check and both repos' docs-check passed; 60 required light/dark render views reviewed. hl.5.1 lander triaged all child proposals (h7, hs, ge, hu, hv; declined the .mergeIn switch and clip-history fixtures). 19a--1 had reopened this phase only to leave closure to its owner; no hl.5 agent is running, so the epic lander closes it. No --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-hl.3](bob-cli-hl.3.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hl.4](bob-cli-hl.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) | [bob-cli-hl.5](bob-cli-hl.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.5.1.1][1] | Need epic DECISIONS for phase work | 1 |
| read-by | [agent:bob-cli-hl.5.1.land--4][2] | Need epic phase clauses for completion check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.land.md

<!-- sase:referenced-by:end -->
