# Bead: bob-cli-mf.10 — End-to-end acceptance, measurements, and decision record

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.10

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.10` · **Size:** medium
**Created:** 2026-11-16 15:38:39 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

acceptance: run real-Obsidian walkthroughs that count commits for both cards, plus timing budgets and light/dark/reduced-motion screenshots. Do a final consistency pass, write the decision record, and propose follow-ups for CLI save-latency trims.

## Notes

[2026-11-17T06:38:56Z · bob-cli-mf.10--5] Latency review: album applyMs was 513.9 ms and its six dry runs were 524–529 ms; the album report records one post-apply albums list but no per-command duration. The failed bank arrangement produced no Bob arrangement calls. The approximately 650 ms list estimate therefore cannot be validated against measured command latency, and no report-in-JSON, scoped verify_installed, or index_changed trim is supported by this run. No PROPOSED FOLLOW-UP added.

[2026-11-17T07:38:26Z · bob-cli-mf.10--8] Latency review of the latest album and bank reruns: Album Schema applyMs=513.9 ms; six settled dry-run samples were 524–529 ms (p50 525.5, p95 529). The report does not isolate the blocking bob albums list call, so these end-to-end values do not establish that embedding its result or another CLI trim would help against the plan's ~650 ms estimate. Bank config apply samples were 172 and 134 ms; revalidations were 19–21 ms. No specific CLI latency trim is supported; no PROPOSED FOLLOW-UP added. The current-source bank rerun still reports one arrangement apply, one revalidation, but two Git commits; successful-path diagnostics are being added to identify their subjects. Real-Obsidian rule-move save coverage is still absent (fixture starts with no rules), so acceptance remains open.

[2026-11-17T08:15:39Z · bob-cli-mf.10--b] Current-source bank rerun bdfqdvp8q9d4 passed (exit 0). Prior run hc4pjvvx7fjj failed in the harness post-save probe because bankArrangeSelectedScope() returned {scope,id} but the probe called startsWith on it; normalizing the probe fixed this without product changes. pluginSources points to /tmp/bob-cli-mf-acceptance/plugin-overlay; overlay and linked bob-ledger-tools main.js both have SHA-256 8244146d1f3ecd1dd82cc323ae19e1c6e0c8e6c04feff6c0dc5bcf43cc4f36b6. The compiled op and lastSetDraft.ops are category.move coffee after convenience; after Enter, saved/projected/category/model order is convenience, coffee. One Enter made Bob apply=1, revalidation=1, config commit=1; total Git commits=2, with the other subject vault(athena): 2 files - bank.md, bank/2026-11.md. Arrangement Undo added one Bob config commit; hide and hide Undo passed. Bank harness totals: Bob dryRuns=15, applies=7, revalidations=35. Album rerun passed; its album update invocations total 12 dry-runs and 4 applies, with one isolated arrangement revalidation and one commit each for arrangement save and Undo; 37 albums list calls are not individually classified as revalidations. Fresh contact sheets reviewed all 18 bank and 29 album screenshots; full-size bank arrangement light, dark, and reduced-motion images reviewed. Album applyMs=513.9 ms versus the accepted approximately 650 ms blocking albums-list estimate, but the report does not isolate that command duration, so no specific trim is supported and no PROPOSED FOLLOW-UP was added. sase bead epic-symbols returned no entries. The real-Obsidian script has no rule.move walkthrough and the fixture starts with no rules; keep this phase open/in progress pending that coverage.

## Dependencies

- **Depends on:** [bob-cli-mf.9](bob-cli-mf.9.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mf.10.md) | [bob-cli-mf.10](bob-cli-mf.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9babe42`](https://github.com/bobs-org/bob-plugins/commit/9babe42d50746942ffa09ea0c94b69e136a81aec) | feat(ledger-tools): add schema arrangement cards | [bob-cli-mf.10](bob-cli-mf.10.md) | 2026-11-17 03:18:58 EST |
