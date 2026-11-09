# Bead: bob-cli-is.2 — Mac type-ahead hold for meaning-changing rewrite aliases

[Bead Pages](../README.md) / [bob-cli-is](README.md) / bob-cli-is.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3r.linker.w0.md) · **Assignee:** `bob-cli-is.2` · **Size:** medium
**Created:** 2026-11-08 11:42:41 EST · **Closed:** 2026-11-08 15:14:55 EST
**Plan:** [202611/close\_outcome\_x\_s\_typing\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md)

## Description

mac-type-ahead-hold: generalize the past-segment dash Return deferral into a meaning-changing-alias flag. Add a bounded type-ahead hold that buffers key-downs while such a rewrite is in flight and replays them after Bob answers. Its first client is the existing x= dash alias. Mac only.

## Notes

[2026-11-08T20:14:55Z · bob-cli-is.2--6] Green exact-SHA macOS CI on SHA d9c4a17 (run 42516983169): lint, build, test, bundle, plist/signature, launch smoke, and install/reinstall. Prior local checks: docs gate, Mac typecheck-tests and app bundle, athena portable suite 2268 passed/1 skipped. Bounded type-ahead hold covers the x= dash rewrite; replayed x=2~3 uses a relation_grammar parse fixture. No remaining epic symbols.

## Dependencies

- **Blocks:** [bob-cli-is.3](bob-cli-is.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-is.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.2.md) | [bob-cli-is.2](bob-cli-is.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@03392a5`](https://github.com/bobs-org/bob-mac-capture/commit/03392a55eb87577ac8bd1b69c381949cc9e2024b) | feat(mac-capture): hold type-ahead keys during dash rewrite | [bob-cli-is.2](bob-cli-is.2.md) | 2026-11-08 15:16:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-is.2--6][1] | Need remaining notes and verification history before closing | 3 |
| read-by | [agent:bob-cli-is.3][2] | check prior phase landing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.3.md

<!-- sase:referenced-by:end -->
