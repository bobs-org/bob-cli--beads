# Bead: bob-cli-on.15.1 — Requirements on the Mac Pull-In card

[Bead Pages](../README.md) / [bob-cli-on.15](bob-cli-on.15.md) / bob-cli-on.15.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.land`
**Created:** 2026-11-22 14:56:48 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_requirement_close_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.15 so the Mac Pull-In card presents nested requirement groups, stages their verdicts safely, and submits them through the existing capability-gated bob contract with compiled and tested native UI.

## Notes

[2026-11-23T02:08:48Z · bob-cli-pj.2.1.land] DISCOVERED ISSUE: pj.2.1 lander triaged bob-cli-pj.2.1.3 PROPOSED FOLLOW-UP #1 and independently reproduced just docs-check on bob-cli 29d7fec7 / Mac 33649498. All three fatal budget errors are introduced by this epic phase .5 commit d76a4849: capture-previews 5998→6082, keyboard 5974→6036, protocol 5999→6107 (cap 6000, canonical bob_docs.markdown.count_words). They are not inherited base failures for .5. Trim the additions within this epic while preserving contract facts. Evidence file:explicit:f0ee94709e52d2aa9074a8ad. Existing trackers bob-cli-jz and bob-cli-h9 also received corroboration; no new task.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md) | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.1][1] | Need exact epic decisions, phase notes, and plan metadata | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md

<!-- sase:referenced-by:end -->
