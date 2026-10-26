# Bead: bob-cli-c9.4.1.5 — Enable local-file and vault-snapshot overwrite

[Bead Pages](../README.md) / [bob-cli-c9.4.1](bob-cli-c9.4.1.md) / bob-cli-c9.4.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) · **Assignee:** `bob-cli-c9.4.1.5` · **Size:** medium
**Created:** 2026-10-25 22:34:44 EDT · **Closed:** 2026-10-26 01:20:28 EDT
**Plan:** [202610/unannotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md)

## Description

local: connect local PDF, Markdown, and vault-note rendering to the overwrite transaction, including explicit status handling and the shared preserved or replaced audio policy, with offline CLI tests.

## Notes

[2026-10-26T05:20:28Z · bob-cli-c9.4.1.5] Local overwrite is wired for Markdown, original local PDF, and same-day vault-note snapshots via CaptureOutcome plus private staging into execute. Dry-run plans before pandoc/listen; in-place replace keeps stem/id/task; prose archives; -N older reading; wip/ready/blocked/archived/read; explicit -s ready; -T title; kept/replaced/--no-audio/-L audio; listen failure leaves bytes; library PDF TARGET and URL overwrite still refused. Execute skips the scan dirty-target veto after publishing because those files are the transaction. Verified: 15 overwrite_local CLI tests, recapture/overwrite/create/force lib tests, URL/collection overwrite refusals, and ordinary create ingest.

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.4](bob-cli-c9.4.1.4.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.4.1.6](bob-cli-c9.4.1.6.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.5/README.md) | [bob-cli-c9.4.1.5](bob-cli-c9.4.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`00200a9`](https://github.com/bobs-org/bob-cli/commit/00200a967fa818fc0f2c40135bc7cc49d2ce927c) | feat(highlights): enable local-file and vault-snapshot overwrite | [bob-cli-c9.4.1.5](bob-cli-c9.4.1.5.md) | 2026-10-26 01:21:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.5][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.5/README.md

<!-- sase:referenced-by:end -->
