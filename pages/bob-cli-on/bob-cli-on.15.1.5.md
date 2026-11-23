# Bead: bob-cli-on.15.1.5 — Verify complete Mac requirement flows and publish their documentation

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.5` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 21:10:14 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

integration: exercise the full fake-bob and current-bob synthetic-vault acceptance matrix, finish cross-surface regression coverage and requirement receipts, update Mac keyboard/preview/protocol docs and the bob-cli requirement contract, and run portable, documentation, scratch-Mac and exact-SHA macOS gates. Record completion evidence for the child epic land agent; do not close ancestors.

## Notes

[2026-11-23T02:10:04Z · bob-cli-on.15.1.5--3] Integration evidence: cargo build --locked --bin bob and cargo test --locked --test cli req_close passed (25 tests). The Mac fixture generator used CLI source 9d0cbfbe165d; the copied RV vectors matched byte-for-byte. Mac portable-check passed (2,699 tests, one skipped). Mac just docs-check passed with capture-previews at 5,976 words, keyboard at 5,995, and protocol at 6,000. CLI just docs-gen and just docs-check passed (447 docs tests, one dependency-related skip; one developer-tier budget warning only). Scratch Scripts/bundle.sh and just typecheck-tests passed for BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, and RefsCoreTests. Exact snapshot SHA d5a72864e411e7a67541417ab4253cf9e2fa87e1 passed GitHub macOS run 45096397284, including lint, build, tests, bundle, signature, launch smoke, and install/reinstall; the temporary CI branch was deleted. The phase epic-symbol query returned no entries. CI: https://github.com/bobs-org/bob-mac-capture/actions/runs/45096397284

[2026-11-23T02:10:14Z · bob-cli-on.15.1.5--3] Verified integration acceptance, fixture provenance, Mac portable/docs/scratch gates, CLI docs generation/check, exact-SHA macOS CI, and empty phase epic-symbols query. Full evidence is in the preceding phase note. Closing this phase only; the child epic and ancestors remain with their land agents.

## Dependencies

- **Depends on:** [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.5.md) | [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9d0cbfb`](https://github.com/bobs-org/bob-cli/commit/9d0cbfbe165d56ac6f24b34d01d861d60d93f1b4) | docs(requirements): describe the Mac requirement card | [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) | 2026-11-22 19:41:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.5--3][1] | Review assigned requirement-close epic scope, evidence, and remaining symbols | 1 |
| read-by | [agent:bob-cli-on.15.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md

<!-- sase:referenced-by:end -->
