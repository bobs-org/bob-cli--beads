# Bead: bob-cli-gh.5 — Agent reviews — bob periods brief, draft, and instruction refresh

[Bead Pages](../README.md) / [bob-cli-gh](README.md) / bob-cli-gh.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.5` · **Size:** medium
**Created:** 2026-11-03 10:55:43 EST · **Closed:** 2026-11-03 15:00:12 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

## Description

reviews: the deterministic, versioned `bob periods brief` bundle for weeks, quarters, and years; `bob periods draft` with Headline and word-cap validation and the empty/drafted/edited/reflected guard; and `bob periods ensure -R` to refresh agent callouts.

## Notes

[2026-11-03T20:00:12Z · bob-cli-gh.5] Implemented the reviews phase: bob periods brief (brief v1 bundle, md+json, token budgets 6k/10k/12k), bob periods draft (Headline+word-cap validation, refused_open/refused_state guards with -F, digest-stamped atomic writes, lock wait + stale check), and bob periods ensure -R (one offline vault_rewrite commit 'periods: refresh agent instructions to vN', reflected notes skipped). Fixed parse_instructions_version, which read the last v on the callout line and marked every note stale (also repairs list -p). Docs: periods.md brief/draft/-R/walkthrough sections plus regenerated CLI reference. Verified: just check green (fmt, full clippy deny gates, entire test suite incl. 24 periods CLI tests covering closed-week golden, quarter/year shapes, determinism, draft lifecycle/validation/lock/stale, and -R commit semantics); just docs-check green.

## Dependencies

- **Depends on:** [bob-cli-gh.3](bob-cli-gh.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gh.9](bob-cli-gh.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gh.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.5/README.md) | [bob-cli-gh.5](bob-cli-gh.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13fb39d`](https://github.com/bobs-org/bob-cli/commit/13fb39d0d40c35ee361400a552a29b08ce1bfcaf) | feat(periods): add agent reviews — brief, draft, and instruction refresh | [bob-cli-gh.5](bob-cli-gh.5.md) | 2026-11-03 15:01:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.5][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-gh.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.land/README.md

<!-- sase:referenced-by:end -->
