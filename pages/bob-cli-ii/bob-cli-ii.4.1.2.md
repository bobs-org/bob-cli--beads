# Bead: bob-cli-ii.4.1.2 — Watch journal folding and remote preparation

[Bead Pages](../README.md) / [bob-cli-ii.4.1](bob-cli-ii.4.1.md) / bob-cli-ii.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.md) · **Assignee:** `bob-cli-ii.4.1.2` · **Size:** medium
**Created:** 2026-11-08 12:01:29 EST · **Closed:** 2026-11-08 13:25:49 EST
**Plan:** [202611/gmail\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_reply_watch.md)

## Description

watch_inputs: add body-free turn/gone journal types and metadata-first watch preparation through the coordinated read layer, including task-level multi-thread effect planning.

## Notes

[2026-11-08T18:11:05Z · bob-cli-ii.4.1.2] PROPOSED FOLLOW-UP: Stabilize Gmail sync guard contention test — native::gmail::sync::guard::tests::real_lock_contention_and_release failed once in the broad Gmail unit run, then passed alone on the unchanged tree; no task bead currently tracks it.

[2026-11-08T18:22:58Z · bob-cli-ii.4.1.2] PROPOSED FOLLOW-UP: Clear the existing records schema lint errors — configured `just lint` still fails on unchanged `src/native/records/schema.rs:122` (derivable Default) and `:1347` (needless borrow); neither file changed in this phase, and no task bead currently tracks them.

[2026-11-08T18:25:49Z · bob-cli-ii.4.1.2] Implemented body-free turn/gone journal folding, metadata-first watch preparation, and deterministic multi-thread task planning. Verified 16 focused watch tests; the Gmail suite's one lock-contention failure passed on isolated rerun. Recorded that flake and the two unchanged records/schema lint errors as proposed follow-ups.

## Dependencies

- **Depends on:** [bob-cli-ii.4.1.1](bob-cli-ii.4.1.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ii.4.1.3](bob-cli-ii.4.1.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.2/README.md) | [bob-cli-ii.4.1.2](bob-cli-ii.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`86af3d5`](https://github.com/bobs-org/bob-cli/commit/86af3d5ebd91dca623891e62cd6cdf9b44b3ba0b) | feat(gmail): add watch journal and preparation planning | [bob-cli-ii.4.1.2](bob-cli-ii.4.1.2.md) | 2026-11-08 13:26:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.4.1.2][1] | Need the phase scope, design file, prior notes, and recorded decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.2/README.md

<!-- sase:referenced-by:end -->
