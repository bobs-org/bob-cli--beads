# Bead: bob-cli-k3.2.1 — Album model — schema parsing, vault registry, and read-only reports

[Bead Pages](../README.md) / [bob-cli-k3.2](bob-cli-k3.2.md) / bob-cli-k3.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-k3.2` · **Assignee:** `bob-cli-k3.2.1.land`
**Created:** 2026-11-11 05:07:02 EST · **Closed:** 2026-11-11 09:09:55 EST
**Plan:** [202611/album\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_model.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/album_model.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_model.md

<!-- sase:links:end -->

## Description

Complete bob-cli-k3.2 with album and record recognition, album-local schema diagnostics, a vault-aware registry with album-wins transition semantics, and read-only bob albums list/check reports. Preserve current config-based records behavior until the parent epic's consumer migration and retirement.

## Notes

[2026-11-11T13:29:31Z · bob-cli-k3.2.1.land] FOLLOW-UP TRIAGE before repair tale: reviewed every child note; the only PROPOSED FOLLOW-UP is bob-cli-k3.2.1.3 note #1. Ran sase_new_task duplicate searches (ci then all types), last-week compact sweeps, and the active-epic scope sweep. Corroborated four mounted-page overages on bob-cli-jz and protocol.md on bob-cli-h9 using independent just docs-check at ba9867a5 / Mac ee26941 / plugins 66841b1 (6036/6177/6060/6186 and 6149 words). No new tasks or causal active-epic attachment needed for those inherited linked-source failures. DECLINED the proposal to defer json-outputs.md: bob_docs.markdown.count_words is 5983 at pre-epic 05ec8253 and ba9867a5 parent, 6109 at HEAD; ba9867a5 adds 126 counted words and crosses cap 6000. The phase note used an incompatible raw count. Keep this docs failure as remaining epic work, and preserve full album contract while tightening the page. All follow-up outcomes have been triaged before proposing.

[2026-11-11T13:32:13Z · bob-cli-k3.2.1.land] LAND AUDIT at ba9867a5 (origin/master fetched, no post-HEAD drift): read the epic, all children and every note, parent phase bob-cli-k3.2 including final DECISIONS, both audited plans and required research; reviewed source and commits f977009a/b6f3b92c/ba9867a5. Scope honors the decisions: this child edits no memory, no forbidden albums-own-record-schemas decision, no vault/config migration. Reviewed non-epic commits d0ada555 (shared host_catalog regions/transactions; notebook snapshot adapter remains compatible) and 01c8e822 (disjoint record spans; preserved, no album consumer migration in this child). Do not close yet. Remaining album work: resolve_route_head joins unchecked routes before I/O and can read ../outside.md or an absolute target; malformed schema noun recovery keeps comments, loses an intact noun in unclosed flow YAML, or takes a nested noun; reports discard finding paths and human key paths/suggestions, ignore folder NoteRead diagnostics, and emit ok:true for pure I/O failure; grouping accepts scalar storage for list fields; human list keeps invalid schemas in normal root groups; RecordDiagnostic Display lost existing non-config field context; album docs omit the ownership/transition details and cross the JSON reference word cap. Source-extracted rustc probe independently produced Some(restaurant # comment), None for an intact flow noun, Some(restaurant) for a nested-only noun, and record value: unknown choice without field status. No Rust repository gate claimed yet; just docs-check ran and failed at six budget findings, with triage recorded separately. Current epic-symbols is empty for both bob-cli-k3.2.1 and bob-cli-k3.2; justfile has no symvision recipe. A medium tale will repair and regression-test this bounded remaining work, run just check/docs-gen/docs-check, and perform this epic plus parent phase closeout in the coder turn without waiting for its commit.

[2026-11-11T13:36:31Z · bob-cli-k3.2.1.land] AUDIT REFINEMENT: inspected records/check.rs::field_state and validate_field_values after the first land note. The existing record checker also accepts scalar input for list fields, so scalar-to-list grouping is not established as a contract regression. Declined a behavior change for that concern; the repair tale preserves existing typed validation and tests missing/unknown/unsupported values instead. All other listed resolver, noun recovery, report diagnostics/I/O, invalid-album human placement, diagnostic Display, and docs defects remain required epic work.

[2026-11-11T14:09:55Z · bob-cli-k3.2.1.land] Landing repairs verified: resolve_route_head confines the route to a vault-root capture stem before I/O (traversal/absolute/reserved/dot, symlink escape, foreign known registry ignored); recover_noun_from_yaml keeps comments/quoted/unclosed flow and ignores nested-only nouns while folder claims still suppress matching config dirs; reports copy finding.path, render path:line key_path plus suggestions, preserve folder/member NoteRead I/O, and set ok false when io_errors are nonempty; human list groups error albums as invalid/unowned while JSON/root keep computed root; grouping covers missing/unknown/null/unsupported and list-on-scalar/empty-scalar as needs_status; RecordDiagnostic Display restores type/field except album file:line key_path; docs cover canonical [[record]], isolation, reserved stems/nouns, optional fields, empty missing folders, counted members, and ok on I/O. json-outputs count_words 5973/6000. Tests: native::albums 31, schema 12, album_and_record_predicates, cli albums 19. just check passed; just docs-gen passed. just docs-check still reports five inherited mounted-page overages (mac-capture capture-panel 6036, capture-previews 6177, keyboard 6060, protocol 6149; plugins bob-navigation-hotkeys 6186) already tracked on bob-cli-jz / bob-cli-h9. epic-symbols empty. justfile has no symvision recipe. Children .1/.2/.3 already closed. No memory edits.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.2.1.land.md) | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ba3f51b`](https://github.com/bobs-org/bob-cli/commit/ba3f51bad3bd491d66e739a895ce4de99149329f) | fix(albums): confine routes, recover nouns, and restore report diagnostics | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2026-11-11 09:11:57 EST |
| bob-cli--plans | [`bob-cli--plans@5335af5`](https://github.com/bobs-org/bob-cli--plans/commit/5335af5dd1df88005093f7e933575f39fdf026ae) | chore(plans): mark album\_model epic plan done | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2026-11-11 09:12:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.2.1.2][1] | Need the parent epic decisions governing this phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.2.1.2/README.md

<!-- sase:referenced-by:end -->
