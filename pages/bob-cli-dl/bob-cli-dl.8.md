# Bead: bob-cli-dl.8 — Turn it on in chezmoi, write the records, and run end-to-end acceptance

[Bead Pages](../README.md) / [bob-cli-dl](README.md) / bob-cli-dl.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2r.linker.w0.md) · **Assignee:** `bob-cli-dl.8` · **Size:** small
**Created:** 2026-10-28 08:15:27 EDT · **Closed:** 2026-10-28 13:17:39 EDT
**Plan:** [202610/relation\_cancel\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_cancel_labels.md)

## Description

rollout: add relations.cancel_labels [duplicate of, superseded by] to chezmoi home/dot_config/bob/config.yml and apply it per the chezmoi rules. Then write the accepted memory changes, drop every planned marker, check cross-repo doc links, run the end-to-end acceptance in a scratch vault, and report the host steps Bryan still has to run.

## Notes

[2026-10-28T17:16:59Z · bob-cli-dl.8] PROPOSED FOLLOW-UP: Task Card Cancel-stage door (⊘ Cancel as duplicate of… / superseded by… rows) was declined for this epic; revisit via the same writer if Bryan wants a second door.

[2026-10-28T17:17:08Z · bob-cli-dl.8] PROPOSED FOLLOW-UP: Mac Similar Tasks "Replace it" action (~~old|"superseded by") is out of scope for this epic; needs a mac-cancel-cue follow-up.

[2026-10-28T17:17:39Z · bob-cli-dl.8] Rollout landed and verified. Chezmoi relations.cancel_labels [duplicate of, superseded by] committed (linked clone f0397b1f) and validated against the new build; live ~/.config/bob/config.yml flips on land + chezmoi update. glossary:task-relation rewrite verified already landed by .6, docs/reference/glossary.md regenerated (ad22422c). All planned (phase ...) markers dropped (e7c95ce5); just docs-check green. Vectors resynced byte-for-byte to bob-plugins (413d60c), 24/24 JS vector tests green. just install done; installed bob reports cancels_source for both labels with zero warnings under the rollout config. Scratch acceptance 23/23: forward cancel+prune+recovery, rerun no-op, reverse ~~ + dry-run parity, 3 coded refusals writing nothing, reconcile/rename/relabel-away never-paths, inert without config. Suites green: 17 task_cancel, 18 relations_cancel, 26 hooks-relations, 91 relations, 965 capture, 95 capture_complete. Host steps for Bryan: (1) land the chezmoi commit, then chezmoi update on every host; (2) install the new Bob Mac Capture build; (3) vault plugin deploy already contains the cancel code - bob plugins sync correctly refused -F over another checkout's uncommitted main.js build, left untouched. Follow-ups noted on bead.

## Dependencies

- **Depends on:** [bob-cli-dl.3](bob-cli-dl.3.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dl.4](bob-cli-dl.4.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dl.6](bob-cli-dl.6.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dl.7](bob-cli-dl.7.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dl.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.8/README.md) | [bob-cli-dl.8](bob-cli-dl.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0349316`](https://github.com/bobs-org/bob-cli/commit/03493169b696813136e6d484d21e27aea60a7e2e) | docs(relations): drop cancel-label planned markers for rollout | [bob-cli-dl.8](bob-cli-dl.8.md) | 2026-10-28 13:19:22 EDT |
| bob-plugins | [`bob-plugins@ff1a24c`](https://github.com/bobs-org/bob-plugins/commit/ff1a24cc49e6e5862d33d0d18b0518cc7ca9354d) | chore(nav): resync task\_cancel vectors from bob-cli | [bob-cli-dl.8](bob-cli-dl.8.md) | 2026-10-28 13:21:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dl.4][1] | Need sibling phase status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.4/README.md

<!-- sase:referenced-by:end -->
