# Bead: bob-cli-ha — Glue start and past timing to the Pomodoro name

[Bead Pages](../README.md) / bob-cli-ha

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cf.md) · **Assignee:** `bob-cli-ha.land`
**Created:** 2026-11-05 05:23:37 EST
**Plan:** [202611/glued\_start\_timing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/glued_start_timing.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/glued_start_timing.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:eaf3c3a97cb043b51c41c712 | attached via sase artifact create --bead |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/glued_start_timing.md

<!-- sase:links:end -->

## Description

Capture `=` and `x=` tokens take their timing glued to a bare Pomodoro name (`=build-`, `=10-3fix`, `x=fix3`); the `@` and `<X>#` separators are retired with teaching errors, and every client, doc, and test teaches only the shorter spellings.

## Notes

[2026-11-05T14:31:47Z · 18i--code] DISCOVERED ISSUE: `just docs-check` on this working tree fails its executable tutorial at TUTORIAL_FENCE 12 in docs/start/first-bob-day.md:117 because the fence still uses `=#focus`; capture rejects that retired syntax and instructs `=focus`. The preceding docs checks pass. This falls within the active glued-timing epic's documentation scope. Reproduction source: file:explicit:eaf3c3a97cb043b51c41c712.

[2026-11-05T15:28:26Z · 18l--code] DISCOVERED ISSUE: Independent reproduction during the approved reconcile coalescing work: just docs-check passes lint, generated drift, strict site build, published URLs, offline links, edit links, and search smoke, then fails the executable tutorial at TUTORIAL_FENCE 12 in docs/start/first-bob-day.md:117. The example uses =#focus, which capture rejects as retired and teaches =focus. This is within the glued-timing epic's documentation scope; the docs phase was closed but the epic remains in progress. Reproduced on 2026-11-05 with just docs-check.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ha.1](bob-cli-ha.1.md) | \`=\` starts and link \`=\` suffixes (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.2](bob-cli-ha.2.md) | \`x=\` past records (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.3](bob-cli-ha.3.md) | Document the glued spellings (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.4](bob-cli-ha.4.md) | Stop composing \`=#\` hints in Bob Mac Capture | ✓ closed | small | 2026-11-05 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ha: Glue start and past timing to the Pomodoro name [in_progress]"]
    n1["bob-cli-ha.1: `=` starts and link `=` suffixes (bob-cli) [closed]"]
    n2["bob-cli-ha.2: `x=` past records (bob-cli) [closed]"]
    n3["bob-cli-ha.3: Document the glued spellings (bob-cli) [closed]"]
    n4["bob-cli-ha.4: Stop composing `=#` hints in Bob Mac Capture [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ha.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.1.md) | [bob-cli-ha.1](bob-cli-ha.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ha.2/README.md) | [bob-cli-ha.2](bob-cli-ha.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.3.md) | [bob-cli-ha.3](bob-cli-ha.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.4.md) | [bob-cli-ha.4](bob-cli-ha.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ha.land/README.md) | [bob-cli-ha](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01cb7b5`](https://github.com/bobs-org/bob-cli/commit/01cb7b5c3eb75d7353ef4a57014cc5ada1178bf6) | feat(capture): add glued Pomodoro start grammar | [bob-cli-ha.1](bob-cli-ha.1.md) | 2026-11-05 08:11:16 EST |
| bob-cli--plans | [`bob-cli--plans@e1faa69`](https://github.com/bobs-org/bob-cli--plans/commit/e1faa69e2ed28fe8d1e37be27a46ad03514baa61) | chore(plans): record reviewer decision selections | [bob-cli-ha.4](bob-cli-ha.4.md) | 2026-11-05 09:19:23 EST |
| bob-cli | [`d012e78`](https://github.com/bobs-org/bob-cli/commit/d012e782bd3b399021027e58f833ed7ce31bd298) | feat(capture)!: glue past timing to the Pomodoro name | [bob-cli-ha.2](bob-cli-ha.2.md) | 2026-11-05 09:29:58 EST |
| bob-cli | [`4327543`](https://github.com/bobs-org/bob-cli/commit/4327543778cfa446e765a5365abb2e558fdad5c0) | docs(capture): document glued timing spellings | [bob-cli-ha.3](bob-cli-ha.3.md) | 2026-11-05 11:12:44 EST |
