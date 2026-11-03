# Bead: bob-cli-gb.1 — bob-cli: one clock spelling table, #on, offclock: note facts, and the effective-clock resolver

[Bead Pages](../README.md) / [bob-cli-gb](README.md) / bob-cli-gb.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.31.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.31.linker.w0.md) · **Assignee:** `bob-cli-gb.1` · **Size:** medium
**Created:** 2026-11-02 17:38:44 EST · **Closed:** 2026-11-02 18:40:53 EST
**Plan:** [202611/off\_on\_tags\_and\_offclock\_areas.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_on_tags_and_offclock_areas.md)

## Description

clock-contract: add the shared spelling table and tri-state ClockTag, make #off canonical and #on win on vault lines, parse offclock: into NoteFacts with lints, and add effective_clock plus Event Task enrichment over the PT13 root walk.

## Notes

[2026-11-02T23:40:53Z · bob-cli-gb.1] Implemented shared #off/#on parsing, offclock note facts and effective clock resolution, Event Task enrichment, resolver health reporting, and documentation. Verified just check, just docs-gen, just docs-check, git diff --check, and scratch capture where #off wrote [off:: 25m].

## Dependencies

- **Blocks:** [bob-cli-gb.2](bob-cli-gb.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.3](bob-cli-gb.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.4](bob-cli-gb.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.5](bob-cli-gb.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.1/README.md) | [bob-cli-gb.1](bob-cli-gb.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ab752cc`](https://github.com/bobs-org/bob-cli/commit/ab752cc536d2b1a011fe5aab1e0fc3205d6c3bdf) | feat(pomodoro-clock): resolve off-clock tags and note defaults | [bob-cli-gb.1](bob-cli-gb.1.md) | 2026-11-02 18:42:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gb.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.1/README.md

<!-- sase:referenced-by:end -->
