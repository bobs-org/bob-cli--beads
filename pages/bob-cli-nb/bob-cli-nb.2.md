# Bead: bob-cli-nb.2 — Step gates and per-step adapters

[Bead Pages](../README.md) / [bob-cli-nb](README.md) / bob-cli-nb.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1e2.md) · **Assignee:** `bob-cli-nb.2` · **Size:** medium
**Created:** 2026-11-18 13:06:51 EST · **Closed:** 2026-11-18 17:03:24 EST
**Plan:** [202611/bob\_tick.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_tick.md)

## Description

gates: add the today's-note readiness gate for gcal and tasks; gcal's once-a-day yesterday sync and its cooldown shared with gcal's host status; the refs change gate (lib/xlib listing fingerprint, pre-scan hook, 6h ceiling); an additive gmail JSON busy field mapped to waiting; per-step JSON adapters with one-line summaries; and gate reasons in -d.

## Notes

[2026-11-18T22:03:24Z · bob-cli-nb.2] Implemented tick gates: readiness gate for gcal/tasks, gcal -n 2 yesterday scope with host-status cooldown, refs change gate with fingerprint/hook/6h ceiling storing pre-scan fingerprint, additive gmail busy JSON field, per-step adapters with summaries and gate JSON in receipts. Verified: 23 tick CLI tests pass, 49 gmail_sync tests pass, tick lib config/schedule tests pass, gcal sync unit tests pass, just fmt and just lint clean, epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-nb.1](bob-cli-nb.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-nb.4](bob-cli-nb.4.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-nb.5](bob-cli-nb.5.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nb.2/README.md) | [bob-cli-nb.2](bob-cli-nb.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`75de001`](https://github.com/bobs-org/bob-cli/commit/75de001f8c3202241ee9b2f3f65936f9f0db7147) | feat(tick): add step gates and per-step adapters | [bob-cli-nb.2](bob-cli-nb.2.md) | 2026-11-18 17:05:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nb.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nb.2/README.md

<!-- sase:referenced-by:end -->
