# Bead: bob-cli-os.9 — Feed enrichment in the dossier and both routes

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.9` · **Size:** medium
**Created:** 2026-11-21 14:59:42 EST · **Closed:** 2026-11-22 02:31:38 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

transcript_dossier: attach proven feed notes, chapters, and transcripts to create and ingest captures under a time budget, render the transcript pages, add the enrich knob, and report each step-down once.

## Notes

[2026-11-22T06:57:02Z · bob-cli-os.9] PROPOSED FOLLOW-UP: docs-check unit tests fail on master independently of this phase — tools/docs/tests/test_contracts.py expects 54 contracts / README table SHA 34f4f8… vs 55 entries including walks.md (already noted on bob-cli-os.5 and others)

[2026-11-22T07:31:38Z · bob-cli-os.9--1] Closed by explicit `sase stitch create -B close` after create_commit landed 2f4fef6d ("feat(ref): attach publisher feed notes and transcripts to episode dossiers"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-os.9` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-os.10](bob-cli-os.10.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-os.6](bob-cli-os.6.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-os.7](bob-cli-os.7.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-os.8](bob-cli-os.8.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-os.9.md) | [bob-cli-os.9](bob-cli-os.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2f4fef6`](https://github.com/bobs-org/bob-cli/commit/2f4fef6dad5b749e944f3cf25fe31ceba351be42) | feat(ref): attach publisher feed notes and transcripts to episode dossiers | [bob-cli-os.9](bob-cli-os.9.md) | 2026-11-22 02:30:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.10][1] | Check sibling phase status and any follow-up notes relevant to rollout | 1 |
| read-by | [agent:bob-cli-os.8][2] | Check whether the dependent transcript_dossier phase assumes a transcript API | 2 |
| read-by | [agent:bob-cli-os.9--1][3] | Need the phase scope, notes, and remaining close work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.8/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-os.9.md

<!-- sase:referenced-by:end -->
