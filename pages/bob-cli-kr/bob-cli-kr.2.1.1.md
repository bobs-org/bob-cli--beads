# Bead: bob-cli-kr.2.1.1 — Validate ordered schema operations and their consequences

[Bead Pages](../README.md) / [bob-cli-kr.2.1](bob-cli-kr.2.1.md) / bob-cli-kr.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-kr.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.2.md) · **Assignee:** `bob-cli-kr.2.1.1` · **Size:** medium
**Created:** 2026-11-12 07:56:42 EST · **Closed:** 2026-11-12 09:09:30 EST
**Plan:** [202611/album\_schema\_writer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_schema_writer.md)

## Description

schema-ops: implement the typed update protocol, pure ordered operations, complete-record impact accounting, shared Rust validation, typed refusals, and semantic inverse operations. No public command yet.

## Notes

[2026-11-12T14:09:06Z · bob-cli-kr.2.1.1] schema-ops landed test-only under src/native/albums/update/ (protocol.rs, ops.rs, mod.rs) gated by #[cfg(test)] in albums/mod.rs; no public command. 17 update tests pass; 197 albums+records lib tests pass; cargo fmt clean; workspace clippy gate shows 0 errors. Wire examples for schema-spans: {"schema_version":1,"expect":"sha256:…","ops":[]} no-op; {"op":"album.set","set":{"label":"Eateries"},"unset":["plural"]}; {"op":"field.add","label":"Status","kind":"choices","position":0,"choices":[{"label":"To try"},{"label":"Liked","emoji":"💚"}]}; {"op":"field.set","field":"status","set":{"required":true}}; {"op":"field.move","field":"status","position":0}; {"op":"field.remove","field":"status"}; {"op":"choice.add","field":"status","label":"Regular","emoji":"🔁","position":2}; {"op":"choice.set","field":"status","value":"regular","set":{"label":"Regular","emoji":"🔁"}} (empty emoji removes icon); {"op":"choice.move","field":"status","value":"regular","position":0}; {"op":"choice.remove","field":"status","value":"regular"}. Undo restoration: field.add accepts restore_key, choice.add accepts restore_value; each only creates an absent key, never renames; field.remove inverse is add+follow-up field.set for required/default/min/max. Interfaces for schema-spans: protocol::parse_envelope(&str)->Envelope{expect,ops}; ops::apply_ops(&[Op],&ApplyInputs)->OpOutcome{after_raw,after_type,after_plural,per_op,derived_keys,consequence,inverse_ops,group_before/after}; ops::ApplyInputs{before_raw,before_type,before_plural,stem,folder,index_refs,other_fields,today}; ops::IndexRefs{index_by,index_facets}; ops::OtherAlbumField{path,key,storage,list}.

[2026-11-12T14:09:30Z · bob-cli-kr.2.1.1] schema-ops verified: 17 update unit tests pass (all 9 ops, ordered batches, collisions, kind-specific defaults incl. today token, unset vs false/zero/empty, used/index/storage refusals with counts, list usage, incomplete-scan guard, missing targets, position edges, inverse round-trips); 197 albums+records lib tests pass; cargo fmt clean; workspace clippy gate 0 errors. Test-only update module under #[cfg(test)], no public command, no version/changelog edits.

## Dependencies

- **Blocks:** [bob-cli-kr.2.1.2](bob-cli-kr.2.1.2.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-kr.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.2.1.1/README.md) | [bob-cli-kr.2.1.1](bob-cli-kr.2.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kr.2.1.1][1] | Need full phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.2.1.1/README.md

<!-- sase:referenced-by:end -->
