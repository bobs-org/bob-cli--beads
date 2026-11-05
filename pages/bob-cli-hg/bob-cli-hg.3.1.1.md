# Bead: bob-cli-hg.3.1.1 — Model gog thread payloads and decode MIME body candidates

[Bead Pages](../README.md) / [bob-cli-hg.3.1](bob-cli-hg.3.1.md) / bob-cli-hg.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.1` · **Size:** medium
**Created:** 2026-11-05 13:16:21 EST · **Closed:** 2026-11-05 13:54:24 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

## Description

mime-model: add the verified gog thread envelope, typed messages and MIME parts, private body decoding, attachment discovery, and fetched-body inputs described in section 3. Include synthetic wire fixtures and decoding tests.

## Notes

[2026-11-05T18:54:13Z · bob-cli-hg.3.1.1] PROPOSED FOLLOW-UP: Make the cargo fmt check pass under the current rustfmt; just check fails on four unchanged base files (capture/plan.rs, config/mod.rs, plan_budget/mod.rs, task_status_hooks/sync.rs), the same repository-wide style drift tracked historically by bob-cli-24 and already noted on bob-cli-hg.2.

[2026-11-05T18:54:24Z · bob-cli-hg.3.1.1] Implemented the typed gog thread model, ordered headers, bounded MIME tree walking, private base64url and charset decoding, body candidate and attachment/CID discovery, and fetched-body hydration. Verified 15 focused Gmail tests pass, git diff --check passes, and just check reaches only the pre-existing rustfmt failure on four unchanged base files; recorded that failure as a proposed follow-up. No epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-hg.3.1.2](bob-cli-hg.3.1.2.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.1/README.md) | [bob-cli-hg.3.1.1](bob-cli-hg.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`df9178d`](https://github.com/bobs-org/bob-cli/commit/df9178df1b6e944c339073689af65ac022e80199) | feat(gmail): model gog threads and decode MIME bodies | [bob-cli-hg.3.1.1](bob-cli-hg.3.1.1.md) | 2026-11-05 14:18:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.3.1.1][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.1/README.md

<!-- sase:referenced-by:end -->
