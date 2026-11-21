# Bead: bob-cli-om.4 — Standalone modal prompts

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.4` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 13:44:58 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

modal-prompts: opt surfaces S2-S6, S12, and S13 into links with a correct sourcePath. Keep each host's guards, and close the Ctrl+[ gaps on these surfaces.

## Notes

[2026-11-21T18:44:28Z · bob-cli-om.4] PROPOSED FOLLOW-UP: sync nav 2.98.0 to the vault once bob-cli-om.5 lands — bob plugins sync refused nav because ws19 (bob-cli-om.5, still running) holds an uncommitted nav deploy at c4953d3 (18:13Z); waited 15 min, it did not land; no -F used. bob-mail 0.3.0 (S13) did deploy. om.5 must rebase onto this commit (both phases bumped nav to 2.98.0, so the later lander goes to 2.99.0) and sync nav from the rebased tree.

[2026-11-21T18:44:36Z · bob-cli-om.4] PROPOSED FOLLOW-UP: q should close S12 Notebook create and S13 Task from email when focus is on a button (decisions:q-and-ctrl-bracket-mirror-esc); this phase closed only the Ctrl+[ gaps the plan names — q still types in the fields, as required.

[2026-11-21T18:44:43Z · bob-cli-om.4] PROPOSED FOLLOW-UP: flaky perf budgets under machine load — test-ledger-tools-event-link-times.cjs ("perf — one build over a 200-link ledger stays under 25 ms") and test-ledger-tools-frees-marks.cjs ("200-link / 2000-task build stays within the 25 ms budget") failed at 245-610 ms inside full npm test with load average 120-167, and passed twice when rerun alone; ledger-tools untouched by this phase. docs:check word-budget failure (bob-navigation-hotkeys.md / plugin-apis.md) reproduces on the clean base, already noted on bob-cli-om.3.

[2026-11-21T18:44:58Z · bob-cli-om.4] Verified modal-prompts in bob-plugins: S2 Move to Next, S3 Release task, S4 batch Keep reason, S5 Rotten keep + decay-card Stay stage, S6 successor inline cancel reason pass links:true with sourcePath (shared task note / released note / shared entry note / keep entry or host filePath / row.notePath; mixed notes -> null); S12 Notebook Summary and S13 Task from email (bob-mail) attach proseField explicitly (recall null, sourcePath null, scope) with a band host under the field and fail open without nav. Host guards kept (Alt+F swallow, decay chord-release/repeat paths, S6 350ms Enter guard + blur commit; S13 Enter still submits nothing). Ctrl+[ gaps closed on S4/S5/S6/S12/S13 after the band layer. S6 parks draft, caret, and band handle across renderResults and rebinds; clicks inside the editor no longer toggle the row. Fixed om.3 gap: logRecall.attach(links) passed no plugin, so every keystroke rebuilt the link index and leaked listeners — index now cached on nav plugin instance. Tests: new test-navigation-prose-modal-prompts.cjs (9, real controller, capture-order DOM, keymap Esc layering) + S6 case in successor-verdicts; 258 affected tests green; full npm test green except 2 load-flaky ledger-tools perf budgets (pass alone); build:check, validate, docs:inventory:check green; docs:check word budget fails identically on clean base. Manifests nav 2.98.0, bob-mail 0.3.0; docs updated (nav prompts section, notebook-gestures, bob-mail). bob-mail synced; nav sync refused by om.5 unlanded dirty deploy (follow-up noted). link_text=path; no memory edits.

## Dependencies

- **Blocks:** [bob-cli-om.10](bob-cli-om.10.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.3](bob-cli-om.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.4/README.md) | [bob-cli-om.4](bob-cli-om.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@24bc9cc`](https://github.com/bobs-org/bob-plugins/commit/24bc9cc6f87df9366afe17d121503cdb5a47408d) | feat(nav): wire \[\[ completion into the standalone modal prompts | [bob-cli-om.4](bob-cli-om.4.md) | 2026-11-21 14:03:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-oo.1][2] | Need to know if om.4 still owns workspace 10 ledger-tools deploy | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.1/README.md

<!-- sase:referenced-by:end -->
