# Bead: bob-cli-qj.3 — Bob Prose in Obsidian

[Bead Pages](../README.md) / [bob-cli-qj](README.md) / bob-cli-qj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.3` · **Size:** medium
**Created:** 2026-11-26 10:56:27 EST · **Closed:** 2026-11-26 15:51:24 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

## Description

prose-plugins: four plugins detect both spellings, display names and command titles change under unchanged ids, a Toggle section numbers command lands, plugin docs are fixed, and the bundles deploy with a currency marker.

## Notes

[2026-11-26T20:51:03Z · bob-cli-qj.3] qj.3 landed in bob-plugins as 9426ee8f feat(prose): Bob Prose in Obsidian with toggle-section-numbers. Marker bob-prose-type-v1 present in all four built bundles (bob-articles, bob-command-mode, bob-navigation-hotkeys, bob-ledger-tools). Deployed via bob plugins sync; all four ids up to date in the vault. Gates: build --check, full unit suite 9988 pass/0 fail, perf 26 pass, validate 12/12, docs:gen + docs:check passed. -r record qj.3 commit and currency marker

[2026-11-26T20:51:24Z · bob-cli-qj.3] Bob Prose in Obsidian landed as bob-plugins 9426ee8f. Detection accepts [[prose]]/[[article]] in all four plugins; Bob Prose display names, renamed commands, and new toggle-section-numbers (flag plumbed from metadata cache through bob articles format --stdin --section-numbers) verified by unit tests. Manifest 0.3.0, docs regenerated, marker bob-prose-type-v1 in all four bundles, vault deploy up to date. Gates: build --check, unit 9988/0, perf 26/0, validate 12/12, docs:check.

## Dependencies

- **Depends on:** [bob-cli-qj.2](bob-cli-qj.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qj.4](bob-cli-qj.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qm.5](../bob-cli-qm/bob-cli-qm.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.3/README.md) | [bob-cli-qj.3](bob-cli-qj.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.4][1] | Need prose-cli commit SHA and prose-plugins marker/commit for the prose-vault phase | 1 |
| read-by | [agent:bob-cli-qm.5--1][2] | Verify the prerequisite phase resolution before resuming bob-cli-qm.5 | 1 |
| read-by | [agent:bob-cli-qm.6][3] | check whether qj.3 renamed article detection to prose and added toggle-section-numbers | 3 |
| read-by | [agent:research.6k.cld][4] | Check qj.3 dependencies for prose card sequencing | 2 |
| read-by | [agent:research.6k.gem][5] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6k.grk][6] | Need qj plugin rename phase files to judge overlap with prose/notebook cards | 1 |
| read-by | [agent:research.6l.gem][7] | Check live progress of active property-card and prose epics for parallelization analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.4.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qm.5.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qm.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cld/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.grk/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
