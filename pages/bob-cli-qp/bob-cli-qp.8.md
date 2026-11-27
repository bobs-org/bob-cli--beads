# Bead: bob-cli-qp.8 — Switch Ref Cards on, docs, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.8` · **Size:** medium
**Created:** 2026-11-26 14:22:09 EST · **Closed:** 2026-11-27 07:59:15 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-go-live: after bob-cli-qm.7 closes, delete the ref preview gate, extend the passive proof, and finish the docs in both repos. Apply only the accepted memory decisions, then deploy clean with provenance.

## Notes

[2026-11-26T21:29:29Z · bob-cli-qq.1] COORDINATION: cabinets kit adds the 240w* cabinet-owned gate/model/state/provider/collector, plus role-aware fold changes in 240s and state binding in 240r; later cabinets phases add gate-guarded hunks in 240o, 248m, and styles.css. Rendering and behavior remain current while cabinetsPreview is absent. Please keep these guarded hunks through go-live cleanup. Cabinets go-live waits for bob-cli-qm.7 and bob-cli-qp.8.

[2026-11-27T05:33:50Z · bob-cli-qp.8] GATE: bob-cli-qm.7 still IN_PROGRESS (itself gated on bob-cli-qj.4 IN_PROGRESS), so plan step 0 gate is unmet. Shared artifacts deferred; ref-owned work landed below UNCOMMITTED in WS13. No vault deploy ran: per plan the clean deploy follows qm.7, and a second agent is RUNNING (possible active deployer; sync refusal protocol applies). -r "Record ref go-live gate state, landed work, and remainder for the land agent"

[2026-11-27T05:34:02Z · bob-cli-qp.8] LANDED (uncommitted, bob-plugins WS13 linked repo): deleted 240u preview fragment + fragments.json line; 249s host no longer reads refCardPreview (eligible/livePath/isCurrent/setup/dispose); 374i preview exports removed; deleted preview-gate unit test + package.json entry; kit test now asserts active-host eligibility; passive suite extended with ref paint/fold/drawer entries and >=24 repaint assertion; e2e runner no longer writes refCardPreview into disposable vault, closed-gate flow removed, re-enable wait uses refNoteCardActive; e2e meta-test updated; ref-card.md admonition/gate text removed; manifest 1.172.1->1.172.2; main.js rebuilt; docs inventory regen (version only). bob-cli: ref.md Ref Card pointer; vault-format reference summary: (net-zero words); highlights-ref-sync note-side edit/marker write-back + protected-keys paragraph with props.md links; new glossary:ref-card strand + memory init regen (AGENTS.md/CLAUDE.md/README/glossary roster, docs/reference/glossary.md). -r "Record ref go-live landed file list for the land agent"

[2026-11-27T05:34:13Z · bob-cli-qp.8] VERIFY: npm run build + build:check exit 0; focused node --test 55+28+80 pass (passive, kit, editor, readouts, vocabulary, ref-library-report, ref acceptance meta incl. offline self-test, species, coordinator, cabinets-kit, plugin-build, cabinets meta, property-card host/ownership/fold/created/inventory); docs:inventory:check + just docs-gen exit 0. Cabinets guarded hunks untouched (no diff in 240o/240r/240s-fold/240w*/248m/styles.css). -r "Record ref go-live verification evidence"

[2026-11-27T05:34:19Z · bob-cli-qp.8] REMAINDER after qm.7 closes done: re-read glossary:property-card + architecture.md + property-editor.md as qm.7 left them; edit property-card strand (add Ref Card, props_v1 + == extension + H1 note); update architecture.md gate history, property-editor.md == fallback, ledger-tools + Reading Board docs, related-cards links; run npm run docs:check + full npm test; bob plugins sync from clean master + post-sync smoke + plugins-list no-drift; record SHAs/versions/evidence; close bead. PROPOSED FOLLOW-UP: docs/reference/vault-format.md lint budget 6030/6000 pre-existing on clean d9f57741 (unchanged by this phase); needs a ~30-word diet. -r "Record ref go-live remainder and follow-up for the land agent"

[2026-11-27T10:43:26Z · bob-cli-qp.8] GATE (run 2, 2026-11-27T10:45Z): bob-cli-qm.7 still IN_PROGRESS (waits on bob-cli-qj.4, IN_PROGRESS). The earlier ref-owned work is committed on master: bob-plugins 4410a5bf (gate removed, bob-ledger-tools 1.172.2) and bob-cli 0e32b956. In the vault, bob-ledger-tools is still 1.172.1, deployed 05:02Z from an uncommitted WS13 build on bd1af860 (the qp.7 repair build, later committed as 2bd92b19). It still has the ref gate and no data.json, so Ref Cards are OFF in the live vault. bob plugins list shows drift on block-id-prompt, bob-ledger-tools, and bob-navigation-hotkeys. Caveat: master has no gate now, so any bob plugins sync from master by any agent turns Ref Cards on before qm.7 closes. The note #5 remainder fits one coder once the gate opens, so no child epic. Monitoring qm.7 under the gate procedure until about 2026-11-30T05:30Z (72h from the first gate check). -r Record ref go-live gate recheck, vault deploy state, and wait plan for the land agent

[2026-11-27T12:57:27Z · bob-cli-qp.8--1] GO-LIVE PROVENANCE (run 3, gate opened: bob-cli-qm.7 closed done 2026-11-27T12:13:54Z). Ref gate removal already on bob-plugins master as 4410a5bf (ancestor of 56baeb9f); bob-cli 0e32b956 carries ref.md/vault-format/highlights-ref-sync and glossary:ref-card (kept as is; matches shipped behavior). This run, on bases bob-cli eef6cc07 and bob-plugins 56baeb9f44ca51df41a8a0fb00889c83d2510e28 (docs only, committed by this turn's finalizer): bob-plugins docs/property-editor.md (== on refs: Reference editor under props_ref_contract_v1, else title focus-or-add, plus a Reference settings row), docs/develop/architecture.md (Ref in props_v1-alone list, == extension, matching-H1 hiding, cardPreviewKinds/refCardPreview gate history), docs/bob-ledger-tools.md (cards list gains Notebook/Prose/Ref links; Areas paragraph dieted to stay 5992/6000 words), docs/area-and-project-cards.md + docs/ref-card.md related-cards links; bob-cli docs/ref.md Reading Board kind vocabulary now cites the shared ref vocabulary + Ref Card; glossary:property-card edited per memory_property_card only (family gains [[ref-card]], props_v1 + == extension, matching first H1). -r "Record ref go-live completion evidence and follow-ups for the land agent"

[2026-11-27T12:57:37Z · bob-cli-qp.8--1] VERIFY + DEPLOY: sase memory init, just docs-gen, just docs-check PASS (bob-cli); npm run docs:check PASS, npm run build:check PASS (bob-plugins); full npm test unit 10237 pass / 0 fail / 5 skip, perf 25/1 where the lone failure (taskLinks typed keystrokes p95 16.45 ms > 12 ms at load avg ~93) passed on isolated rerun 26/26 (11.01 ms), already tracked by bob-cli-pg. apollo vault: bob plugins sync from the bob-cli root (default checkout, clean 56baeb9f, no -F, no refusal; the prior ws12 dirty deploy was proven by c41e07e9) copied bob-ledger-tools manifest+main.js and bob-navigation-hotkeys main.js; bob plugins list -f json ok=true count=12 synced=12 drift=0, every plugin clean at 56baeb9f; deployed bundle has 0 refCardPreview/cardPreviewKinds hits and no bob-ledger-tools data.json, so Ref Cards are live. athena vault (ssh, read-only): synced=12 drift=0, bob-ledger-tools 1.172.4 clean at 56baeb9f. LIMITATION, not a pass: the Obsidian startup smoke cannot run on apollo (no Obsidian or Xvfb installed); the identical 56baeb9f bundles passed qm.7's isolated and deployed-vault smokes on athena (bob-cli-qm.7 note #9). Versions: bob-ledger-tools 1.172.4, bob-navigation-hotkeys 2.107.13, block-id-prompt 1.46.0, bob-articles 0.4.0, bob-chips 0.16.0, bob-command-mode 0.6.0, bob-emoji 0.2.0, bob-mail 0.3.0, bob-project-tasks 1.2.0, bob-vim-surround 1.5.2, bob-vim-yank-flash 0.1.1, task-status-cycler 1.64.2. Ref acceptance evidence (qp.7 GO 54/54): file:explicit:71e7c7a55117ffd98b5fec4b (report), file:explicit:65cd84a81d3610f4285ddd5c (run+build log), file:explicit:4f6ec6de1f7e3ef296d67c86 (screenshots). Test logs: ~/.cache/sase/tmp/qp8/ on apollo. -r "Record ref go-live completion evidence and follow-ups for the land agent"

[2026-11-27T12:57:44Z · bob-cli-qp.8--1] RESOLVED (supersedes the note #5 PROPOSED FOLLOW-UP): docs/reference/vault-format.md now counts 5969/6000 budget words on bob-cli eef6cc07 and just docs-check passes, so no word-budget diet is needed. -r "Record ref go-live completion evidence and follow-ups for the land agent"

[2026-11-27T12:58:01Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F1 retype or re-home the 13 root *_ref hub notes — they get no Ref Card today; Bryan decides whether they become typed hubs or move (plan:202611/ref_cards.md Follow-ups). -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:08Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F2 Reading Board consumes the shared ref-library snapshot — 241 still spawns its own bob ref list -s ready,next,wip; reuse the 241a/241ak report service the Ref Card already shares. -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:16Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F3 dock the reading-task embed into the Ref Card — only if screenshots show the duplicated lane hurts and a safe cross-note lane writer exists; today the embed stays visible below the card. -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:23Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F4 bob-supplied reading-time/page estimates and an agent-report Bottom line excerpt — add them as additive bob ref list fields, then patch existing card slots. -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:31Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F5 code-block and link counts on the Ref Card — derive them from the saved-source catalog, not by reading the note or PDF at paint time. -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:39Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F6 bob ref retitle — one previewed cross-note write covering title:, the matching H1, and the reading task's link alias, which the Reference editor's Title row would then use. -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:58:53Z · bob-cli-qp.8--1] PROPOSED FOLLOW-UP: F7 make the kit's hardcoded species lists descriptor-driven from 240f — the 240m silent-created set and the 240q kinds/attributes lists; safe now that both qm and qp go-lives landed (cabinets bob-cli-qq.9 still edits nearby hunks). -r "Record ref-cards plan follow-ups F1-F7 for land-agent triage"

[2026-11-27T12:59:15Z · bob-cli-qp.8--1] Ref go-live complete after qm.7 closed done: gate removed on master (4410a5bf, deployed via 56baeb9f), docs in both repos updated (property-editor == on ref

… and 536 more characters

## Dependencies

- **Depends on:** [bob-cli-qp.7](bob-cli-qp.7.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.9](../bob-cli-qq/bob-cli-qq.9.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.8.md) | [bob-cli-qp.8](bob-cli-qp.8.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e32b95`](https://github.com/bobs-org/bob-cli/commit/0e32b956c2ed665a1043e965db1791a6f387fbef) | docs(ref): remove preview-gate docs and add ref-card glossary strand | [bob-cli-qp.8](bob-cli-qp.8.md) | 2026-11-27 00:35:37 EST |
| bob-plugins | [`bob-plugins@4410a5b`](https://github.com/bobs-org/bob-plugins/commit/4410a5bf20505e468f3672a73b7eaece0c22a7c8) | feat(ref): remove ref-card preview gate and extend passive coverage | [bob-cli-qp.8](bob-cli-qp.8.md) | 2026-11-27 00:36:13 EST |
| bob-cli | [`7666118`](https://github.com/bobs-org/bob-cli/commit/7666118c640875cdcbc380f0a9accb249e63abd8) | docs(ref): finish Ref Card go-live docs and property-card glossary | [bob-cli-qp.8](bob-cli-qp.8.md) | 2026-11-27 08:00:47 EST |
| bob-plugins | [`bob-plugins@546ecfa`](https://github.com/bobs-org/bob-plugins/commit/546ecfa5c382bddeaaed1658cef24c61d9a0bd54) | docs(ref-card): document the live Ref Card across plugin docs | [bob-cli-qp.8](bob-cli-qp.8.md) | 2026-11-27 08:01:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.7][1] | See whether go-live already started and what it expects from acceptance | 1 |
| read-by | [agent:bob-cli-qp.8][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-qp.8--1][2] | Need the phase scope, design file, notes, and epic decisions to finish ref go-live | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.7.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.8.md

<!-- sase:referenced-by:end -->
