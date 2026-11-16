# Bead: bob-cli-mb.1 — bob-cli: shared note tiers and \`capture-complete -A\` archive catalog

[Bead Pages](../README.md) / [bob-cli-mb](README.md) / bob-cli-mb.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cs.md) · **Assignee:** `bob-cli-mb.1` · **Size:** medium
**Created:** 2026-11-16 10:14:21 EST · **Closed:** 2026-11-16 11:06:51 EST
**Plan:** [202611/note\_goto\_followups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_followups.md)

## Description

cli-archive-scope: give `note_catalog` one shared path-tier predicate (living, archive, hidden), add an archive catalog of top-level done/ notes, superseded library folders, and zorg daily satellites, and serve it behind a new `capture-complete -A/--archived-notes` flag with an `archived` marker; help, docs, and tests.

## Notes

[2026-11-16T16:06:34Z · bob-cli-mb.1] Verified read-only release probes on /home/bryan/bob: living catalog median 92.84 ms, 3,652 rows, 763,193 bytes; clean-base median 89.35 ms, 3,652 rows, 763,175 bytes, so living scan is +3.9% (within the 10% budget). With -A, median 64.72 ms, 1,891 rows, 339,407 bytes: 55 archive rows and 1,836 satellites (54 done-group rows), zero warnings. No follow-up required.

[2026-11-16T16:06:51Z · bob-cli-mb.1] Implemented shared note-tier classification and capture-complete -A archive/satellite catalog output. Verified just all, just docs-check, release build, CLI help, and live release probes; living latency is +3.9% versus clean base, within the 10% budget. Epic-symbol check is clear.

## Dependencies

- **Blocks:** [bob-cli-mb.2](bob-cli-mb.2.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mb.4](bob-cli-mb.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mb.1/README.md) | [bob-cli-mb.1](bob-cli-mb.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`430162f`](https://github.com/bobs-org/bob-cli/commit/430162f5716f93cf64b846dde5572e745b4013f3) | feat(note-catalog): add archive tiers to note goto | [bob-cli-mb.1](bob-cli-mb.1.md) | 2026-11-16 11:07:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mb.1][1] | Need the phase scope and design file; checking earlier work before continuing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mb.1/README.md

<!-- sase:referenced-by:end -->
