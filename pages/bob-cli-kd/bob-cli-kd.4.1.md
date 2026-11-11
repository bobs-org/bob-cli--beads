# Bead: bob-cli-kd.4.1 — Weekly bank import with deterministic matching and one guarded commit

[Bead Pages](../README.md) / [bob-cli-kd.4](bob-cli-kd.4.md) / bob-cli-kd.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) · **Assignee:** `bob-cli-kd.4.1.land`
**Created:** 2026-11-11 14:24:04 EST
**Plan:** [202611/bank\_import.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_import.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md

<!-- sase:links:end -->

## Description

Complete bob-cli-kd.4: import posted Wells Fargo QFX/OFX and CSV transactions once, preserve typed rows and edits, journal private identities, and install the Monday PRE chore after the command is verified.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.land/README.md) | [bob-cli-kd.4.1](bob-cli-kd.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.4.1.1][1] | Need parent epic DECISIONS and remaining work notes | 1 |
| read-by | [agent:research.49.cld][2] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.gem][3] | Understand phase 4.1 import implementation status | 1 |
| read-by | [agent:research.49.grk][4] | Need import child-epic phase list so the e2e scorecard is accurate | 1 |
| read-by | [agent:research.49.mus][5] | kd import child epic status for guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
