# Bead: bob-cli-hz.2 — Bob capture-rewrite relation grammar

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.2` · **Size:** medium
**Created:** 2026-11-06 12:50:21 EST · **Closed:** 2026-11-06 14:04:25 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

bob-grammar: in bob-cli capture-rewrite, an `=` opener replaces the relation `-` alias, `~~=` gives `~`, and a new `toggle_relation_direction` rule flips a complete token on a glued `~`/`=`. Ships with docs, help, and tests as `feat(capture)!`.

## Notes

[2026-11-06T19:04:25Z · bob-cli-hz.2--1] Closed by explicit `sase stitch create -B close` after create_commit landed 0869f792 ("feat(capture)!: rewrite relation directions"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-hz.2` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-hz.3](bob-cli-hz.3.md) ◐ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hz.5](bob-cli-hz.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.2.md) | [bob-cli-hz.2](bob-cli-hz.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hz.2--1][1] | Resume after monitored verification passed but host completion rejected stale fingerprint and missing stage evidence | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.2.md

<!-- sase:referenced-by:end -->
