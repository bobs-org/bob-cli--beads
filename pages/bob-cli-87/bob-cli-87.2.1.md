# Bead: bob-cli-87.2.1 — Obsidian snapshot view core

[Bead Pages](../README.md) / [bob-cli-87.2](bob-cli-87.2.md) / bob-cli-87.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) · **Assignee:** `bob-cli-87.2.1.land`
**Created:** 2026-10-16 07:26:12 EDT · **Closed:** 2026-10-16 11:28:28 EDT
**Plan:** [202610/snapshot\_view\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/snapshot_view_core.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:015da024c10eb8fd59ecb5fc | attached via sase artifact create --bead |
| related | file:explicit:28b089609636028ae170391f | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md

<!-- sase:links:end -->

## Description

Vault notes project into a tested engine-neutral view and the agreed Markdown contract, with Obsidian resolution, bounded embeds, and consistent source reads.

## Notes

[2026-10-16T14:48:18Z · bob-cli-87.2.1.land] LAND FOLLOW-UP TRIAGE: Reviewed all child notes; the only PROPOSED FOLLOW-UP is bob-cli-87.2.1.4 note #1, containing two command-metadata failures. Independently reproduced both on clean a086cd9 (file:explicit:28b089609636028ae170391f). /sase_new_task searches and the one-week all-status task sweep found no semantic duplicate. Closed bob-cli-4j covers the earlier ref create:audio omission, not these new template arguments, so no +1 or reopen. Both failures trace to 31528a1 / bob-cli-8b.2 and were recorded together as a DISCOVERED ISSUE on active epic bob-cli-8b, with separate remedies. No standalone tasks created; no proposal declined as invalid. These failures are unrelated to snapshot work and must not block its close after snapshot repairs pass.

[2026-10-16T14:52:54Z · bob-cli-87.2.1.land] LAND AUDIT at a086cd9: Read this epic, all four child scopes and every child note, approved child/outer plans and inherited DECISIONS, epic commits 426b07c/29f5f4e/8da6615/a086cd9, and actual classify/resolve/view/obsidian/serialize/transclusion source and tests. Existing snapshot suite: 81 passed; audio URI extraction tests: 2 passed. Read-once source store, typed view, bounded full/heading/block embeds, deterministic guards, and no-vault-write boundary are present. DECISIONS honored: no memory changes; outer text-layer/plugin branches remain with their owners. Intervening commits reviewed: 1a57e47 profile requires shared-contract integration; c1b1cef/31528a1 templates and 298ebdf cleanup docs require no snapshot behavior integration. master matches origin/master; no PR base. Audit probes (temporary, now removed) found six epic-caused failures: whole-line remote image parser makes zero progress; paragraph/list/heading block-ID anchors disappear; prelude heading collides with authored Snapshot content; explicit self-link picks the first ambiguous heading; code comments hide later indexed headings; raw task bodies lose source comments. Pandoc confirms strike splitting emits literal delimiters/loses formatting; LabeledRow omits .label; profile tests still use a separate contract fixture. Source review additionally found inline note/image embeds silently downgraded to links contrary to the approved content policy. Evidence with exact regression patch and output: file:explicit:015da024c10eb8fd59ecb5fc. These remain epic work and prevent close. A validated medium tale, sase_plan_snapshot_view_landing_repairs.md, covers only these repairs and final closeout of this epic and phase bob-cli-87.2 in its coder turn, without waiting for its own commit. Both epic-symbols checks are empty; justfile has no symvision recipe. Follow-up triage is complete in the preceding note. Full just check is reserved for the repaired tree; no check-full was run.

[2026-10-16T15:28:28Z · bob-cli-87.2.1.land--1] Completed the landing repairs: parser dispatch now advances on remote or unhandled images and preserves inline images/note embeds; typed anchors are emitted on headings, prose, and list items, namespaced in repeated embeds, and collision-safe for the prelude; fragment indexing protects code comments and ambiguous self-links never invent targets; parsed task records retain original comment-bearing source bodies; serializer emits .label rows and preserves strike formatting around lifted links; the profile and serializer now share the complete contract fixture. Focused snapshot tests and the two audio URI tests passed earlier in this session. Monitored just check ran 51 tests successfully and failed only the two documented clean-base capture-templates metadata and native-path-count assertions, matching file:explicit:28b089609636028ae170391f; their remediation remains recorded on active bob-cli-8b, with no duplicate task, and bob-cli-4j remains unrelated. Reviewed prior landing history and current bc27d52 (README/install_all only; no relevant drift). git diff --check is clean. epic-symbols is empty; just symvision is unavailable.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.land.md) | [bob-cli-87.2.1](bob-cli-87.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`71be24a`](https://github.com/bobs-org/bob-cli/commit/71be24aec573ff43d07235fdd4180b781af31d4e) | fix(snapshot): complete view landing repairs | [bob-cli-87.2.1](bob-cli-87.2.1.md) | 2026-10-16 11:29:38 EDT |
| bob-cli--plans | [`bob-cli--plans@f55b439`](https://github.com/bobs-org/bob-cli--plans/commit/f55b439bfc4dc0dac70d23b46ec5eed1d32e8af7) | docs(snapshot): mark view core plan done | [bob-cli-87.2.1](bob-cli-87.2.1.md) | 2026-10-16 11:31:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.2.1.1--4][1] | Need governing epic decisions for the model-contract phase | 1 |
| read-by | [agent:bob-cli-87.2.1.2][2] | parent epic scope | 2 |
| read-by | [agent:bob-cli-87.2.1.3][3] | need epic DECISIONS for phase work | 1 |
| read-by | [agent:bob-cli-87.2.1.land--1][4] | Confirm the child epic's direct parent and recorded landing close | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.land.md

<!-- sase:referenced-by:end -->
