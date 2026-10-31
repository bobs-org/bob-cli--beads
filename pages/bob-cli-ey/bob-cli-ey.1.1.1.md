# Bead: bob-cli-ey.1.1.1 — Delete the @@route+block-id draft-wide form

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 15:16:16 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

global-route-id-removal: delete `@@route+id` end to end (parent plan §1.5): `ParsedGlobalDestination.block_id`/`mode`, the `draft.rs` `+` branch, the `GlobalSubBulletRoute`/`GlobalSubBulletBlockId` spans and `Need::Task` from `classify_global_token`, `global_destination.mode`/`block_id` in capture-parse and capture JSON, the "under ^id" human output, `capture_related/draft.rs` handling, and its tests and docs. `@@route+id` now fails with the generic `@@` declaration error. Commit as `feat(capture)!:`.

## Notes

[2026-10-31T19:16:16Z · bob-cli-ey.1.1.1--a] Verified just docs-gen, just docs-check, and just check; epic-symbol scan had no leftovers. Landed feat(capture)!: remove @route+block-id as 36c48075 on origin/master.

## Dependencies

- **Blocks:** [bob-cli-ey.1.1.2](bob-cli-ey.1.1.2.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.1.md) | [bob-cli-ey.1.1.1](bob-cli-ey.1.1.1.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`36c4807`](https://github.com/bobs-org/bob-cli/commit/36c48075510ff202a5d717fdf1a13e8bea7b37a8) | feat(capture)!: remove @@route+block-id | [bob-cli-ey.1.1.1](bob-cli-ey.1.1.1.md) | 2026-10-31 15:10:07 EDT |
