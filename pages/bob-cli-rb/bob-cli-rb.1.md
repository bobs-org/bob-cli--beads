# Bead: bob-cli-rb.1 — bob-cli capture.type\_leads loader, bob types surfacing, rename guard

[Bead Pages](../README.md) / [bob-cli-rb](README.md) / bob-cli-rb.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.1` · **Size:** medium
**Created:** 2026-11-27 15:03:20 EST · **Closed:** 2026-11-27 15:50:00 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

## Description

lead_config: add the deploy-safe `capture.type_leads` loader with parser-probe validation and per-entry degradation, show leads and their warnings in `bob types`, guard `bob types rename`, and document the config key.

## Notes

[2026-11-27T20:49:40Z · bob-cli-rb.1--2] PROPOSED FOLLOW-UP: Repair baseline Clippy failures in src/native/prose/convert/inline.rs — both the repaired phase check and clean-HEAD check report denied bool::then-in-filter_map and useless-format lints in this untouched file.

[2026-11-27T20:50:00Z · bob-cli-rb.1--2] Phase implementation completed. The repaired phase check and clean-HEAD check reproduce the two denied baseline Clippy lints in untouched src/native/prose/convert/inline.rs; epic-symbols is clear, and the temporary clean-base worktree was removed.

## Dependencies

- **Blocks:** [bob-cli-rb.2](bob-cli-rb.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rb.5](bob-cli-rb.5.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.1.md) | [bob-cli-rb.1](bob-cli-rb.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`421de94`](https://github.com/bobs-org/bob-cli/commit/421de94dc381f1947e24154d181ef44b6829c86c) | feat(types): add configurable capture type leads | [bob-cli-rb.1](bob-cli-rb.1.md) | 2026-11-27 15:51:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rb.1--2][1] | Verify the phase close and proposed baseline-follow-up note were recorded | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.1.md

<!-- sase:referenced-by:end -->
