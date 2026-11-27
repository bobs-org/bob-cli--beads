# Bead: bob-cli-qp.8 — Switch Ref Cards on, docs, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.8` · **Size:** medium
**Created:** 2026-11-26 14:22:09 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-go-live: after bob-cli-qm.7 closes, delete the ref preview gate, extend the passive proof, and finish the docs in both repos. Apply only the accepted memory decisions, then deploy clean with provenance.

## Notes

[2026-11-26T21:29:29Z · bob-cli-qq.1] COORDINATION: cabinets kit adds the 240w* cabinet-owned gate/model/state/provider/collector, plus role-aware fold changes in 240s and state binding in 240r; later cabinets phases add gate-guarded hunks in 240o, 248m, and styles.css. Rendering and behavior remain current while cabinetsPreview is absent. Please keep these guarded hunks through go-live cleanup. Cabinets go-live waits for bob-cli-qm.7 and bob-cli-qp.8.

[2026-11-27T05:33:50Z · bob-cli-qp.8] GATE: bob-cli-qm.7 still IN_PROGRESS (itself gated on bob-cli-qj.4 IN_PROGRESS), so plan step 0 gate is unmet. Shared artifacts deferred; ref-owned work landed below UNCOMMITTED in WS13. No vault deploy ran: per plan the clean deploy follows qm.7, and a second agent is RUNNING (possible active deployer; sync refusal protocol applies). -r "Record ref go-live gate state, landed work, and remainder for the land agent"

[2026-11-27T05:34:02Z · bob-cli-qp.8] LANDED (uncommitted, bob-plugins WS13 linked repo): deleted 240u preview fragment + fragments.json line; 249s host no longer reads refCardPreview (eligible/livePath/isCurrent/setup/dispose); 374i preview exports removed; deleted preview-gate unit test + package.json entry; kit test now asserts active-host eligibility; passive suite extended with ref paint/fold/drawer entries and >=24 repaint assertion; e2e runner no longer writes refCardPreview into disposable vault, closed-gate flow removed, re-enable wait uses refNoteCardActive; e2e meta-test updated; ref-card.md admonition/gate text removed; manifest 1.172.1->1.172.2; main.js rebuilt; docs inventory regen (version only). bob-cli: ref.md Ref Card pointer; vault-format reference summary: (net-zero words); highlights-ref-sync note-side edit/marker write-back + protected-keys paragraph with props.md links; new glossary:ref-card strand + memory init regen (AGENTS.md/CLAUDE.md/README/glossary roster, docs/reference/glossary.md). -r "Record ref go-live landed file list for the land agent"

[2026-11-27T05:34:13Z · bob-cli-qp.8] VERIFY: npm run build + build:check exit 0; focused node --test 55+28+80 pass (passive, kit, editor, readouts, vocabulary, ref-library-report, ref acceptance meta incl. offline self-test, species, coordinator, cabinets-kit, plugin-build, cabinets meta, property-card host/ownership/fold/created/inventory); docs:inventory:check + just docs-gen exit 0. Cabinets guarded hunks untouched (no diff in 240o/240r/240s-fold/240w*/248m/styles.css). -r "Record ref go-live verification evidence"

[2026-11-27T05:34:19Z · bob-cli-qp.8] REMAINDER after qm.7 closes done: re-read glossary:property-card + architecture.md + property-editor.md as qm.7 left them; edit property-card strand (add Ref Card, props_v1 + == extension + H1 note); update architecture.md gate history, property-editor.md == fallback, ledger-tools + Reading Board docs, related-cards links; run npm run docs:check + full npm test; bob plugins sync from clean master + post-sync smoke + plugins-list no-drift; record SHAs/versions/evidence; close bead. PROPOSED FOLLOW-UP: docs/reference/vault-format.md lint budget 6030/6000 pre-existing on clean d9f57741 (unchanged by this phase); needs a ~30-word diet. -r "Record ref go-live remainder and follow-up for the land agent"

## Dependencies

- **Depends on:** [bob-cli-qp.7](bob-cli-qp.7.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.9](../bob-cli-qq/bob-cli-qq.9.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.8/README.md) | [bob-cli-qp.8](bob-cli-qp.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e32b95`](https://github.com/bobs-org/bob-cli/commit/0e32b956c2ed665a1043e965db1791a6f387fbef) | docs(ref): remove preview-gate docs and add ref-card glossary strand | [bob-cli-qp.8](bob-cli-qp.8.md) | 2026-11-27 00:35:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.7][1] | See whether go-live already started and what it expects from acceptance | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.7.md

<!-- sase:referenced-by:end -->
