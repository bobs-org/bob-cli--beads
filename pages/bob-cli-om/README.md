# Bead: bob-cli-om — Wikilink completion in Bob's prose prompts

[Bead Pages](../README.md) / bob-cli-om

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.land`
**Created:** 2026-11-21 10:32:17 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/prose_wikilink_completion.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md

<!-- sase:links:end -->

## Description

Typing `[[` in any Bob-owned field that writes Markdown prose into the vault (intentions, Work/Rotten/Cancel/Schedule Log reasons, record text, notebook summaries, the Mac Pull-In reason) opens one consistent LINK band that inserts exactly the link it shows, never submits a half-typed link, never touches text after the caret, and never writes the vault. Identifier and filter fields stay literal.

## Notes

[2026-11-21T19:13:56Z · bob-cli-o6.6.1.5] DISCOVERED ISSUE: this epic's nav doc additions pushed bob-plugins docs/bob-navigation-hotkeys.md past the 6000-word reference cap. On a clean worktree at bob-plugins 24bc9cc, npm run docs:check lint exits 1 with 'docs/reference/plugins/bob-navigation-hotkeys.md:1: budget: over budget at 6302 words (cap 6000 for reference/)'; plugin-apis.md also warns at 8274/8000. wc growth: 983076e 8631 -> 79fe2e1 (om.3) 8918 -> 24bc9cc (om.4) 8973. The landing should trim the page back under the cap (tracked by task bob-cli-ob, now +1'd with this evidence). Reported by bob-cli-o6.6.1.5.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-om.1](bob-cli-om.1.md) | Fix bob's wikilink field range and ranking, publish shared vectors | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.10](bob-cli-om.10.md) | Prose-field role lint and end-to-end walkthrough | ◐ in_progress | small | 2026-11-21 | 1 | 1 |
| [bob-cli-om.2](bob-cli-om.2.md) | Obsidian link engine (field model, ranking port, metadata index) | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.3](bob-cli-om.3.md) | proseField controller, LINK band, and the Work summary pilot | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.4](bob-cli-om.4.md) | Standalone modal prompts | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.5](bob-cli-om.5.md) | Task Card stages and the scheduled inline reason | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.6](bob-cli-om.6.md) | Intention Card fields | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.7](bob-cli-om.7.md) | Record Card typed stages and link-stage convergence | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-om.8](bob-cli-om.8.md) | bob capture-complete --links-only | ✓ closed | small | 2026-11-21 | 1 | 1 |
| [bob-cli-om.9](bob-cli-om.9.md) | Mac Pull-In reason link band | ✓ closed | medium | 2026-11-21 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-om: Wikilink completion in Bob's prose prompts [in_progress]"]
    n1["bob-cli-om.1: Fix bob's wikilink field range and ranking, publish shared vectors [closed]"]
    n2["bob-cli-om.10: Prose-field role lint and end-to-end walkthrough [in_progress]"]
    n3["bob-cli-om.2: Obsidian link engine (field model, ranking port, metadata index) [closed]"]
    n4["bob-cli-om.3: proseField controller, LINK band, and the Work summary pilot [closed]"]
    n5["bob-cli-om.4: Standalone modal prompts [closed]"]
    n6["bob-cli-om.5: Task Card stages and the scheduled inline reason [closed]"]
    n7["bob-cli-om.6: Intention Card fields [closed]"]
    n8["bob-cli-om.7: Record Card typed stages and link-stage convergence [closed]"]
    n9["bob-cli-om.8: bob capture-complete --links-only [closed]"]
    n10["bob-cli-om.9: Mac Pull-In reason link band [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n1 -.-> n3
    n1 -.-> n9
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n4 -.-> n8
    n5 -.-> n2
    n6 -.-> n2
    n7 -.-> n2
    n8 -.-> n2
    n9 -.-> n10
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-om.1.md) | [bob-cli-om.1](bob-cli-om.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.10/README.md) | [bob-cli-om.10](bob-cli-om.10.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.2/README.md) | [bob-cli-om.2](bob-cli-om.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.3/README.md) | [bob-cli-om.3](bob-cli-om.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.4/README.md) | [bob-cli-om.4](bob-cli-om.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.5/README.md) | [bob-cli-om.5](bob-cli-om.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.6/README.md) | [bob-cli-om.6](bob-cli-om.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md) | [bob-cli-om.7](bob-cli-om.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.8/README.md) | [bob-cli-om.8](bob-cli-om.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-om.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.9/README.md) | [bob-cli-om.9](bob-cli-om.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-om.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.land/README.md) | [bob-cli-om](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`746f4d5`](https://github.com/bobs-org/bob-cli/commit/746f4d5a4aa5ada921ca8bce5d454a473ab4d0ed) | fix(capture): preserve wikilink fields and rank candidates | [bob-cli-om.1](bob-cli-om.1.md) | 2026-11-21 11:23:05 EST |
| bob-plugins | [`bob-plugins@92f643d`](https://github.com/bobs-org/bob-plugins/commit/92f643dea982b557cd08200f532fd4e82749a2ad) | feat(nav): add prose wikilink link engine (field model, ranking, metadata index) | [bob-cli-om.2](bob-cli-om.2.md) | 2026-11-21 11:38:13 EST |
| bob-cli | [`270b5b2`](https://github.com/bobs-org/bob-cli/commit/270b5b23fb38d15663c68efd85f3bde4161d4bd6) | feat(capture-complete): add -L/--links-only and -S/--source-note | [bob-cli-om.8](bob-cli-om.8.md) | 2026-11-21 12:21:19 EST |
| bob-plugins | [`bob-plugins@79fe2e1`](https://github.com/bobs-org/bob-plugins/commit/79fe2e15e25956aa913944d97cb8605f5ad65ad6) | feat(nav): add proseField LINK band and Work summary \[\[ pilot | [bob-cli-om.3](bob-cli-om.3.md) | 2026-11-21 12:31:56 EST |
| bob-plugins | [`bob-plugins@cdd9df7`](https://github.com/bobs-org/bob-plugins/commit/cdd9df707ad1f2b1d1a1ff23a6c5ee2f920067fb) | feat(nav): complete \[\[ links in Task Card reason stages and the scheduled inline reason | [bob-cli-om.5](bob-cli-om.5.md) | 2026-11-21 13:44:18 EST |
| bob-plugins | [`bob-plugins@24bc9cc`](https://github.com/bobs-org/bob-plugins/commit/24bc9cc6f87df9366afe17d121503cdb5a47408d) | feat(nav): wire \[\[ completion into the standalone modal prompts | [bob-cli-om.4](bob-cli-om.4.md) | 2026-11-21 14:03:19 EST |
| bob-plugins | [`bob-plugins@da0737b`](https://github.com/bobs-org/bob-plugins/commit/da0737b159bb9465fbb3836c8e7720f4510c1455) | feat(ledger-tools): complete \[\[ wikilinks in the Intention Card fields | [bob-cli-om.6](bob-cli-om.6.md) | 2026-11-21 14:23:32 EST |
| bob-plugins | [`bob-plugins@e6d7aed`](https://github.com/bobs-org/bob-plugins/commit/e6d7aed7fdc21825d56a785618e730e56af86a0b) | feat(ledger-tools): complete \[\[ links in the Record Card typed stages | [bob-cli-om.7](bob-cli-om.7.md) | 2026-11-21 14:36:58 EST |
| bob-plugins | [`bob-plugins@c2e28ca`](https://github.com/bobs-org/bob-plugins/commit/c2e28cad167df64c11f373c8c98be5d3fb79ef74) | feat(bob-plugins): lint prose field roles and add walkthrough | [bob-cli-om.10](bob-cli-om.10.md) | 2026-11-21 15:03:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.5][1] | Check epic notes for an existing DISCOVERED ISSUE about the nav docs budget | 2 |
| read-by | [agent:bob-cli-om.2][2] | Need epic plan and decisions context | 1 |
| read-by | [agent:bob-cli-om.6][3] | Check sibling phase states and epic notes | 1 |
| read-by | [agent:bob-cli-om.7][4] | see sibling phase status and notes | 1 |
| read-by | [agent:bob-cli-om.8][5] | Need epic plan and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-o6.6.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.8/README.md

<!-- sase:referenced-by:end -->
