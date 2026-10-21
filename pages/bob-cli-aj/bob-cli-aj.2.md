# Bead: bob-cli-aj.2 — Bob Mac Capture relation-card trigger and label-range fixes

[Bead Pages](../README.md) / [bob-cli-aj](README.md) / bob-cli-aj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12t.md) · **Assignee:** `bob-cli-aj.2` · **Size:** medium
**Created:** 2026-10-21 08:01:49 EDT · **Closed:** 2026-10-21 09:45:56 EDT
**Plan:** [202610/relation\_pipe\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_pipe_card.md)

## Description

mac: forward a typed `|` to the rewrite lane and request completion afterwards, read the token from bob's `relation` object, replace only the label range, and update tests, fixtures, and docs.

## Notes

[2026-10-21T13:45:56Z · bob-cli-aj.2--5] Completed the Mac relation-card trigger and label-range work. Verified portable-check, docs-check, and the isolated Mac Scripts/bundle.sh plus just typecheck-tests run; epic-symbol check reports no remaining symbols.

## Dependencies

- **Depends on:** [bob-cli-aj.1](bob-cli-aj.1.md) ✓ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aj.2.md) | [bob-cli-aj.2](bob-cli-aj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@bf40f48`](https://github.com/bobs-org/bob-mac-capture/commit/bf40f48c465378ad175fdc8817f6a95f8c0f54da) | feat(capture): open relation label cards from typed pipe | [bob-cli-aj.2](bob-cli-aj.2.md) | 2026-10-21 09:46:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-aj.2--5][1] | Need the phase scope, design file, and prior notes before finishing assigned work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aj.2.md

<!-- sase:referenced-by:end -->
