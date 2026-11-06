# Bead: bob-cli-hg.3.1 — Gmail message model and inert body renderer

[Bead Pages](../README.md) / [bob-cli-hg.3](bob-cli-hg.3.md) / bob-cli-hg.3.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.land`
**Created:** 2026-11-05 13:16:21 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_mail_body.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md

<!-- sase:links:end -->

## Description

Complete bob-cli-hg.3 with a pure, tested renderer that preserves readable email content while preventing sender text from becoming active vault syntax.

## Notes

[2026-11-05T20:16:24Z · 18r--code] DISCOVERED ISSUE: On bob-cli HEAD df9178df, just lint fails with denied clippy::derivable_impls at src/native/gmail/body/mime.rs:27, introduced in commit df9178df while modeling the Gmail MIME inventory. The lint report is attached to bob-cli-24 as file:explicit:30cd9d60cfa6efcdb1acf197. This falls within the active Gmail renderer scope.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.land/README.md) | [bob-cli-hg.3.1](bob-cli-hg.3.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.3.1.1][1] | Need the governing epic decisions and plan context for this phase | 2 |
| read-by | [agent:bob-cli-hg.3.1.2][2] | Need parent epic DECISIONS and child phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.2/README.md

<!-- sase:referenced-by:end -->
