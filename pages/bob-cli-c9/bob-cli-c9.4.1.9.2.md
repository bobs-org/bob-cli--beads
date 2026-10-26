# Bead: bob-cli-c9.4.1.9.2 — Preserve task alias, user fields, and audio; align output and docs

[Bead Pages](../README.md) / [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) / bob-cli-c9.4.1.9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) · **Assignee:** `bob-cli-c9.4.1.9.2` · **Size:** medium
**Created:** 2026-10-26 03:39:12 EDT · **Closed:** 2026-10-26 05:25:19 EDT
**Plan:** [202610/overwrite\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/overwrite_landing_fixes.md)

## Description

output: rewrite the task alias only on a real title change, report the final task state, align success output with the contract, keep the Play link, narration diagnostics, and audio extension correct, apply keep_user_fields, and correct the create and clip docs.

## Notes

[2026-10-26T09:24:56Z · bob-cli-c9.4.1.9.2] PROPOSED FOLLOW-UP: title-route -N <v2-stem> overwrite misses the family when the source file stem collides with the rejected Info title (same-stem source + stem-equal Info title falls back to humanize(-N stem) = "report v2" for identity, matching nothing). Worked around in tests with distinctly named sources; fix belongs in recapture identity derivation (plan_local_pdf fallback should use the file stem, not the -N stem).

[2026-10-26T09:25:02Z · bob-cli-c9.4.1.9.2] PROPOSED FOLLOW-UP: capture_related synthetic timing tests (synthetic_vault_query_is_under_250ms, synthetic_vault_draft_contract_is_under_250ms) fail under parallel full-suite load but pass in isolation on this tree; untouched by this phase, tracked by bob-cli-ca per the epic plan.

[2026-10-26T09:25:19Z · bob-cli-c9.4.1.9.2] Output phase done: alias rewrite gated on real title change with old (vN) suffix preserved; success/dry-run lines report final status/highlights/task state with inline reopen hint, kept-audio parenthetical, and sync: committed short-sha (push-pending text kept); Play link bound on markdown/vault-note renders; finished narration kept via post_listen_error on all routes; -a with new extension publishes at library stem and removes old companion in-transaction; aliases/topics/research carried into marker and live note; clip/create docs corrected. Verified: cargo fmt, clippy gate (-D unused, -D private_interfaces) exit 0, just docs-gen + docs-check pass, cargo test lib 3534 ok, cli 2188 ok (incl. 8 new overwrite tests); 2 capture_related timing flakes fail only under parallel load and pass in isolation (PROPOSED FOLLOW-UP noted, tracked by bob-cli-ca).

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.9.1](bob-cli-c9.4.1.9.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-c9.4.1.9.3](bob-cli-c9.4.1.9.3.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.2/README.md) | [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`43f8aff`](https://github.com/bobs-org/bob-cli/commit/43f8aff5d0a39b8c982fe7048e6839d86406c0fe) | feat(highlights): overwrite local and web routes with alias preservation | [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) | 2026-10-26 05:26:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.9.2][1] | check full detail with notes | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.2/README.md

<!-- sase:referenced-by:end -->
