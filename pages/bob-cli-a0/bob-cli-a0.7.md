# Bead: bob-cli-a0.7 — Hand-written product reference

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.7` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT · **Closed:** 2026-10-20 00:29:30 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

reference-pages: write Capture syntax with a token index, Vault format, Configuration and environment, and JSON outputs, plus env-var drift and search smoke coverage.

## Notes

[2026-10-20T04:01:58Z · bob-cli-a0.7.1.land] Child-epic landing audit at f30389c7: all three product-reference phases are closed and their notes reviewed, with zero PROPOSED FOLLOW-UP entries. The four pages and nav exist, 65 focused environment/token/lint tests pass, and both child/parent epic-symbol scans are empty. Completion is blocked by epic-caused scanner delimiter bugs (string braces hide production names or leak test names), inaccurate/incomplete JSON command descriptions, missing per-operation capture examples/literal-query enforcement, and plugin checkout selection wording. A validated medium remaining-work tale is being proposed; it must repair these gaps, integrate the newer tutorial/demo/sandbox, run just check and docs gates, close bob-cli-a0.7.1, mark product_reference.md done, and then close only this phase normally. bob-cli-a0 remains for its waiting land agent. No unrelated follow-up task is needed.

[2026-10-20T04:30:22Z · bob-cli-a0.7.1.land] Child epic bob-cli-a0.7.1 closed after the remaining-work tale. Four reference pages are live (capture-syntax, vault-format, configuration, json-outputs) with named token anchors, Pending/Next, and task-line anatomy in the Material HTML. Literal token/lane/goal search coverage is enforced (71 smoke cases; token spellings must appear as queries at their headings). Environment guard regressions cover string/char delimiters. Plugin install documents --repo then BOB_PLUGINS_DIR then default, with foreign-checkout refusal. JSON catalog matches source for ref scan/today, capture writes, vault-sync StatusRecord, and other formats. Tutorial related/next links added; mounts.yml empty so Mac hotkey README links stay. Gates: just check passed; just docs-check passed (268 pytest, tutorial, lychee, search smoke); just docs-build-material passed. epic-symbols for bob-cli-a0.7: none. justfile still has no symvision recipe. Child phases offered zero PROPOSED FOLLOW-UPs; no new triage. bob-cli-a0 left open. plan:202610/product_reference.md status done; parent docs-site plan untouched.

## Dependencies

- **Blocks:** [bob-cli-a0.12](bob-cli-a0.12.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.3](bob-cli-a0.3.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.4](bob-cli-a0.4.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.8](bob-cli-a0.8.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.md) | [bob-cli-a0.7](bob-cli-a0.7.md) | 0 |
