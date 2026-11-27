# Bead: bob-cli-qj.2 — bob prose with permanent legacy aliases

[Bead Pages](../README.md) / [bob-cli-qj](README.md) / bob-cli-qj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.2` · **Size:** medium
**Created:** 2026-11-26 10:56:27 EST · **Closed:** 2026-11-26 13:49:38 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

## Description

prose-cli: one predicate reads both type spellings, writers emit [[prose]], bob prose becomes canonical with bob articles as a hidden alias, copy and docs move to prose, and a section-numbers flag plus a host probe ship; wire vocabulary stays frozen.

## Notes

[2026-11-26T18:49:11Z · bob-cli-qj.2] PROPOSED FOLLOW-UP: Triage the baseline capture/drawer test failures — clean base cf414ce reproduces native::capture::block_diff::tests::annotate_drawer_lines_uses_after_snapshot_except_removed with the same missing Stale drawer annotation already tracked by bob-cli-qo; the full check also reported unrelated capture/task-drawer assertion drift.

[2026-11-26T18:49:38Z · bob-cli-qj.2] Implemented canonical prose typing and bob prose behavior, retained the hidden articles alias, added section-number toggling, updated docs and generated help. Verified: docs-gen; docs-check (447 passed, 1 skipped); check-scripts (152 passed); focused prose CLI (48 passed), prose library (39 passed, 1 ignored), note-catalog, root-help, and nightly tests; cargo fmt and diff checks. The initial repo-wide just check failed with phase expectation failures and unrelated drawer/capture failures. The phase tests now pass focused reruns; the representative drawer mismatch reproduces on clean base cf414ce and is tracked as bob-cli-qo, with a proposed follow-up recorded here. Epic symbols were empty.

## Dependencies

- **Depends on:** [bob-cli-qj.1](bob-cli-qj.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qj.3](bob-cli-qj.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qj.4](bob-cli-qj.4.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.2/README.md) | [bob-cli-qj.2](bob-cli-qj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4168e20`](https://github.com/bobs-org/bob-cli/commit/4168e2013a35cf08e11858c2d66a61d60f5f8a8b) | feat(prose): make prose the canonical note type and CLI | [bob-cli-qj.2](bob-cli-qj.2.md) | 2026-11-26 14:48:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.2][1] | Need phase notes and design details to see whether earlier work left an explicit remainder | 3 |
| read-by | [agent:research.6k.gem][2] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md

<!-- sase:referenced-by:end -->
