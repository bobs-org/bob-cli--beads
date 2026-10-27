# Bead: bob-cli-an.6.6.6.5.6.5.5.1 — Mark the source manifest published when a pending feed retry succeeds

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.1` · **Size:** small
**Created:** 2026-10-25 07:49:26 EDT · **Closed:** 2026-10-25 07:57:39 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

## Description

listen-manifest: resolve bob-cli-bq in sase-listen flush_pending so a successful retry marks the originating library manifest published, with success and failure tests.

## Notes

[2026-10-25T11:57:30Z · bob-cli-an.6.6.6.5.6.5.5.1] listen-manifest done in sase-listen checkout. Baseline: reproduced bob-cli-bq — flush_pending dropped the outbox entry after _push_episode succeeded without calling mark_manifest_published, so the source library manifest kept published:false. Fix (src/sase_listen/feedhost.py): flush_pending takes library and passes it to _push_episode; on success it calls mark_manifest_published(episode_id, library) before dropping the outbox. A mark failure (OSError/ValueError) keeps the outbox entry via queue_publish and lands in failed with a 'delivered but the source manifest could not be marked published' error, so nothing is lost silently — surfaced by publish --pending's existing failure output. publish_any now threads its library into its best-effort flush_pending call. Tests (tests/test_feedhost.py, 4 new): success marks both manifests + empties outbox + second flush is a no-op; failure (missing MP3) keeps outbox and published:false; mixed batch splits correctly; monkeypatched mark failure stays queued. Docs: docs/multi-machine.md Outbox paragraph notes the new mark-on-retry behavior. Gate: sase tool run check (ruff + format + mypy --strict + codespell + full pytest) succeeded. Limitation: repo has no reconcile command, so the three stale Athena manifests (outbox already empty, feed already has the episodes) need a manual one-time repair per episode id with the repo venv: python -c "from sase_listen.feed import mark_manifest_published; mark_manifest_published('<episode-id>')". Leaving bob-cli-bq open for the lander to verify/close.

[2026-10-25T11:57:39Z · bob-cli-an.6.6.6.5.6.5.5.1] flush_pending now marks the source manifest published on successful retry (library threaded through push+mark; mark failures stay queued and reported). 4 new tests in tests/test_feedhost.py; sase tool run check green. bq left open for lander verification; no reconcile command exists so the three stale Athena manifests need the manual one-shot repair recorded in the phase note.

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.1][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md

<!-- sase:referenced-by:end -->
