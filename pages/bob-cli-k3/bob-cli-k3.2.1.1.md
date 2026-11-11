# Bead: bob-cli-k3.2.1.1 — Parse album declarations through shared record schema validation

[Bead Pages](../README.md) / [bob-cli-k3.2.1](bob-cli-k3.2.1.md) / bob-cli-k3.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-k3.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-k3.2.md) · **Assignee:** `bob-cli-k3.2.1.1` · **Size:** medium
**Created:** 2026-11-11 05:07:02 EST · **Closed:** 2026-11-11 05:58:46 EST
**Plan:** [202611/album\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_model.md)

## Description

album-schema: add album/record type predicates and the album declaration model; refactor record schema helpers around source-aware diagnostics; parse top-level album facts and the ordered record mapping with precise file/line/key paths, retaining claims when validation fails. Preserve config parser behavior and cover the local schema rules in unit tests.

## Notes

[2026-11-11T10:58:46Z · bob-cli-k3.2.1.1--2] Implemented album declaration parsing with shared source-aware record schema validation, preserved config parsing behavior, and added album/record type predicates. Verified cargo test --lib native::records::schema::tests (11 passed), cargo test --lib native::albums::tests (10 passed), cargo test --lib native::projects::tests::parse::album_and_record_predicates_use_top_level_type_names (1 passed), git diff --check, and no remaining epic symbols.

## Dependencies

- **Blocks:** [bob-cli-k3.2.1.2](bob-cli-k3.2.1.2.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-k3.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-k3.2.1.1.md) | [bob-cli-k3.2.1.1](bob-cli-k3.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f977009`](https://github.com/bobs-org/bob-cli/commit/f977009a26f64775b377c27ed885fdf61ef6f1da) | feat(albums): parse declarations through shared schema validation | [bob-cli-k3.2.1.1](bob-cli-k3.2.1.1.md) | 2026-11-11 06:00:18 EST |
