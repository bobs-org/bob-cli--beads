# Bead: bob-cli-mj.3 — bob-cli: streamed copies and sync guards for every attachment

[Bead Pages](../README.md) / [bob-cli-mj](README.md) / bob-cli-mj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.63.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.63.linker.w0.md) · **Assignee:** `bob-cli-mj.3` · **Size:** medium
**Created:** 2026-11-16 17:31:30 EST · **Closed:** 2026-11-16 19:39:21 EST
**Plan:** [202611/video\_attachments\_z\_player.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/video_attachments_z_player.md)

## Description

cli-guards: stream attachment hashing and copying (no whole-file buffers, abort when the source changes after planning), refuse attachments of 95 MiB or more and destinations the vault .gitignore ignores, warn at 50 MiB, document the new codes, and record the decision strand; mark the commit with !.

## Notes

[2026-11-17T00:39:21Z · bob-cli-mj.3] Implemented bounded attachment hashing/copying, source-change checks across reuse and fanout, 50/95 MiB guards, batched gitignore refusal, structured capture/import warnings and codes, and docs/help updates. Verified with just check, just docs-gen, and just docs-check. Omitted the proposed decision strand per the epic reviewer decision memory_video_decision=false.

## Dependencies

- **Depends on:** [bob-cli-mj.1](bob-cli-mj.1.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.3/README.md) | [bob-cli-mj.3](bob-cli-mj.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mj.3][1] | Need the phase scope, design file, prior notes, and epic decisions before completing the assigned work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.3/README.md

<!-- sase:referenced-by:end -->
