# Bead: bob-cli-nu — Command chips: one-gesture bob runs from Obsidian notes

[Bead Pages](../README.md) / bob-cli-nu

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.land`
**Created:** 2026-11-20 05:59:33 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/command_chips.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md

<!-- sase:links:end -->

## Description

Typing `run: bob …` in an inline code span, or a `bob-run` fence, gives a quiet ▶ chip. One click or ⌘↵ runs it through Bob Command Mode the way the sheet's Ctrl+Enter would. A chip holds one command or a whole `&&` sequence, and its run state shows in place. The copy-chip plugin becomes `bob-chips` and owns both kinds, and the GTD rows that hold bob commands become command chips.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-nu.1](bob-cli-nu.1.md) | Rename bob-copy-chips to bob-chips with no behavior change | ✓ closed | medium | 2026-11-20 | 1 | 1 |
| [bob-cli-nu.2](bob-cli-nu.2.md) | Command Mode chip engine (resolve, runText, openText, provenance) | ✓ closed | medium | 2026-11-20 | 1 | 1 |
| [bob-cli-nu.3](bob-cli-nu.3.md) | run:/bob-run grammar, command-chip cursor rule, and vectors | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-nu.4](bob-cli-nu.4.md) | Inline command chips in Live Preview and Reading view | ◐ in_progress | large | 2026-11-20 | 1 | 0 |
| [bob-cli-nu.5](bob-cli-nu.5.md) | The bob-run sequence card | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-nu.6](bob-cli-nu.6.md) | ⌘↵ runs the command chip at the cursor, with an armed chip and keycap hint | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-nu.7](bob-cli-nu.7.md) | Mod+Shift+Y makes and edits command chips | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-nu.8](bob-cli-nu.8.md) | GTD rows, guide, glossary, and coordination | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-nu: Command chips: one-gesture bob runs from Obsidian notes [in_progress]"]
    n1["bob-cli-nu.1: Rename bob-copy-chips to bob-chips with no behavior change [closed]"]
    n2["bob-cli-nu.2: Command Mode chip engine (resolve, runText, openText, provenance) [closed]"]
    n3["bob-cli-nu.3: run:/bob-run grammar, command-chip cursor rule, and vectors [in_progress]"]
    n4["bob-cli-nu.4: Inline command chips in Live Preview and Reading view [in_progress]"]
    n5["bob-cli-nu.5: The bob-run sequence card [in_progress]"]
    n6["bob-cli-nu.6: ⌘↵ runs the command chip at the cursor, with an armed chip and keycap hint [in_progress]"]
    n7["bob-cli-nu.7: Mod+Shift+Y makes and edits command chips [in_progress]"]
    n8["bob-cli-nu.8: GTD rows, guide, glossary, and coordination [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n7
    n6 -.-> n8
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.1/README.md) | [bob-cli-nu.1](bob-cli-nu.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-nu.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.2.md) | [bob-cli-nu.2](bob-cli-nu.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-nu.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.3/README.md) | [bob-cli-nu.3](bob-cli-nu.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4/README.md) | [bob-cli-nu.4](bob-cli-nu.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md) | [bob-cli-nu.5](bob-cli-nu.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md) | [bob-cli-nu.6](bob-cli-nu.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.7/README.md) | [bob-cli-nu.7](bob-cli-nu.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.8/README.md) | [bob-cli-nu.8](bob-cli-nu.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-nu.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.land/README.md) | [bob-cli-nu](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@bf13f43`](https://github.com/bobs-org/bob-plugins/commit/bf13f430fade45369de709523c321b72d3761ce3) | feat(plugins): rename bob-copy-chips to bob-chips | [bob-cli-nu.1](bob-cli-nu.1.md) | 2026-11-20 06:50:46 EST |
| bob-plugins | [`bob-plugins@591998e`](https://github.com/bobs-org/bob-plugins/commit/591998e36b0f41e61c3871d24a48478b541e52b5) | feat(bob-command-mode): add chip execution engine and provenance | [bob-cli-nu.2](bob-cli-nu.2.md) | 2026-11-20 07:12:03 EST |
