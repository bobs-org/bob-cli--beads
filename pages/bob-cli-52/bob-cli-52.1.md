# Bead: bob-cli-52.1 — Typed, non-printing URL ingest extracted from bob ref create

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.1` · **Size:** medium
**Created:** 2026-10-07 08:11:16 EDT · **Closed:** 2026-10-07 08:39:57 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

ingest: extract a typed URL ingest API from `ref create`. It returns created, already-in-library, and already-queued outcomes, or a typed error kind with a retryable flag. It uses fixed reading-queue defaults, a machine-wide ingest lock, and fsync on install. `ref create` output and exit codes stay byte-identical. Also add the shared ⚠️ fallback-note helper.

## Notes

[2026-10-07T12:39:41Z · bob-cli-52.1] PROPOSED FOLLOW-UP: lib tests every_value_arg_has_a_decision and listen_filter_renders_card_and_encoded_play_link fail identically on the clean base tree (verified via stash); the listen one is already recorded in docs/highlights-create.md as a bob-cli-4s.6 follow-up

[2026-10-07T12:39:57Z · bob-cli-52.1] ingest.rs typed URL ingest (Created/AlreadyInLibrary/AlreadyQueued, kinds+retryable, fallback_note, ingest.lock, fsync, Config::for_vault) with 6 unit tests; characterization CLI test for timeout/blocked/crash/missing-uv; docs Ingest boundary. Verified: cargo fmt clean, clippy exit 0, 6/6 ingest unit tests, 38/38 create CLI tests, 172/172 highlights CLI tests, full cli suite 1112/1112 on rerun (first run hit 3 flaky completion tests that passed on rerun). 2 lib failures (every_value_arg_has_a_decision, listen_filter) reproduce identically on clean base; recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-52.5](bob-cli-52.5.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.6](bob-cli-52.6.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.1/README.md) | [bob-cli-52.1](bob-cli-52.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2eafe60`](https://github.com/bobs-org/bob-cli/commit/2eafe60c505be3852633cb61e1f2cc29db409b17) | feat(ref): add typed non-printing URL ingest for reading queue | [bob-cli-52.1](bob-cli-52.1.md) | 2026-10-07 08:41:05 EDT |
