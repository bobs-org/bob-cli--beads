# Bead: bob-cli-6u.18.2 — Projects sync hoist, Sub-projects placement, and inline ^prj schedule issues

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.2` · **Size:** small
**Created:** 2026-10-12 18:07:06 EDT · **Closed:** 2026-10-12 19:48:35 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

cli-projects-sync: gate the hoist on an open ^prj, insert Sub-projects after the whole Cancel Log / Depends-On subtree, match only direct Depends-On children, report invalid or duplicate inline ^prj dates, skip fenced lines, tag-helper tests.

## Notes

[2026-10-12T23:48:22Z · bob-cli-6u.18.2] Hoist gated on open ^prj; Sub-projects insert after Cancel Log / Depends-On subtree; only direct ^prj Depends-On children match; invalid/duplicate inline ^prj scheduled reported; fenced ^prj skipped; PDT tag tests + CRLF; blocking.rs uses case-insensitive prj id. just check: only bob-cli-6m percent-listen failures. BOB_DIR=~/bob new-build projects sync --dry-run: 85 projects, 0 hoists, 0 errors, 0 warnings.

[2026-10-12T23:48:27Z · bob-cli-6u.18.2] PROPOSED FOLLOW-UP: just check still fails capture::r#ref percent-listen tests — already tracked by bob-cli-6m

[2026-10-12T23:48:35Z · bob-cli-6u.18.2] Gated hoist on open ^prj, insert Sub-projects after Cancel Log/Depends-On subtree, report invalid/duplicate inline ^prj scheduled, skip fenced ^prj, PDT tag+CRLF tests, case-insensitive prj id. just check: only bob-cli-6m percent-listen failures. Vault dry-run: 85 projects, 0 hoists, 0 errors.

## Dependencies

- **Depends on:** [bob-cli-6u.18.1](bob-cli-6u.18.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.18.6](bob-cli-6u.18.6.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.2/README.md) | [bob-cli-6u.18.2](bob-cli-6u.18.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b09612e`](https://github.com/bobs-org/bob-cli/commit/b09612ee99c0f977417da4bcab9c52c1518cc161) | fix(projects): gate hoist and Sub-projects placement | [bob-cli-6u.18.2](bob-cli-6u.18.2.md) | 2026-10-12 19:49:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.2/README.md

<!-- sase:referenced-by:end -->
