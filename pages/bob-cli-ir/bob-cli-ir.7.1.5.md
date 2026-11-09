# Bead: bob-cli-ir.7.1.5 — Records update CLI and dependent shell completion

[Bead Pages](../README.md) / [bob-cli-ir.7.1](bob-cli-ir.7.1.md) / bob-cli-ir.7.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.7.md) · **Assignee:** `bob-cli-ir.7.1.5` · **Size:** medium
**Created:** 2026-11-09 02:47:02 EST · **Closed:** 2026-11-09 05:43:57 EST
**Plan:** [202611/record\_append.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_append.md)

## Description

update-cli: add bob records update, its command catalog entry, and read-only shell completion for TYPE, existing STEM, and schema KEY=VALUE inputs; generate help documentation and prove parity with capture's shared update planner.

## Notes

[2026-11-09T10:43:57Z · bob-cli-ir.7.1.5] Implemented bob records update (TYPE STEM, -d/-f/-n/-o/-s, dry-run/open, human/JSON with changed/before/notes/warnings, exit 2 usage/missing/invalid, no-op no-rewrite, guarded writer). Added __catalog records-update entry with preview and typed slots, dispatch/help/registry coverage, retained TYPE completion with STEM and KEY=VALUE providers reusing capture validators/catalogs. Added isolated-vault parity tests and write-locked completion tests. Ran just docs-gen, updated docs/records.md, just check exit 0, docs-check passed. epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-ir.7.1.3](bob-cli-ir.7.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.7.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.5/README.md) | [bob-cli-ir.7.1.5](bob-cli-ir.7.1.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.7.1.5][1] | check notes and full description | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.5/README.md

<!-- sase:referenced-by:end -->
