# Bead: bob-cli-fv.3 — Structured description parser

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.3` · **Size:** medium
**Created:** 2026-11-02 09:28:51 EST · **Closed:** 2026-11-02 10:30:48 EST
**Plan:** [202611/gcal\_description\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_description_bullets.md)

## Description

description-parser: one linear HTML/plain-text parse into structured lines that feeds both directive verdicts (shared vectors stay byte-identical) and the future bullets. GcalEvent carries the result behind a redacted Debug.

## Notes

[2026-11-02T15:30:48Z · bob-cli-fv.3] Structured description parser landed: GcalEvent.description is EventDescription (redacted Debug: line/directive/oversized counts only). One linear HTML/plain parse feeds description_directives (shared tests/fixtures/event_buffer/vectors.json stay byte-identical) and outline (tests/fixtures/gcal_description/outline.json). Oversized 64 KiB flag does not stop parse. just check and just docs-check passed after rebase onto origin/master. No leftover --epic-symbol entries. Decision record not written (decision_record=no); propose-once memory not edited (no new record to supersede it).

## Dependencies

- **Blocks:** [bob-cli-fv.4](bob-cli-fv.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fv.5](bob-cli-fv.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.3/README.md) | [bob-cli-fv.3](bob-cli-fv.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`35c0a39`](https://github.com/bobs-org/bob-cli/commit/35c0a39a9f7c5b909db517b4aa94e0d67eff869d) | feat(gcal): parse calendar descriptions into structured lines | [bob-cli-fv.3](bob-cli-fv.3.md) | 2026-11-02 10:31:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fv.3][1] | Need full description, notes, design file, and attachments | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.3/README.md

<!-- sase:referenced-by:end -->
