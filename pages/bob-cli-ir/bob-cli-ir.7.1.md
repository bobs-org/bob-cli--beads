# Bead: bob-cli-ir.7.1 — Existing-record updates through capture and the records CLI

[Bead Pages](../README.md) / [bob-cli-ir.7](bob-cli-ir.7.md) / bob-cli-ir.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.7.md) · **Assignee:** `bob-cli-ir.7.1.land`
**Created:** 2026-11-09 02:47:01 EST · **Closed:** 2026-11-09 07:04:47 EST
**Plan:** [202611/record\_append.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_append.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/record_append.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_append.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ir.7 so capture and bob records update edit existing records without changing unrelated bytes, with accurate previews and guided input.

## Notes

[2026-11-09T11:21:56Z · bob-cli-ir.7.1.land] Lander triage (bob-cli-ir.7.1.land): no child phase recorded any PROPOSED FOLLOW-UP entry, so no /sase_new_task filings were needed. Integration: the only non-epic commit since the epic started is 5e49fa5e (bob-cli-ir.10.1.1, capture-complete -F/--record-field + record.edit); its update-item behavior is folded into the remediation tale, not a separate task. Reviewer findings declined with reasons: (1) current/before values go through validate_field_values, so stored relative-date words and comma-bearing list members are normalized — declined because bob records check uses the same stored-value validator (shared-validator rule); (2) plan_update returns no historical warnings when a supplied field is invalid — declined because those warnings come from the renderer and the refused update already reports its typed error; (3) records new/update -s shell completion emits KEY= and KEY=value rows together — declined because the completion protocol passes no current word and shells prefix-filter; (4) human records update -d prints Markdown without warnings — matches records new; (5) 12641768 bumped GRAMMAR_REVISION 20->21 without a feat(capture)! subject — landed history is immutable and same-day 1c4939b9 feat(records)! already marks the release breaking. Remaining epic-caused gaps (stale collision copy, record_value need on optional-empty updates, update recovery draft dropping parent note, update record.title falling back to note text, record_target rows with grammar-unaddressable stems, symlink alias targets, -F empty bullet on update items, missing record_target key docs, missing parse/CLI unknown/ambiguous target tests) are planned as one tale that ends with this epic's closeout.

[2026-11-09T12:04:47Z · bob-cli-ir.7.1.land] Landed existing-record updates: five phase commits 8cc4a754,12641768,96196052,1c4939b9,a729a8fd plus landing fixes items1-9 (collision copy, optional-empty record_value, recovery draft, update title, addressable target stems, symlink refusal, -F prefill with no-op drop, record_target keys docs, unknown/ambiguous tests) with focused CLI/unit tests; just check pass, docs-check pass

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.7.1.land.md) | [bob-cli-ir.7.1](bob-cli-ir.7.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`941ee72`](https://github.com/bobs-org/bob-cli/commit/941ee724de7c4767e02623585ad62a0893ca98d2) | feat(capture): land existing-record update fixes | [bob-cli-ir.7.1](bob-cli-ir.7.1.md) | 2026-11-09 07:07:20 EST |
| bob-cli--plans | [`bob-cli--plans@2c460ed`](https://github.com/bobs-org/bob-cli--plans/commit/2c460ed80578757da28538e6fab158886d7d3e74) | docs(plans): mark record append landing done | [bob-cli-ir.7.1](bob-cli-ir.7.1.md) | 2026-11-09 07:08:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.7.1.1][1] | Need parent epic DECISIONS and scope | 1 |
| read-by | [agent:bob-cli-ir.7.1.2][2] | Need parent epic decisions and phase status context for assigned work | 1 |
| read-by | [agent:bob-cli-ir.7.1.3][3] | Need parent epic DECISIONS and phase design | 2 |
| read-by | [agent:bob-cli-ir.7.1.4][4] | Need the parent epic decisions and governing phase context | 1 |
| read-by | [agent:bob-cli-ir.7.1.5][5] | Need epic DECISIONS and child status | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.4/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.7.1.5/README.md

<!-- sase:referenced-by:end -->
