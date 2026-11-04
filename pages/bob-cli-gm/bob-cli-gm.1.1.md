# Bead: bob-cli-gm.1.1 — Complete capture target-run grammar in bounded phases

[Bead Pages](../README.md) / [bob-cli-gm.1](bob-cli-gm.1.md) / bob-cli-gm.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) · **Assignee:** `bob-cli-gm.1.1.land`
**Created:** 2026-11-03 16:48:52 EST · **Closed:** 2026-11-03 21:10:44 EST
**Plan:** [202611/capture\_target\_runs\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_target_runs_finish.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_target_runs_finish.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_target_runs_finish.md

<!-- sase:links:end -->

## Description

Complete bob-cli-gm.1 with equivalent per-target execution, one editor item with targets, coded refusals, and one grammar revision bump.

## Notes

[2026-11-04T01:06:23Z · bob-cli-gm.1.1.land] LAND AUDIT / FOLLOW-UP TRIAGE: Read all four children and every note, both target-run plan artifacts, all four epic commits (d1f34842, a7c4b07f, 6a5b69b0, c341649a), current selector/adapters/draft/template/wire source, and intervening master commits through 734214e9. DECISIONS remain split_edges=refuse and memory_bulk_capture=no; no memory edits. PROPOSED FOLLOW-UP outcomes from gm.1.1.4: #1 docs generation independently reproduces on 734214e9 (uv run --project tools/docs bob-docs gen --check -> missing front matter in glossary/task-merge.md), causally owned by active bob-cli-go; corroborating DISCOVERED ISSUE appended there, no separate task. #2 catalog 69-versus-67 expectations were already repaired by dd90f8c7 in both nodes; appended resolution evidence to existing bob-cli-de, declined new duplicate or stale +1. Sase_new_task searches across types/all statuses, last-week task sweep, and active-epic scope sweep completed. Parent gm.1 note #1 incomplete-member discrepancy is resolved by the approved child contract: preserve singleton Need::Task; no independent follow-up task. Carry this resolution into the eventual close note. Both gm.1.1 and gm.1 currently have zero epic-symbol entries; justfile has no symvision recipe. Remaining parser and publication defects will be specified in a medium repair tale that must finish this epic and parent phase closeout itself.

[2026-11-04T01:07:31Z · bob-cli-gm.1.1.land] REMAINING EPIC WORK (reproduced with locally built bob at 734214e9): (1) hello @a+x middle @a+x goodbye incorrectly returns duplicate_capture_target in editor and strict capture although all markers are literal; @a+x @b+y note @a+x later is also wrongly refused. @a+x note @a+x reports duplicate instead of the approved split refusal. (2) @a+x s:3 @b+y note exposes two targets but capture dry-run produces one sub_bullet and one new mac_inbox task, with no schedule; leading schedule variants reveal selection loses extracted terminal state when singleton member views reparse raw text. (3) singleton @a+x p:2 note now fails strict parsing as retired priority while editor leaves p:2 literal; run probing must not change singleton behavior. (4) capture_complete/cli.rs and generated capture-complete help still claim grammar 4; activation c341649a lacks required ! and BREAKING CHANGE trailer. Repair these in a medium tale, retain grammar 9, finalize with a breaking capture commit without rewriting history. Integration audit: all 10 non-epic commits since d1f34842 reviewed, master equals origin/master; newer shared drawer ensure, staged project moves, and note-pull batch each compose with target runs in isolated dry-run probes and leave vault bytes unchanged. No changes needed to task-split/merge or periods/attachment source for this grammar scope. Complete current checks after fixes, then close this epic and only parent phase bob-cli-gm.1.

[2026-11-04T02:10:44Z · bob-cli-gm.1.1.land] Implemented and activated the approved target-run contract: duplicates are checked only within the selected run; split-edge refusal takes precedence; execution and template drafts fan out with schedule/priority semantics; editor parsing returns one item with targets, exact spans, and coded refusals; singleton behavior is preserved; grammar revision and CLI reference are 9. Also repaired the pre-existing task-split catalog/completion/help coverage and five Clippy errors required to make the named check pass. Verification: named sase tool run check 75c13c781669fb3c04788943911c8868 succeeded; focused capture parser/rewrite/completion/template suites and isolated scratch-vault dry-run/failure byte-preservation checks passed; docs-reference generation passed; git diff --check is clean. just docs-check lint passed, while generated drift remains blocked by unchanged sase/memory/glossary/task-merge.md missing front matter; no memory edit was made. Follow-up triage: docs generator issue is already recorded for bob-cli-go; the earlier 69/67 catalog count issue was recorded against bob-cli-de, and the later task-split catalog coverage is now represented at count 70; the incomplete Need::Task discrepancy is resolved by the approved singleton-preservation contract. No symvision recipe or epic symbols remain.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.land.md) | [bob-cli-gm.1.1](bob-cli-gm.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ebedfca`](https://github.com/bobs-org/bob-cli/commit/ebedfca8e666a9a79e9cc2989aca0a6b78edd983) | feat(capture)!: complete target-run grammar and landing | [bob-cli-gm.1.1](bob-cli-gm.1.1.md) | 2026-11-03 21:13:52 EST |
| bob-cli--plans | [`bob-cli--plans@c7dd457`](https://github.com/bobs-org/bob-cli--plans/commit/c7dd4577898944f1a6e05ae31c3bff3e31802ef3) | docs(plan): mark target-run landing complete | [bob-cli-gm.1.1](bob-cli-gm.1.1.md) | 2026-11-03 21:14:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gm.1.1.2][1] | Need the epic's final decisions before implementing its execution phase | 1 |
| read-by | [agent:bob-cli-gm.1.1.3][2] | epic decisions and scope | 1 |
| read-by | [agent:bob-cli-gm.1.1.4--1][3] | Need epic decisions and phase rules before completing the activation bead | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.4.md

<!-- sase:referenced-by:end -->
