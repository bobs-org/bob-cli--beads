# Bead: bob-cli-oj.3 — Album \`walk\_by\` and group-major record walk lines in bob

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.3` · **Size:** large
**Created:** 2026-11-21 07:41:35 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

walk-by-cli: in bob-cli, add the album `walk_by` key (non-list choices field), order `ring_slots` group-major, rewrite at most five walk lines when a record's `walk_by` value changes, report groups and group heads in albums and records JSON with a `record_walk_groups_v1` capability, add the `bob albums update` set/unset op, strip `«`/`»` from walk labels, extend the shared golden vectors, and document it.

## Notes

[2026-11-21T12:49:25Z · bob-cli-oj.3] Planning evidence: inspected clean bob-cli d27041cd and the required audited parent plan/research. No prior phase notes or landed walk_by implementation found. Proposing a child epic with sequential model, record-writes, album-writes, and docs-proof phases; each coding phase is medium. Existing album updates only edit record: spans, record updates do not stage neighbor walk edits, and album fingerprints omit walk configuration. Existing field-key renames are explicitly refused, so preserve that restriction while keeping walk_by references valid for label changes and any future supported rename. The child land agent must verify and close bob-cli-oj.3 only after the full scope is done.

[2026-11-21T12:49:26Z · bob-cli-oj.3] PROPOSED FOLLOW-UP: Decisions-web record for derived group stops remains skipped — inherited memory_decision_group_stops=no forbids this addition; no decisions memory was edited or proposed for implementation. The outer land agent should retain the accepted design contract as evidence and triage the skipped record without overriding that decision.

## Dependencies

- **Blocks:** [bob-cli-oj.4](bob-cli-oj.4.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |
