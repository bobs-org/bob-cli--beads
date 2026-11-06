# Bead: bob-cli-hg.12.1.2 — Outgoing Markdown renderer and attachment snapshots

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.2` · **Size:** medium
**Created:** 2026-11-06 07:12:29 EST · **Closed:** 2026-11-06 10:31:32 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

compose-render: implement conservative HTML/plain output, syntax refusals, flattened links, and validated attachment snapshots from section 4.2.

## Notes

[2026-11-06T15:31:06Z · bob-cli-hg.12.1.2] PROPOSED FOLLOW-UP: just docs-check test_readme_table_matches_original_contract_index_snapshot fails identically on the clean base tree; tracked by bob-cli-hs

[2026-11-06T15:31:32Z · bob-cli-hg.12.1.2] compose-render done: render.rs (conservative HTML+plain, 10 refusal kinds with line numbers, wikilink flattening, declared-embed resolution) and attachments.rs (vault validation, 0700/0600 snapshots, RAII cleanup) with 21 new unit tests; docs/gmail.md gains Outgoing message rendering. Verified: cargo fmt clean, clippy gate exit 0 with no new-file warnings, focused 29 compose tests green, full workspace suite green (5409+3263 passed, 0 failed), just docs-check 446 passed with 1 pre-existing README-snapshot failure also failing on base (tracked by bob-cli-hs). No CLI surface added; tempfile moved from dev-deps to deps for runtime staging.

## Dependencies

- **Depends on:** [bob-cli-hg.12.1.1](bob-cli-hg.12.1.1.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hg.12.1.3](bob-cli-hg.12.1.3.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.2/README.md) | [bob-cli-hg.12.1.2](bob-cli-hg.12.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ee05db4`](https://github.com/bobs-org/bob-cli/commit/ee05db4d8ffeb6714ee90abbcf65d9d7c6215e46) | feat(gmail): add compose render and attachment staging | [bob-cli-hg.12.1.2](bob-cli-hg.12.1.2.md) | 2026-11-06 10:33:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.2][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-hg.12.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md

<!-- sase:referenced-by:end -->
