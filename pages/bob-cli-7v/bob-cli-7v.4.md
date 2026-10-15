# Bead: bob-cli-7v.4 — Variadic TARGET, fail-fast validation, and collection overlap policy

[Bead Pages](../README.md) / [bob-cli-7v](README.md) / bob-cli-7v.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.4` · **Size:** medium
**Created:** 2026-10-15 12:30:28 EDT · **Closed:** 2026-10-15 13:21:35 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

## Description

gate: make TARGET variadic, route two or more targets into a new collection module that runs every pre-network check (kinds, -H, duplicates, cap, name waterfall, overlap, target plan) with polished errors, and rewrite the -N/TARGET help; the route itself is a stub until the next phase.

## Notes

[2026-10-15T17:21:35Z · bob-cli-7v.4] Implemented variadic create targets, collection help, fail-fast URL/name validation, target planning, and grouped overlap checks; verified the collection CLI and overlap tests plus full just check (passed). Epic-symbol check found no entries to resolve.

## Dependencies

- **Depends on:** [bob-cli-7v.1](bob-cli-7v.1.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-7v.2](bob-cli-7v.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7v.5](bob-cli-7v.5.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.4/README.md) | [bob-cli-7v.4](bob-cli-7v.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5feaaac`](https://github.com/bobs-org/bob-cli/commit/5feaaac1a322b5756d3469464d866ca85a89bcae) | feat(highlights-ref): add multi-url collection gate | [bob-cli-7v.4](bob-cli-7v.4.md) | 2026-10-15 13:22:20 EDT |
