# Bead: bob-cli-kf.4 — Bank month-note parser fixes

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.4` · **Size:** small
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 14:10:35 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

bank-parser-fixes: validate trailing tokens before the out-of-month early return in day-heading parsing, parse frontmatter from BOM-stripped text, and correct the latent write-planner anchors to match the documented contract.

## Notes

[2026-11-11T19:10:35Z · bob-cli-kf.4] Fixed all three bank-parser items: ISO day headings now validate trailing tokens before the out-of-month early return (multi-token junk like '2025-12-31 year-end review' is prose again); month-note frontmatter parses from BOM-stripped text; write planners anchor appends after indented free-note children, keep one blank line after empty-day headings, and insert earliest days after the first fence block. Added 4 regression tests (grammar trailing-junk/out-of-month, BOM frontmatter, append-after-children, empty-day blank, day-notes-fence insert). Verified: cargo test --lib bank 26/26 pass, cargo fmt clean, just lint exit 0, no clippy hits in bank files.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.4/README.md) | [bob-cli-kf.4](bob-cli-kf.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`757e36b`](https://github.com/bobs-org/bob-cli/commit/757e36bb0d758031e2eaf2c065d1662577034583) | fix(bank): validate out-of-month headings, BOM frontmatter, planner anchors | [bob-cli-kf.4](bob-cli-kf.4.md) | 2026-11-11 14:11:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kf.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.4/README.md

<!-- sase:referenced-by:end -->
