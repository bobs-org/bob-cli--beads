# Bead: bob-cli-hg.3.1.2 — Make sender text inert in every Markdown and YAML context

[Bead Pages](../README.md) / [bob-cli-hg.3.1](bob-cli-hg.3.1.md) / bob-cli-hg.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.2` · **Size:** medium
**Created:** 2026-11-05 13:16:21 EST · **Closed:** 2026-11-05 18:51:28 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

## Description

inert-output: implement the shared final serialization boundary, safe text helpers, strict link policy, and adversarial property tests in section 4. Preserve only renderer-owned Markdown structure and keep operational identifiers opaque.

## Notes

[2026-11-05T23:51:18Z · bob-cli-hg.3.1.2] PROPOSED FOLLOW-UP: tests/cli docs_reference::cli_reference_is_current fails identically on the clean base tree (capture-parse.md drifted; run just docs-gen). Reproduced via git stash -u + single-test rerun. Unrelated to inert-output.

[2026-11-05T23:51:28Z · bob-cli-hg.3.1.2] inert-output done: new src/native/gmail/body/inert.rs (Block/Inline/SafeUrl, render_blocks final serializer, single-line/multiline/label/YAML helpers, strict http/https/mailto link policy, writer-only local embed, 10 tests incl. 2000-case adversarial corpus asserting parse_tasks/all_inline_fields/raw_wikilink_spans/block_ids clean plus no <%,<!--,![,[[ and YAML round-trips); wired via body/mod.rs; also derived Default for MimeInventory (pre-existing clippy::derivable_impls denial). Verified: cargo fmt clean, repo clippy gate clean, lib 5175 pass, all 18 integration targets pass, gmail 32 pass, doctests clean. Pre-existing cli_reference_is_current docs failure reproduces on clean base, recorded as PROPOSED FOLLOW-UP. No epic-symbols left.

## Dependencies

- **Depends on:** [bob-cli-hg.3.1.1](bob-cli-hg.3.1.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.3.1.3](bob-cli-hg.3.1.3.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.2/README.md) | [bob-cli-hg.3.1.2](bob-cli-hg.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1cbe970`](https://github.com/bobs-org/bob-cli/commit/1cbe9703e6989482906e7d6b8efed1238d69777a) | feat(gmail): add inert output serialization boundary for gmail body | [bob-cli-hg.3.1.2](bob-cli-hg.3.1.2.md) | 2026-11-05 18:53:03 EST |
