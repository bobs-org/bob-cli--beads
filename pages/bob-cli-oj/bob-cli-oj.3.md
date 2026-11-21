# Bead: bob-cli-oj.3 — Album \`walk\_by\` and group-major record walk lines in bob

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.3` · **Size:** large
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 11:13:04 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

walk-by-cli: in bob-cli, add the album `walk_by` key (non-list choices field), order `ring_slots` group-major, rewrite at most five walk lines when a record's `walk_by` value changes, report groups and group heads in albums and records JSON with a `record_walk_groups_v1` capability, add the `bob albums update` set/unset op, strip `«`/`»` from walk labels, extend the shared golden vectors, and document it.

## Notes

[2026-11-21T12:49:25Z · bob-cli-oj.3] Planning evidence: inspected clean bob-cli d27041cd and the required audited parent plan/research. No prior phase notes or landed walk_by implementation found. Proposing a child epic with sequential model, record-writes, album-writes, and docs-proof phases; each coding phase is medium. Existing album updates only edit record: spans, record updates do not stage neighbor walk edits, and album fingerprints omit walk configuration. Existing field-key renames are explicitly refused, so preserve that restriction while keeping walk_by references valid for label changes and any future supported rename. The child land agent must verify and close bob-cli-oj.3 only after the full scope is done.

[2026-11-21T12:49:26Z · bob-cli-oj.3] PROPOSED FOLLOW-UP: Decisions-web record for derived group stops remains skipped — inherited memory_decision_group_stops=no forbids this addition; no decisions memory was edited or proposed for implementation. The outer land agent should retain the accepted design contract as evidence and triage the skipped record without overriding that decision.

[2026-11-21T16:13:38Z · bob-cli-oj.3.1.land] walk-by-cli complete: albums may declare walk_by as a non-list Choices field; ring_slots are group-major; record membership moves rewrite at most five walk lines in the same guarded transaction; albums/records JSON expose groups and heads with record_walk_groups_v1; walk_by.set string|null is reversible including quoted, commented, and invalid authored spans; «/» are stripped from walk labels; shared vectors remain tests/fixtures/record_walk/vectors.json.

Child epic bob-cli-oj.3.1 and phases .1-.4 are closed with resolution done after landing repairs (YAML scalar decode, authored vs effective, restore locators, emitted-selection bind, explicit unset of invalid keys, capture JSON correction, grouped rollback and mixed-capture regressions). `sase bead epic-symbols` is empty on oj.3 and oj.3.1. justfile has no symvision recipe.

Verification: just fmt passed; just check passed; just install on athena installed bob 0.5.0 at ~/.cargo/bin/bob. just docs-check fails only on pre-existing vault-format.md 6016/6000 (bob-cli-oc / bob-cli-o6). plugin-apis.md 8165/8000 warning remains bob-cli-ob / outer bob-cli-oj. Inherited decisions held: daily_create=yes, walk_more_albums=no, memory_glossary deferred to oj.8, memory_decision_group_stops=no (declined decisions-web stays declined). Integration review of 05c1679a found no grouped-walk changes needed. Live albums unchanged. Outer epic bob-cli-oj and plan:202611/bracket_n_group_jumps.md remain open.

## Dependencies

- **Blocks:** [bob-cli-oj.4](bob-cli-oj.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.3.1.1][1] | Need notes, DECISIONS, design files, and remaining work | 3 |
| read-by | [agent:bob-cli-oj.3.1.3][2] | Need outer phase scope, final decisions, and progress | 1 |
| read-by | [agent:bob-cli-oj.3.1.4][3] | Need outer phase final decisions relevant to grouped walk documentation | 1 |
| read-by | [agent:bob-cli-oj.6][4] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
