# Bead: bob-cli-cc — Exact code-block copy from Bob Refs, and Command-Y in Highlights

[Bead Pages](../README.md) / bob-cli-cc

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.land`
**Created:** 2026-10-26 09:00:55 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_code_block_copy.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-ci][2] | Active epic cc's Mac phases (cc.7-cc.9) touch the same RefsPanelModel Highlights paths; cc.7's new Copy test also fails |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ci/README.md

<!-- sase:links:end -->

## Description

While reading a bob-rendered reference in Highlights, Command-Y C Return puts the code block on the current page on the clipboard byte for byte (tabs, indentation, long lines, Mermaid source). The original Markdown of every new reference is preserved in the vault, one key (M) away, and `bob ref code` gives agents and the CLI the same data.

## Notes

[2026-10-26T16:41:38Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land] DISCOVERED ISSUE (from batch-13 lander bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land, 2026-10-26 ~12:45 EDT): `just check` on master 5e8c6ecd fails in code from this epic.

(1) The lib tests did not compile. cc.5's a6d3ecbf test `frozen_frontmatter_keeps_source_markdown_pointer` (src/native/highlights_ref/overwrite.rs:2068) called `render_frozen_note` with 10 args. c9.5.1's 38a02d7b had already dropped the `ref_type`/`stem` params (8 args). Error E0061, so clippy --all-targets and every `cargo test --lib` failed. The batch-13 landing commit FIXES this by removing the two stale args. No action needed beyond rebasing.

(2) After that fix, these still fail (they first reproduced on cc.4's fb28faa1 in batch-13 phase .1's note #6, monitor bf362a42xf4d):
- `native::catalog::tests::public_leaves_are_entries_or_excluded` (src/native/catalog/tests.rs:122): public leaf ["ref", "code"] is neither an entry nor excluded.
- `native::completion::kinds::tests::every_value_arg_has_a_decision` (src/native/completion/kinds.rs:721): missing decisions for `ref code:number` and `ref code:page`.
- `help::ref_help_matches_grouped_snapshot` (tests/cli/help.rs:1001): the ref help fixture lacks the new code row/example.

(3) This is new since cc.5's a6d3ecbf: `native::highlights_ref::source_store::tests::inspect_reports_dangling_mismatch_missing_orphan_and_history` panics at src/native/highlights_ref/source_store.rs:1358 with `saved + missing-catalog source.md`, left 1, right 2.

Totals: lib 3617 passed / 3 failed / 1 ignored; cli 2227 passed / 1 failed; all other binaries passed. Log: /tmp/b13_land_check2.log on athena. No task bead was created, because these belong to this active epic's lander.

[2026-10-26T16:49:15Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land] DISCOVERED ISSUE (batch-13 lander, Mac CI): RefsPanelModelTests.testHighlightsCopyShowStashesAndLibraryRestoresTheFilter, added by cc.7 (bob-mac-capture 7b9bbdd), has failed in every master macOS CI run since it landed: 40334595958 (7b9bbdd), 40354939648 (672ee8a), 40358201800 (d8a828f, cc.8). At d8a828f: RefsPanelModelTests.swift:3540 XCTAssertTrue failed; :3558 nil != "ref/chat/small_reading.md". This matches the restore-selection pattern of the six pre-existing failures from 14b's 1311536 Highlights-key session, now tracked as bob-cli-ci. The cc lander should confirm whether its new test inherits that baseline or is its own regression before landing.

[2026-10-26T16:53:15Z · bob-cli-c9.land] DISCOVERED ISSUE (from bob-cli-c9.land; includes bob-cli-c9.6 PROPOSED FOLLOW-UP note 1): master just check and docs-check are red from this epic's phases, reproduced on 5e8c6ecd on athena and in CI runs 40351653996/40356912584 (ubuntu+macOS). (1) cc.4 fb28faa1 'bob ref code': native::completion::kinds::tests::every_value_arg_has_a_decision ('value-taking args without a kinds decision: ["ref code:number", "ref code:page"]'), native::catalog::tests::public_leaves_are_entries_or_excluded ('public leaf ["ref", "code"] is neither an entry nor excluded'), and tests/cli help::ref_help_matches_grouped_snapshot (the grouped bob ref help now lists 'code' and a 'bob ref code ea_graph 2 | pbcopy' example; snapshot not updated). (2) cc.5 a6d3ecbf: source_store::tests::inspect_reports_dangling_mismatch_missing_orphan_and_history fails deterministically in isolation (health.saved 1 vs expected 2, 'saved + missing-catalog source.md'). (3) cc.3 009060f9: just docs-check lint fails 'src/native/highlights_ref/source_store.rs:185: undocumented production environment name BOB_TEST_FIXTURE_PDF; document it in docs/reference/configuration.md or add a reasoned exact exception' (lint stops docs-check before later gates). Also FYI, already fixed by bob-cli-c9.land in its landing commit: a6d3ecbf's new overwrite.rs unit test called render_frozen_note with the old 10-argument signature (bob-cli-c9.5.1 landing 38a02d7b cut it to 8), so lib tests and clippy --all-targets did not compile; the call now drops the ref_type/stem arguments.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-cc.1](bob-cli-cc.1.md) | Keep bob's note walkers out of .bob | ✓ closed | small | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.10](bob-cli-cc.10.md) | Decision records | ◐ in_progress | xsmall | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.2](bob-cli-cc.2.md) | Render-time code catalog on both pandoc routes | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.3](bob-cli-cc.3.md) | Write-once source store and the source\_markdown pointer | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.4](bob-cli-cc.4.md) | bob ref code read surface | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.5](bob-cli-cc.5.md) | Overwrite repointing and the doctor sources check | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.6](bob-cli-cc.6.md) | Verified attach of existing references' sources | ○ open | medium | 2026-10-26 | 1 | 0 |
| [bob-cli-cc.7](bob-cli-cc.7.md) | Command-Y takeover in Highlights and type-ahead | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.8](bob-cli-cc.8.md) | RefsCore code catalog, C and M rows, and the code picker model | ✓ closed | medium | 2026-10-26 | 1 | 1 |
| [bob-cli-cc.9](bob-cli-cc.9.md) | Code picker, preview well, and panel wiring | ✓ closed | medium | 2026-10-26 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-cc: Exact code-block copy from Bob Refs, and Command-Y in Highlights [in_progress]"]
    n1["bob-cli-cc.1: Keep bob's note walkers out of .bob [closed]"]
    n2["bob-cli-cc.10: Decision records [in_progress]"]
    n3["bob-cli-cc.2: Render-time code catalog on both pandoc routes [closed]"]
    n4["bob-cli-cc.3: Write-once source store and the source_markdown pointer [closed]"]
    n5["bob-cli-cc.4: bob ref code read surface [closed]"]
    n6["bob-cli-cc.5: Overwrite repointing and the doctor sources check [closed]"]
    n7["bob-cli-cc.6: Verified attach of existing references' sources [open]"]
    n8["bob-cli-cc.7: Command-Y takeover in Highlights and type-ahead [closed]"]
    n9["bob-cli-cc.8: RefsCore code catalog, C and M rows, and the code picker model [closed]"]
    n10["bob-cli-cc.9: Code picker, preview well, and panel wiring [closed]"]
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
    n1 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n5 -.-> n7
    n5 -.-> n9
    n6 -.-> n2
    n8 -.-> n9
    n9 -.-> n10
    n10 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.1/README.md) | [bob-cli-cc.1](bob-cli-cc.1.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.10/README.md) | [bob-cli-cc.10](bob-cli-cc.10.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-cc.2.md) | [bob-cli-cc.2](bob-cli-cc.2.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md) | [bob-cli-cc.3](bob-cli-cc.3.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.4/README.md) | [bob-cli-cc.4](bob-cli-cc.4.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md) | [bob-cli-cc.5](bob-cli-cc.5.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.6/README.md) | [bob-cli-cc.6](bob-cli-cc.6.md) | 0 |
| [bbugyi200.athena.bob-cli-cc.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.7/README.md) | [bob-cli-cc.7](bob-cli-cc.7.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-cc.8.md) | [bob-cli-cc.8](bob-cli-cc.8.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.9/README.md) | [bob-cli-cc.9](bob-cli-cc.9.md) | 1 |
| [bbugyi200.athena.bob-cli-cc.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.land/README.md) | [bob-cli-cc](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01f7ec9`](https://github.com/bobs-org/bob-cli/commit/01f7ec972ccbe499ca46dc1e377023c0c32bdf92) | fix(vault): keep note walkers out of .bob | [bob-cli-cc.1](bob-cli-cc.1.md) | 2026-10-26 09:20:31 EDT |
| bob-mac-capture | [`bob-mac-capture@7b9bbdd`](https://github.com/bobs-org/bob-mac-capture/commit/7b9bbddabfd2b3368bb77287842e045f677cabb7) | feat(refs): Command-Y takeover opens the Copy card from Highlights | [bob-cli-cc.7](bob-cli-cc.7.md) | 2026-10-26 09:53:32 EDT |
| bob-cli | [`c7ced49`](https://github.com/bobs-org/bob-cli/commit/c7ced497d875f5c569d1a324ca9ac5a59a6e49eb) | feat(highlights-ref): build render-time code catalog | [bob-cli-cc.2](bob-cli-cc.2.md) | 2026-10-26 10:32:44 EDT |
| bob-cli | [`009060f`](https://github.com/bobs-org/bob-cli/commit/009060f9b4b2b09f67c1d7754a23c9c64923a412) | feat(highlights-ref): write-once source store and source\_markdown pointer | [bob-cli-cc.3](bob-cli-cc.3.md) | 2026-10-26 11:18:37 EDT |
| bob-cli | [`fb28faa`](https://github.com/bobs-org/bob-cli/commit/fb28faa1af7094601f2762a03ff681301a836d50) | feat(ref): add saved code catalog read command | [bob-cli-cc.4](bob-cli-cc.4.md) | 2026-10-26 11:40:34 EDT |
| bob-mac-capture | [`bob-mac-capture@d8a828f`](https://github.com/bobs-org/bob-mac-capture/commit/d8a828f173182f7084a1bc40ec276434287873b1) | feat(refs): add code picker and catalog models | [bob-cli-cc.8](bob-cli-cc.8.md) | 2026-10-26 12:20:36 EDT |
| bob-cli | [`a6d3ecb`](https://github.com/bobs-org/bob-cli/commit/a6d3ecbfd4743f2aa9e44e49e9b5bba282f41fec) | feat(highlights-ref): overwrite source store and doctor ref sources | [bob-cli-cc.5](bob-cli-cc.5.md) | 2026-10-26 12:21:15 EDT |
| bob-mac-capture | [`bob-mac-capture@c7a5f37`](https://github.com/bobs-org/bob-mac-capture/commit/c7a5f372f104e3252e47d65d605d1d297aebbdc7) | feat(refs): wire Copy card code picker and preview well | [bob-cli-cc.9](bob-cli-cc.9.md) | 2026-10-26 13:05:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][1] | Need the epic scope to attach ref code catalog and source_store test failures | 2 |
| read-by | [agent:bob-cli-c9.land][2] | Check whether active epic cc owns the ref code help/catalog CI failures and overwrite source-store integration | 1 |
| read-by | [agent:bob-cli-cc.3][3] | Need parent epic plan and design | 1 |
| read-by | [agent:bob-cli-cc.5][4] | Need parent epic scope and sibling phases | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md

<!-- sase:referenced-by:end -->
