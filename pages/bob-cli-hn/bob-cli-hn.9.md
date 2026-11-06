# Bead: bob-cli-hn.9 — Mac Pull-In card verdict UI

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.9` · **Size:** large
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-06 11:13:07 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

mac-card: wire the outcome model into the Pull-In card (⌃X/⌃⇧X routing, inline reason field, glyphs, capsule, consequence strip, labels, two-step Esc, reopen on refusal with choices intact, VoiceOver actions), then update docs and gate on the exact-SHA macOS CI run.

## Notes

[2026-11-06T04:09:29Z · bob-cli-hn.9] PROPOSED FOLLOW-UP: docs-check offline lychee fails identically on clean base (task-merge index.html references missing capture#merging-tasks-into-a-new-task-with anchor); lint and build pass on both trees — existing docs link issue, not verdict UI scope

[2026-11-06T16:13:03Z · bob-cli-hn.9--2] PROPOSED FOLLOW-UP: residual macOS CI failures are the existing bob-cli-h7 / hu / hv cluster (9 separator + 2 comma + word-motion; related-lane debounce; equals-in-editor). Phase footer regression is gone. Clean-base run 42216904060: https://github.com/bobs-org/bob-mac-capture/actions/runs/42216904060. This snapshot SHA af178c4eebba4a63d0c2e8ab2a62720a1b9123b4 run: https://github.com/bobs-org/bob-mac-capture/actions/runs/42246543708. Do not create beads.

[2026-11-06T16:13:07Z · bob-cli-hn.9--2] Footer contract test now requests closeSupported:true (production default stays false). Offer-close refusals reopen the remembered card via routeContext?.pullInChoiceForBack and showReseededPullInChoice. Stale commit calls dismissPullInChoice so it never arms two-step Esc. Delayed stale-pick refresh clears isPreviewing. Tests cover staging/commit argv, reason editing, two-step Esc, stale/conflict/refused reopen, legacy stale-pick refresh, stale-guard dismiss (attributedDraft so Return hits commitPullInChoice), old-Bob gate, inbox-route verdict round-trip, router chords, and design renders; MoveThenPullIn seed counts non-empty capture-block seeds only. just portable-check exit 0. Mac scratch Scripts/bundle.sh + just typecheck-tests PASS (copy deleted). No docs/ changes. Snapshot SHA af178c4eebba4a63d0c2e8ab2a62720a1b9123b4 run https://github.com/bobs-org/bob-mac-capture/actions/runs/42246543708: Lint and Build passed; footer, stale-guard, seed, and all new verdict/inbox/router/design tests passed. Residual failures are the existing bob-cli-h7 / hu / hv cluster (9 CaptureSeparatorToggleTests + 2 comma CapturePanelModelTests + word-motion); related-lane debounce and equals-in-editor passed on this snapshot. Clean-base 42216904060 on a3e533b: https://github.com/bobs-org/bob-mac-capture/actions/runs/42216904060.

## Dependencies

- **Depends on:** [bob-cli-hn.8](bob-cli-hn.8.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.9.md) | [bob-cli-hn.9](bob-cli-hn.9.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6f4e279`](https://github.com/bobs-org/bob-mac-capture/commit/6f4e27990823b7174d5902f08f20f52c1390c53f) | feat(mac-capture): stage Done and Cancel verdicts on Pull-In card | [bob-cli-hn.9](bob-cli-hn.9.md) | 2026-11-05 23:14:41 EST |
| bob-mac-capture | [`bob-mac-capture@5b0dca6`](https://github.com/bobs-org/bob-mac-capture/commit/5b0dca60fbcc6695ed7a1dad77b27be01a9b3eb0) | fix(mac-capture): reopen Pull-In verdicts after offer-close refusal | [bob-cli-hn.9](bob-cli-hn.9.md) | 2026-11-06 11:14:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.9--2][1] | Read hn.9 before residual note, epic-symbols, and close | 2 |
| read-by | [agent:bob-cli-hn.land][2] | Need the child scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.9.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.land.md

<!-- sase:referenced-by:end -->
