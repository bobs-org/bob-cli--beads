# Bead: bob-cli-qj.4 — Host gate, vault cutover, and canonical plugin calls

[Bead Pages](../README.md) / [bob-cli-qj](README.md) / bob-cli-qj.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.4` · **Size:** small
**Created:** 2026-11-26 10:56:27 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

## Description

prose-vault: pass the host-currency gate, retype the one live note and rename the vault's type files, switch plugin calls to bob prose, and apply only accepted memory decisions.

## Notes

[2026-11-27T11:29:15Z · bob-cli-qj.4] GATE RERUN (2026-11-27 ~11:10Z): prose-type-read passes on athena, apollo, and the Mac (all bob 0.6.0 from master), but all three hosts lacked bob-prose-type-v1 in the four plugins. Cause: qj.3's bob-plugins commit 9426ee8f never reached origin/master and is in no local clone (its workspace-10 clone was re-cloned), and later syncs from master overwrote the dirty deploy. This turn re-lands the qj.3 plugin work on bob-plugins master (detection of [[prose]]/[[article]] in bob-articles, command-mode, navigation-hotkeys, and ledger-tools; Bob Prose copy; toggle-section-numbers; command-mode rows; docs; marker), with the spawn argv already switched to bob prose (plan step 2), because every host's bob already passes the probe. Deployed on apollo (all four synced with the marker; ledger-tools went through the documented landed-build recipe for 2bd92b19, no -F). Memory step 3 had already landed in bob-cli 4168e201; this turn only fixed the decision strand's evidence to cite 4168e201. Verified: bob-plugins npm test 10223 pass / 2 fail (both reproduce on clean base 0ffb4511), validate 12/12, build:check, docs:gen, docs:check (via bob-cli), bob-cli just docs-gen and docs-check pass, and bob prose format --stdin [--section-numbers off] -f json returns schema 1 plans from the installed bob. Remaining: a gate to sync athena and the Mac, then the vault cutover.

[2026-11-27T11:29:24Z · bob-cli-qj.4] PROPOSED FOLLOW-UP: Triage the two baseline bob-plugins unit failures already tracked by bob-cli-q5.6.1: test-navigation-relation-links-stage 'links-to row follows blocks with N…' and test-prose-field-roles (744-snooze-card-modal.js:129 needs a bob-text role). Both reproduce on clean base 0ffb4511.

[2026-11-27T11:29:32Z · bob-cli-qj.4] PROPOSED FOLLOW-UP: Guard phase closes against unpushed linked-repo commits. qj.3 closed citing bob-plugins 9426ee8f, which never reached origin/master, so qm.5, qm.6, and qj.4 all found the Bob Prose work missing. A close or land check that the cited linked-repo SHA is reachable from upstream would catch this.

## Dependencies

- **Depends on:** [bob-cli-qj.2](bob-cli-qj.2.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qj.3](bob-cli-qj.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qj.5](bob-cli-qj.5.md) ◐ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qm.7](../bob-cli-qm/bob-cli-qm.7.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.4/README.md) | [bob-cli-qj.4](bob-cli-qj.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`16a2497`](https://github.com/bobs-org/bob-cli/commit/16a2497d0a73f8497220a656116eaf311c08d246) | docs(decisions): cite the prose-cli commit in prose-notes-are-owned-prose | [bob-cli-qj.4](bob-cli-qj.4.md) | 2026-11-27 06:34:53 EST |
| bob-plugins | [`bob-plugins@c41e07e`](https://github.com/bobs-org/bob-plugins/commit/c41e07e9d6d66e06410af472df4117b0be6efc49) | feat(prose): Bob Prose in Obsidian with canonical bob prose calls | [bob-cli-qj.4](bob-cli-qj.4.md) | 2026-11-27 06:35:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qm.5--1][1] | Check whether the active prose-vault phase touches files shared with this prose-seam implementation | 1 |
| read-by | [agent:bob-cli-qm.6][2] | check whether qj.4 found qj.3 changes missing on master | 1 |
| read-by | [agent:bob-cli-qm.7--1][3] | Check the required glossary/deployment gate before proceeding with bob-cli-qm.7 | 1 |
| read-by | [agent:bob-cli-qp.8][4] | Check qj.4 gate for qm.7 before ref go-live | 1 |
| read-by | [agent:research.6k.cld][5] | Check qj.4 dependencies | 1 |
| read-by | [agent:research.6k.gem][6] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6l.gem][7] | Check live progress of active property-card and prose epics for parallelization analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qm.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qm.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qm.7.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.8.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cld/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
