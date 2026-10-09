# Bead: bob-cli-5y.9 — bob ref create requires -P; ingest, jobs, and fallbacks carry the parent

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.9` · **Size:** medium
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 19:38:31 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

ref-create-parent: make -P required with no default, thread the resolved parent through typed ingest, ref jobs, and clip-failure fallbacks, and delete the obsidian_ref defaults.

## Notes

[2026-10-09T23:38:13Z · bob-cli-5y.9] PROPOSED FOLLOW-UP: skipped memory decision memory_ref_parent_decision — add decisions strand ref-tasks-live-with-their-parent (residence is the parent, #ref plus path-qualified link is identity, ^ref-<slug> is only an address, only Ready refs keep REFERENCES)

[2026-10-09T23:38:19Z · bob-cli-5y.9] PROPOSED FOLLOW-UP: skipped memory decision memory_glossary_ref_terms — update glossary reference-task (single #task #ref reading task in parent note), reference-note (holds no open tasks, embeds its reading task), and area-note (drop the reference-task residence exception) strands

[2026-10-09T23:38:31Z · bob-cli-5y.9] ref-create-parent done: -P required with custom missing-parent error plus capture-targets hint (exit 2), always resolved before any work, DEFAULT_PARENT/INGEST_PARENT deleted; IngestRequest.parent threads through all three clip routes; JobFile/NewJob carry optional parent (schema 1, old jobs fall back to source inbox), worker clips under effective parent, fallbacks land in the parent note with retry naming -P, jobs list shows parent in human and JSON; capture stages mac_inbox, gkeep passes gkeep_inbox; docs updated; verified: cargo fmt --check, cargo clippy, cargo test --no-fail-fast all exit 0 (lib 2151, cli 1323 incl. 3 new tests); 2 PROPOSED FOLLOW-UPs recorded for the skipped memory decisions

## Dependencies

- **Blocks:** [bob-cli-5y.10](bob-cli-5y.10.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.4](bob-cli-5y.4.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.7](bob-cli-5y.7.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.9/README.md) | [bob-cli-5y.9](bob-cli-5y.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e6aa7a4`](https://github.com/bobs-org/bob-cli/commit/e6aa7a491c4fcf504e02edf774442d934a7f5494) | feat(ref): require -P parent for bob ref create end to end | [bob-cli-5y.9](bob-cli-5y.9.md) | 2026-10-09 19:40:19 EDT |
