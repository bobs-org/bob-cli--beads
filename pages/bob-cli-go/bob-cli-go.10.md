# Bead: bob-cli-go.10 — Capture \`\>\` transfer grammar, execution, and output

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.10` · **Size:** large
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-04 08:36:08 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

transfer-capture: after bob-cli-gm and bob-cli-gl.2 land, recognize `@src+id… > @dest[+id][#name]` in both resolvers before fan-out, execute moves through batch_move and merges through the engine, report moves[] and merges[], add the shell-redirect guard, and bump the grammar once.

## Notes

[2026-11-04T06:49:05Z · bob-cli-go.10] PLANNING: Verified bob-cli-gm and bob-cli-gl.2 are closed and their code is present; no transfer implementation or prior phase work notes exist at 3741ce2e. Authored and validated a five-phase child epic for shared lexer/shell guard, both resolvers and one grammar bump, staged moves, staged merges/offers, and docs/integration. Parent DECISIONS retained; no memory or product changes made. Original phase remains open for the child epic land agent to verify and close after implementation.

[2026-11-04T13:36:28Z · bob-cli-go.10.1.land] Verified by bob-cli-go.10.1 landing: child epic completed every transfer-capture deliverable - claim before fan-out in both resolvers, CaptureKind::Transfer with task_move/task_merge modes and transfer object/spans/needs/coded diagnostics, moves via batch_move in typed order, merges via plan_task_merge (Explicit, first merge label or 'merged into'), resolved duplicate/alias/overlap/destination-is-source refusals, pull_in offers, moves[]/merges[]/repaired_files[] and human lines, shell_ate_transfer_arrow guard, single grammar bump to 10 (706eab67 feat(capture)!), docs (capture.md section, capture-syntax token row + example, search_smoke, json-outputs, compatibility, --help). Landing fixed epic-caused glued-arrow false positives; just check passes; worked capture-parse example reports task_merge + transfer at grammar 10. Only just docs-check generated drift fails, on the pre-existing glossary:task-merge front matter owned by bob-cli-go memory closeout. epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-go.11](bob-cli-go.11.md) ○ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.5](bob-cli-go.5.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.6](bob-cli-go.6.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.md) | [bob-cli-go.10](bob-cli-go.10.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.10.1.1][1] | Need to confirm no memory edits authorized for child | 2 |
| read-by | [agent:bob-cli-go.10.1.5][2] | Need parent phase scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.5/README.md

<!-- sase:referenced-by:end -->
