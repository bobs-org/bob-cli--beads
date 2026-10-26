# Bead: bob-cli-c9.3.1 — Complete ref create force-mode parsing and rereads

[Bead Pages](../README.md) / [bob-cli-c9.3](bob-cli-c9.3.md) / bob-cli-c9.3.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.land`
**Created:** 2026-10-25 15:22:58 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_create_reread.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md

<!-- sase:links:end -->

## Description

Complete bob-cli-c9.3 so an explicit reread creates a separate reading with durable lineage, a new reading task, and no changes to earlier readings, across every supported create route and queued intake.

## Notes

[2026-10-25T23:45:17Z · bob-cli-c9.3.1.land] Land verification (bob-cli-c9.3.1.land): just check green at 9923063e (fmt, clippy gate, cargo test --no-fail-fast, exit 0); no upstream drift (origin/master == HEAD); the only non-epic commit during the epic, 55334b09 (Markdown section numbering Lua filter), sits on the shared render path and needs no integration. Epic symbols: none for bob-cli-c9.3.1 or bob-cli-c9.3. Code review found remaining epic work (regressions and unmet plan items), planned as a child epic: title-route stem probe ignores title identity (different-title stems refuse/reread instead of _2; -N remedy lost); locked intake recheck refuses every audio attach onto a __vN or natural protocol__v2 reference; multi-family URL overlap returns Ambiguous so -N can reread a partially overlapping family; collection -L attach treats readings as separate groups and single-source -L attaches to the oldest reading; deleted-root families mint <root>__v2__vN; filed refusal drops reading numbers; exact-output replacement lost under -f overwrite on URL/collection routes; plain reread prints no narrated-reading hint; -f -L -P on a library PDF attaches; vault-note preflight runs after parent resolution; post-fetch guard ignores redirect final_url; parser raw-argv misses bob ref -n create and -df=MODE; rereads still auto-discover Markdown audio; docs/help gaps; stale dead_code allows. FOLLOW-UP TRIAGE: (1) bob-cli-c9.3.1.3 PROPOSED FOLLOW-UP (full-scan raw intake moves lack the locked reread recheck) - ABSORBED into the remaining epic work, not filed as a task: the epic's acceptance requires queued reread + scan to file nothing over an occupant, and create -f queues __vN PDFs that a full bob ref scan moves through doctor.rs plan_xlib_intake without the whole-bundle recheck. No other PROPOSED FOLLOW-UP entries exist on any child. Reviewer-noted items deliberately NOT filed: per-create library+task index build (by design: the plan requires resolving hits through the library index); whole-bundle checks for ordinary (non-__vN) full-scan moves and redirect-aware dedupe for ordinary captures (pre-existing, race-only/no reported harm, outside this epic's contract); URL reread dry runs still fetch (matches the documented URL dry-run contract in docs/highlights-create.md; the reread decision and line are computed before fetch); -f overwrite -L on a filed reference keeps the old companion-audio attach permission (plan keeps audio replacement permissions under either mode).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) | [bob-cli-c9.3.1](bob-cli-c9.3.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.1][1] | parent epic scope | 1 |
| read-by | [agent:bob-cli-c9.3.1.4][2] | Need parent epic status | 1 |
| read-by | [agent:bob-cli-c9.3.1.5][3] | Need epic DECISIONS | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.5/README.md

<!-- sase:referenced-by:end -->
