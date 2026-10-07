# Bead: bob-cli-52.6 — bob gkeep pull clips URL-only Keep notes

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.6` · **Size:** medium
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 09:40:50 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

gkeep: the adapter emits shared-link annotations; the R5 URL-only rule becomes a `create_ref` plan action; a clip pre-pass runs before the vault lock; a `ref_created` journal event; retryable failures stay in Keep and permanent ones are written as tasks with a ⚠️ note; the archive guard checks attachment counts. Also covers dry-run, list, JSON, `-R`, and docs.

## Notes

[2026-10-07T13:40:32Z · bob-cli-52.6] PROPOSED FOLLOW-UP: lib completion kinds test fails on clean base too (tracked by bob-cli-4j) and listen-card test fails on clean base too (see bob-cli-4u); capture_pomodoros warning test flakes under parallel cargo test (tracked by bob-cli-40) — all unrelated to gkeep phase

[2026-10-07T13:40:36Z · bob-cli-52.6] PROPOSED FOLLOW-UP: cli highlights::create::ingest_characterizes_url_failure_modes fails identically on the clean base tree (expects uv-missing error, gets private-address resolve refusal) — needs triage, no tracking bead found

[2026-10-07T13:40:50Z · bob-cli-52.6] gkeep phase done: R5 create_ref planner + ingest clip pre-pass before vault lock with per-clip ref_created journal; retryable stays in Keep (exit 1), permanent falls back to task with fallback_note child; archive guard sends expect_attachments; -R flag; dry-run/list/human/JSON surfaces; docs/gkeep.md. Verified: 77 gkeep integration + 110 lib gkeep tests pass, fmt clean, clippy clean for touched files, adapter self-test ok. Full lib has only base-identical failures (4j/4u) plus the bob-cli-40 parallel flake; one cli failure reproduces on base (recorded as follow-ups). Deliberate deviation: per-note JSON uses 'clip' object since 'ref' already holds the REF id.

## Dependencies

- **Depends on:** [bob-cli-52.1](bob-cli-52.1.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.2](bob-cli-52.2.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.3](bob-cli-52.3.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.9](bob-cli-52.9.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.6/README.md) | [bob-cli-52.6](bob-cli-52.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0a8c879`](https://github.com/bobs-org/bob-cli/commit/0a8c87907f55af9dcfce121a059615f848ef6ab9) | feat(gkeep): clip URL-only Keep notes into reading queue on pull | [bob-cli-52.6](bob-cli-52.6.md) | 2026-10-07 09:42:32 EDT |
