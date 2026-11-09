# Bead: bob-cli-ix.3 — Document \`Nx\` and record the decision

[Bead Pages](../README.md) / [bob-cli-ix](README.md) / bob-cli-ix.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3s.linker.w0.md) · **Assignee:** `bob-cli-ix.3` · **Size:** medium
**Created:** 2026-11-09 05:24:37 EST · **Closed:** 2026-11-09 08:24:18 EST
**Plan:** [202611/sized\_pomodoro\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/sized_pomodoro_close.md)

## Description

docs: update capture.md, the capture-syntax reference, and capture/capture-parse help, regenerate CLI docs, and add the exact-or-refuse decision record when its decision is on.

## Notes

[2026-11-09T13:24:05Z · bob-cli-ix.3] PROPOSED FOLLOW-UP: root-long help fixture still expects the old capture-related summary; commit 44427b30 changed the about string to "List existing tasks and record notes a new capture may duplicate" without updating tests/fixtures/help/root-long.txt, so help::root_help_matches_sectioned_short_and_long_snapshots fails on the clean base tree too

[2026-11-09T13:24:18Z · bob-cli-ix.3] Docs phase done: capture.md gained Grammar-at-a-glance [N]x row plus Closing at a size (rule, exact-or-refuse table, refusal copy, captions, tip, hint, mnemonic), Event-Task C sentence, chain/link rows, prose rows (2X4 lumber, x made it 2x, x 2x faster, = 2x, 0x, 100x, 2x=3, =2x, 2x#bugs), never-extends fix; capture-syntax gained [N]x token row and nx-close section; capture/capture-parse help updated with mnemonic, hint, refusal codes, captions, tip; CLI goldens regenerated; grammar-22 note in compatibility.md; no memory strand per decision_record=no. Verified: just docs-gen ok, just docs-check ok (447 passed), cargo fmt+clippy ok, lib 5962 passed, cli suite 3381/3382 (sole failure is pre-existing root-long fixture drift from 44427b30, recorded as follow-up), doc-tests ok.

## Dependencies

- **Depends on:** [bob-cli-ix.2](bob-cli-ix.2.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ix.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ix.3/README.md) | [bob-cli-ix.3](bob-cli-ix.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5f361c5`](https://github.com/bobs-org/bob-cli/commit/5f361c5a253f6e7022d61c98bd6dc0068717d663) | docs(capture): document the sized Nx close | [bob-cli-ix.3](bob-cli-ix.3.md) | 2026-11-09 08:25:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ix.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ix.3/README.md

<!-- sase:referenced-by:end -->
