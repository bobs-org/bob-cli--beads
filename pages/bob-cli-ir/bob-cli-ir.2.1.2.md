# Bead: bob-cli-ir.2.1.2 — Lazy per-folder records index and suggestions

[Bead Pages](../README.md) / [bob-cli-ir.2.1](bob-cli-ir.2.1.md) / bob-cli-ir.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.2.md) · **Assignee:** `bob-cli-ir.2.1.2` · **Size:** medium
**Created:** 2026-11-08 11:17:51 EST · **Closed:** 2026-11-08 12:45:06 EST
**Plan:** [202611/records\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/records_engine.md)

## Description

folder-index: implement frontmatter-only folder discovery, case-insensitive stem lookup, diagnostics, collapsed value frequencies, nearest matches, and performance evidence.

## Notes

[2026-11-08T17:37:31Z · bob-cli-ir.2.1.2] Public interfaces for planner-contract: RecordCatalog::new(vault_root) + folder(dir) lazily indexes one folder's immediate Markdown files through the closing frontmatter delimiter (missing folders stay empty and are never created). FolderIndex exposes notes(), lookup_stem (case-insensitive Exact/Ambiguous/None, original spelling/path), nearest_stems/nearest_values (bounded_levenshtein distance 2, top 3), value_suggestions (collapse by case-folded wikilink alias or target stem, insert most-frequent original, count a record once, rank frequency then recency then path), and colliding_path(stem, reserved) for on-disk plus caller-planned paths. IndexedRecord keeps raw Scalar/List/Null fields and MissingTitle/InvalidYaml/NoteRead diagnostics so a bad YAML or missing title still collides. Athena release 500-note evidence: cold=4.35ms, warm-cached=120ns, 5 warm-FS samples 3.11–3.87ms (under 10ms). Two consumers share one read; unrelated folders are not opened.

[2026-11-08T17:45:06Z · bob-cli-ir.2.1.2] just check green; records catalog tests 48 pass (1 ignored timing); athena release 500-note evidence cold=4.349236ms warm_cached=120ns warm_fs_samples=[3.433999ms, 3.865534ms, 3.109619ms, 3.369364ms, 3.541823ms] all under 10ms; no leftover --epic-symbol entries; RecordCatalog/FolderIndex API recorded on the bead for planner-contract

## Dependencies

- **Depends on:** [bob-cli-ir.2.1.1](bob-cli-ir.2.1.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.2.1.4](bob-cli-ir.2.1.4.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.2.1.2/README.md) | [bob-cli-ir.2.1.2](bob-cli-ir.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b9db700`](https://github.com/bobs-org/bob-cli/commit/b9db7007934c7ef97343ba998704934374cf8732) | feat(records): add lazy per-folder catalog index and suggestions | [bob-cli-ir.2.1.2](bob-cli-ir.2.1.2.md) | 2026-11-08 12:46:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.2.1.3][1] | Need sibling phase status to check prior work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.2.1.3/README.md

<!-- sase:referenced-by:end -->
