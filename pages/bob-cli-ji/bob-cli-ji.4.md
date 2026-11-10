# Bead: bob-cli-ji.4 — Writing, previewing, and applying notes

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.4` · **Size:** medium
**Created:** 2026-11-10 05:59:46 EST · **Closed:** 2026-11-10 09:54:35 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

## Description

write: normalize one-line and multi-line input into canonical lines using shared vectors, and reject bad routes and conflicts at write time. Show the faithful 'lands as' preview and terminal time rail, then save or clear. Report saved versus applied, and on the writer run the immediate sync. Add the preview and save JSON with highlight spans, golden JSON fixtures for the Mac, and the `docs/gcal-notes.md` contract.

## Notes

[2026-11-10T14:53:25Z · bob-cli-ji.4] PROPOSED FOLLOW-UP: Bring docs/reference/json-outputs.md and the four docs/reference/mac-capture pages under the 6000-word budget — just docs-check reports the same five overages on clean base a2809a1d.

[2026-11-10T14:54:35Z · bob-cli-ji.4] Implemented note normalization/validation, preview and time rail, JSON goldens, save/clear, and writer-host immediate sync for event and series days. Verified 13 gcal note integration tests, normalization vectors, 2048-byte limit, cargo fmt, diff check, and docs-gen. docs-check still fails on five unchanged reference pages; reproduced identically on clean base a2809a1d and recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-ji.2](bob-cli-ji.2.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.5](bob-cli-ji.5.md) ◐ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.6](bob-cli-ji.6.md) ◐ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7](bob-cli-ji.7.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.4/README.md) | [bob-cli-ji.4](bob-cli-ji.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf7c060`](https://github.com/bobs-org/bob-cli/commit/cf7c06052b26b64d5fb68e10a4b65b5f759fac10) | feat(gcal): add private event note writes and preview | [bob-cli-ji.4](bob-cli-ji.4.md) | 2026-11-10 09:56:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.40.cld][1] | Check phase progress and notes for guide accuracy | 1 |
| read-by | [agent:research.40.mus][2] | research guide on adding metadata to private event tasks | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.mus/README.md

<!-- sase:referenced-by:end -->
