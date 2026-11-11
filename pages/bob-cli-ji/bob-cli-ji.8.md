# Bead: bob-cli-ji.8 — Finish private event notes — correctness fixes and the missing extras

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.8

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.land`
**Created:** 2026-11-10 22:31:45 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_private_gcal_event_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md

<!-- sase:links:end -->

## Description

Close the gaps the bob-cli-ji land audit found in `bob gcal note`: previews that show a stale note, options that are silently swallowed as note text, orphan clear commands that fail, an account-blind note fold, held rows reported as updates, and an incomplete extras phase (`-e`, `-A`, the doctor `notes` check, and the fragile-description hint). Every fix ships with tests, and the JSON stays compatible with Bob Mac Capture.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.land/README.md) | [bob-cli-ji.8](bob-cli-ji.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.8.1][1] | Need epic DECISIONS that this phase must honor | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md

<!-- sase:referenced-by:end -->
