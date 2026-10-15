# Bead: bob-cli-7r.6 — Bob Mac Capture relationship preview rows, owner header, and notifications

[Bead Pages](../README.md) / [bob-cli-7r](README.md) / bob-cli-7r.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.w0.md) · **Assignee:** `bob-cli-7r.6` · **Size:** medium
**Created:** 2026-10-14 16:21:12 EDT · **Closed:** 2026-10-14 19:53:59 EDT
**Plan:** [202610/capture\_relate\_existing\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_relate_existing_tasks.md)

## Description

mac_preview: give `task_dependency` items an owner header. Render one `⛓`/`🧱` row per relationship for every owner kind, in place of the headline and literal DEPENDS ON row. Stop printing the owner line twice, put the owner card first, and write relationship notification copy. Fixtures, tests, and README.

## Notes

[2026-10-14T23:53:53Z · bob-cli-7r.6--8] PROPOSED FOLLOW-UP: Record existing-owner relationship rules in the decisions memory web — this phase decision_record=false, so no memory file was edited.

[2026-10-14T23:53:59Z · bob-cli-7r.6--8] Implemented relationship rows, owner header/card ordering and suppression, relationship notifications, fixtures/tests/README; just portable-check passed and no phase epic symbols remain. macOS bundle/typecheck remain unverified after the recorded host connection timeout.

## Dependencies

- **Depends on:** [bob-cli-7r.3](bob-cli-7r.3.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7r.5](bob-cli-7r.5.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7r.7](bob-cli-7r.7.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7r.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7r.6.md) | [bob-cli-7r.6](bob-cli-7r.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e5b2ef3`](https://github.com/bobs-org/bob-mac-capture/commit/e5b2ef309916d09ab9967853a94982fc8b2853d5) | feat(mac-capture): add relationship-aware task previews | [bob-cli-7r.6](bob-cli-7r.6.md) | 2026-10-14 19:54:30 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7r.6--8][1] | Verify phase closure and recorded follow-up note | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7r.6.md

<!-- sase:referenced-by:end -->
