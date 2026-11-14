# Bead: bob-cli-lm.2 — Nav family b — four commands, repeat tables, selector letter, landing, toast, vimrc

[Bead Pages](../README.md) / [bob-cli-lm](README.md) / bob-cli-lm.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4n.linker.w0.md) · **Assignee:** `bob-cli-lm.2` · **Size:** medium
**Created:** 2026-11-14 12:51:53 EST · **Closed:** 2026-11-14 14:09:55 EST
**Plan:** [202611/bank\_walk\_family\_b.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_walk_family_b.md)

## Description

keys: add family `b` to bob-navigation-hotkeys (commands, ]] / ]} repeat, [[ s w n b ]] selector, walkMode v4 with per-family attention), the serialized bank-walk runtime with payee-start landing and jump history, the bank toast, and the vault vimrc lines.

## Notes

[2026-11-14T19:03:16Z · bob-cli-lm.2] PROPOSED FOLLOW-UP: Triage pre-existing bob-plugins suite failures tracked by bob-cli-eh, bob-cli-km, bob-cli-io, bob-cli-ki, and bob-cli-ju — this phase reproduced the note-ready startup-storm 3-vs-2 scan failure on unchanged Ledger Tools/test files; the full unit suite also hit the already-tracked single-sample 200-link timing assertions. Focused bank-walk and navigation tests pass; this phase changes no Ledger Tools source.

[2026-11-14T19:09:55Z · bob-cli-lm.2] Implemented and deployed bank bracket navigation with row/day commands, counted and repeated gestures, the b selector and per-family waiting attention, payee-column landing with one stale-row retry, bank toast, and the four vault vimrc mappings. npm run validate and the focused bank/navigation/walker-footer tests pass; docs inventory is current, the deployed main.js and styles.css match the built plugin, and epic-symbol audit is clear. Full unit suite still reports five unrelated, already-tracked Ledger Tools startup/performance failures; recorded on this bead with their tracker IDs.

## Dependencies

- **Depends on:** [bob-cli-lm.1](bob-cli-lm.1.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lm.4](bob-cli-lm.4.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lm.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lm.2/README.md) | [bob-cli-lm.2](bob-cli-lm.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3745bfd`](https://github.com/bobs-org/bob-plugins/commit/3745bfdee30c70ae446d6e8d37385d93d1b97da0) | feat(navigation): add bank bracket walk family | [bob-cli-lm.2](bob-cli-lm.2.md) | 2026-11-14 14:12:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lm.2][1] | Need the phase scope, prior notes, and linked design before continuing assigned work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lm.2/README.md

<!-- sase:referenced-by:end -->
