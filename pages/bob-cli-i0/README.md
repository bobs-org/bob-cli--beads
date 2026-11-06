# Bead: bob-cli-i0 — just install-all: a wait worth sitting through

[Bead Pages](../README.md) / bob-cli-i0

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.land`
**Created:** 2026-11-06 15:11:24 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/install_all_wait_and_whats_new.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md

<!-- sase:links:end -->

## Description

`just install-all` (and plain `just install`) stop looking hung during their long bob-cli and Bob Mac Capture builds. All three repos are pulled first, then one fit-to-screen "What's new" digest shows the commits since each repo's last successful install on this host, with full messages when they fit. Each build then runs behind one live status line: activity, elapsed time, and an ETA that only per-host history of comparable builds can earn. Compiler chatter goes to a log, failures print an excerpt, and the run ends with a summary, a terminal bell, and on macOS a Notification Center banner. A missing or failing helper always falls back to today's behavior.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-i0.1](bob-cli-i0.1.md) | install\_ui package core, state store, and script test harness | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.2](bob-cli-i0.2.md) | What's new digest engine | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.3](bob-cli-i0.3.md) | Live status line runner and build history | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.4](bob-cli-i0.4.md) | Pull everything first, print the digest, end with a signal | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.5](bob-cli-i0.5.md) | Route builds and plugin sync through the live line | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.6](bob-cli-i0.6.md) | Earned ETA ranges, plan line, and comparative summary | ✓ closed | medium | 2026-11-06 | 1 | 1 |
| [bob-cli-i0.7](bob-cli-i0.7.md) | Docs refresh and real-terminal acceptance | ✓ closed | small | 2026-11-06 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-i0: just install-all: a wait worth sitting through [in_progress]"]
    n1["bob-cli-i0.1: install_ui package core, state store, and script test harness [closed]"]
    n2["bob-cli-i0.2: What's new digest engine [closed]"]
    n3["bob-cli-i0.3: Live status line runner and build history [closed]"]
    n4["bob-cli-i0.4: Pull everything first, print the digest, end with a signal [closed]"]
    n5["bob-cli-i0.5: Route builds and plugin sync through the live line [closed]"]
    n6["bob-cli-i0.6: Earned ETA ranges, plan line, and comparative summary [closed]"]
    n7["bob-cli-i0.7: Docs refresh and real-terminal acceptance [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n5
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.1/README.md) | [bob-cli-i0.1](bob-cli-i0.1.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.2/README.md) | [bob-cli-i0.2](bob-cli-i0.2.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.3/README.md) | [bob-cli-i0.3](bob-cli-i0.3.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.4/README.md) | [bob-cli-i0.4](bob-cli-i0.4.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.5/README.md) | [bob-cli-i0.5](bob-cli-i0.5.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.6/README.md) | [bob-cli-i0.6](bob-cli-i0.6.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.7/README.md) | [bob-cli-i0.7](bob-cli-i0.7.md) | 1 |
| [bbugyi200.athena.bob-cli-i0.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.land/README.md) | [bob-cli-i0](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`10be962`](https://github.com/bobs-org/bob-cli/commit/10be96258b86bdf3ad8bdc6cabd5ae34e71e7bf0) | feat(install): add install\_ui core, watermarks, and script tests | [bob-cli-i0.1](bob-cli-i0.1.md) | 2026-11-06 15:33:58 EST |
| bob-cli | [`4fd782a`](https://github.com/bobs-org/bob-cli/commit/4fd782a3c172e732244a7625b2c236bcbd1f3600) | feat(install): add What's new digest engine | [bob-cli-i0.2](bob-cli-i0.2.md) | 2026-11-06 15:56:29 EST |
| bob-cli | [`9ade2d6`](https://github.com/bobs-org/bob-cli/commit/9ade2d64ac64a5935512501890d550224f592940) | feat(install): pull everything first, print the digest, end with a signal | [bob-cli-i0.4](bob-cli-i0.4.md) | 2026-11-06 16:10:16 EST |
| bob-cli | [`d9b190f`](https://github.com/bobs-org/bob-cli/commit/d9b190f30a298bd89391cf35c01dd4051d1fe9a0) | feat(install): add live build runner and history | [bob-cli-i0.3](bob-cli-i0.3.md) | 2026-11-06 16:24:45 EST |
| bob-cli | [`d5e49b1`](https://github.com/bobs-org/bob-cli/commit/d5e49b172c9299ec6bbb60cc866aa29025e426f5) | feat(install): route builds through the live runner | [bob-cli-i0.5](bob-cli-i0.5.md) | 2026-11-06 17:02:10 EST |
| bob-cli | [`a3238f7`](https://github.com/bobs-org/bob-cli/commit/a3238f70b4582cedb6c2c7fe8f2859d077a783ee) | feat(install): earn ETA ranges, plan line, and summary comparison | [bob-cli-i0.6](bob-cli-i0.6.md) | 2026-11-06 17:28:43 EST |
| bob-cli | [`a435a8e`](https://github.com/bobs-org/bob-cli/commit/a435a8e134f0a92a99b3e4e45b8fa5ad6cbc763e) | docs(install): document live install flow | [bob-cli-i0.7](bob-cli-i0.7.md) | 2026-11-06 17:43:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-i0.2][1] | Need epic scope for phase i0.2 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.2/README.md

<!-- sase:referenced-by:end -->
