# Bead: bob-cli-om.3 — proseField controller, LINK band, and the Work summary pilot

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.3` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 12:27:56 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

link-band: build the two-mode proseField controller and the LINK band (rendering, CSS, keyboard contract, undo-safe insertion, a11y, unresolved-link hint) and api.proseField v1. Pilot it on block-id-prompt's Work summary prompt (S1) and verify undo, IME, and Esc layering in real Obsidian.

## Notes

[2026-11-21T17:27:28Z · bob-cli-om.3] PROPOSED FOLLOW-UP: vault sync of block-id-prompt 1.40.0 (S1 links:true) was refused — bob-cli_13 still stamps a dirty 1.39.2 deploy from 2026-11-21T14:34:23Z (source_head 3860513, title-block walkthrough); nav 2.97.0 did deploy. Do not -F; sync 1.40.0 once that stamp clears. Current ws 13 occupant is bob-cli-oo.1 (different epic).

[2026-11-21T17:27:40Z · bob-cli-om.3] PROPOSED FOLLOW-UP: npm run docs:check lint already exceeds word budgets on origin for plugin-apis.md, bob-navigation-hotkeys.md, and vault-format.md; this phase added a short proseField/S1 section to the first two. Reproduces on the clean tree.

[2026-11-21T17:27:56Z · bob-cli-om.3] Verified link-band: api.proseField v1 wraps attachLogRecall at call time (480 stays at cap via 727 re-export); LINK band CSS/ARIA/keyboard (IME→link→recall→host, Esc/q/Ctrl+[, Enter/Tab accept, zero-row Enter closes, dismissal memory); undo-safe insertText; S1 Work summary attach links:true with sourcePath (task-link-open → target.path else source.sourcePath). Tests: test-navigation-link-engine.cjs (vectors+index), test-navigation-prose-field.cjs, S1 work-log, R9 10k-note keystroke best CPU ≤8ms and first-build best-of ≤40ms (inbound now O(edges); headings/blocks lazy), preview-link-band --self-test, obsidian-prose-field-e2e --self-test. Live Obsidian binary absent (UNDO-GAP). Fragments 189/189a/189b/727 ≤1000 lines. Manifests nav 2.97.0 / bip 1.40.0. docs:inventory:check green. No leftover --epic-symbol. bob plugins sync deployed nav 2.97.0; bip 1.40.0 refused (see follow-up). link_text=path; no decision-record edits.

## Dependencies

- **Depends on:** [bob-cli-om.2](bob-cli-om.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.4](bob-cli-om.4.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.5](bob-cli-om.5.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.6](bob-cli-om.6.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.7](bob-cli-om.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.3/README.md) | [bob-cli-om.3](bob-cli-om.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@79fe2e1`](https://github.com/bobs-org/bob-plugins/commit/79fe2e15e25956aa913944d97cb8605f5ad65ad6) | feat(nav): add proseField LINK band and Work summary \[\[ pilot | [bob-cli-om.3](bob-cli-om.3.md) | 2026-11-21 12:31:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.3][1] | Need the phase scope, notes, and design file before continuing implementation | 6 |
| read-by | [agent:bob-cli-om.4][2] | Need prior phase notes on proseField API | 1 |
| read-by | [agent:bob-cli-om.5][3] | Need link-band phase notes for the proseField API I build on | 1 |
| read-by | [agent:bob-cli-om.6][4] | See link-band phase notes about real-Obsidian spike results and blur/rebind behavior | 1 |
| read-by | [agent:bob-cli-oo.1][5] | Need om.3 status because vault stamp still names its dirty workspace 10 deploy | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.6/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.1/README.md

<!-- sase:referenced-by:end -->
