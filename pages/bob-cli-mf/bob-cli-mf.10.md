# Bead: bob-cli-mf.10 — End-to-end acceptance, measurements, and decision record

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.10` · **Size:** medium
**Created:** 2026-11-16 15:38:39 EST · **Closed:** 2026-11-17 04:25:33 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:320a6276021490979e5d934b | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: run real-Obsidian walkthroughs that count commits for both cards, plus timing budgets and light/dark/reduced-motion screenshots. Do a final consistency pass, write the decision record, and propose follow-ups for CLI save-latency trims.

## Notes

[2026-11-17T06:38:56Z · bob-cli-mf.10--5] Latency review: album applyMs was 513.9 ms and its six dry runs were 524–529 ms; the album report records one post-apply albums list but no per-command duration. The failed bank arrangement produced no Bob arrangement calls. The approximately 650 ms list estimate therefore cannot be validated against measured command latency, and no report-in-JSON, scoped verify_installed, or index_changed trim is supported by this run. No PROPOSED FOLLOW-UP added.

[2026-11-17T07:38:26Z · bob-cli-mf.10--8] Latency review of the latest album and bank reruns: Album Schema applyMs=513.9 ms; six settled dry-run samples were 524–529 ms (p50 525.5, p95 529). The report does not isolate the blocking bob albums list call, so these end-to-end values do not establish that embedding its result or another CLI trim would help against the plan's ~650 ms estimate. Bank config apply samples were 172 and 134 ms; revalidations were 19–21 ms. No specific CLI latency trim is supported; no PROPOSED FOLLOW-UP added. The current-source bank rerun still reports one arrangement apply, one revalidation, but two Git commits; successful-path diagnostics are being added to identify their subjects. Real-Obsidian rule-move save coverage is still absent (fixture starts with no rules), so acceptance remains open.

[2026-11-17T08:15:39Z · bob-cli-mf.10--b] Current-source bank rerun bdfqdvp8q9d4 passed (exit 0). Prior run hc4pjvvx7fjj failed in the harness post-save probe because bankArrangeSelectedScope() returned {scope,id} but the probe called startsWith on it; normalizing the probe fixed this without product changes. pluginSources points to /tmp/bob-cli-mf-acceptance/plugin-overlay; overlay and linked bob-ledger-tools main.js both have SHA-256 8244146d1f3ecd1dd82cc323ae19e1c6e0c8e6c04feff6c0dc5bcf43cc4f36b6. The compiled op and lastSetDraft.ops are category.move coffee after convenience; after Enter, saved/projected/category/model order is convenience, coffee. One Enter made Bob apply=1, revalidation=1, config commit=1; total Git commits=2, with the other subject vault(athena): 2 files - bank.md, bank/2026-11.md. Arrangement Undo added one Bob config commit; hide and hide Undo passed. Bank harness totals: Bob dryRuns=15, applies=7, revalidations=35. Album rerun passed; its album update invocations total 12 dry-runs and 4 applies, with one isolated arrangement revalidation and one commit each for arrangement save and Undo; 37 albums list calls are not individually classified as revalidations. Fresh contact sheets reviewed all 18 bank and 29 album screenshots; full-size bank arrangement light, dark, and reduced-motion images reviewed. Album applyMs=513.9 ms versus the accepted approximately 650 ms blocking albums-list estimate, but the report does not isolate that command duration, so no specific trim is supported and no PROPOSED FOLLOW-UP was added. sase bead epic-symbols returned no entries. The real-Obsidian script has no rule.move walkthrough and the fixture starts with no rules; keep this phase open/in progress pending that coverage.

[2026-11-17T09:06:36Z · bob-cli-mf.10] PROPOSED FOLLOW-UP: Decision record schema-arrangement-is-one-commit — The accepted decision_record=no branch forbids memory edits in this epic. The land agent may separately propose the durable record that reorder gestures form one guarded envelope, one commit, and one Undo; no memory was edited.

[2026-11-17T09:06:51Z · bob-cli-mf.10] PROPOSED FOLLOW-UP: Album-level emoji — The acceptance plan defers album-level emoji because album.set has no emoji field. Triage separately from the delivered choice/category Emoji Slot.

[2026-11-17T09:15:05Z · bob-cli-mf.10] PROPOSED FOLLOW-UP: Repair existing plugin suite failures — npm test on bob-plugins 9babe42 plus this harness reported 15 failures (7125/7143 passed; 3 skipped); a clean git-archive export of 9babe42 reproduced the same assertions for 14 in the 12 affected files. They cover event-link/keep-moving/off-clock timing, reading-board/stats/priority CSS contracts, bracket/walkMode (bob-cli-md), highlights-hints, period-links daily aliases, and block-marks hardcoded dates (bob-cli-m8; also mf.9 notes). The remaining frees-marks timing failure passed on clean base and on an isolated changed-tree rerun (17/17), indicating load sensitivity. No acceptance-related test failed. Logs retained for final evidence.

[2026-11-17T09:24:49Z · bob-cli-mf.10] PROPOSED FOLLOW-UP: Measure schema save stages before choosing CLI latency trims — Final Obsidian end-to-end save observations were album 458.1 ms and bank 523.6 ms (one sample each). Bank config apply p50/p95 was 157.5/178 ms and config revalidation 17.5/18 ms (n=2 each); album does not isolate albums-list duration, so the plan's approximately 650 ms list estimate remains unverified. Add per-stage timings and repeatable save samples; evaluate embedding the refreshed report in update JSON, scoped verify_installed, and index_changed only if attribution supports them. Treat offline interactive save as a separate product decision. Evidence: file:explicit:320a6276021490979e5d934b.

[2026-11-17T09:25:10Z · bob-cli-mf.10] Final acceptance complete on bob-ledger-tools 1.127.1. Added the missing real-Obsidian three-rule move/save/Undo walkthrough; it exposed and fixed discarded post-write reports, stale positional rule identities after save, and duplicate config revalidation. Bank now passes 72/72 checks (tool b635e385eed15d5befbc58dc72e32621); album passes 101/101 (34fa625c96d9ddf4639b2ef740b3a95c). Rule move and Undo each make exactly one config apply, one config revalidation, and one Git commit; loud first Enter only confirms. Quiet category save makes one config commit plus the separately identified prior fixture vault-sync commit; category Undo and album save/Undo each make one config commit. Nudge p95: bank 3.8 ms, album 3.5 ms (n=60 each); bank emoji-filter p95 20.6 ms (n=20); settled dry-run p95 bank 468 ms, album 527 ms (n=6 each). Reviewed all 21 bank and 29 album screenshots, including light/dark/reduced-motion compact cards. Focused tests 56/56; build, manifests, docs generation, diff check and full docs:check pass (447 docs tests, 1 skip). Final npm test has 7127 pass, 15 fail, 3 skip, exactly the same 15 failure locations as before these fixes: 14 reproduced on clean base, frees-marks passes on both isolated trees; no new failures. Existing failure and deferred latency/emoji/decision-record follow-ups are noted for land-agent triage. Synced plugin 1.127.1 via bob plugins sync. No memory changed under decision_record=no. No epic-symbol entries remain. Reports, 50 screenshots, logs, base comparison, timings, source hashes and patch are preserved in attached artifact file:explicit:320a6276021490979e5d934b (bob-cli-mf.10-acceptance.tar.gz).

[2026-11-17T09:25:33Z · bob-cli-mf.10] Verified real-Obsidian bank 72/72 and album 101/101, including rule move/save/Undo and one write commit per gesture; album commits are album-update commits. Fixed refreshed-report propagation, rule identity reseeding, and duplicate config reads; 56 focused tests and full docs gate pass. Recorded unchanged base-suite failures and latency follow-ups. Reviewed 50 screenshots, synced 1.127.1, preserved artifact file:explicit:320a6276021490979e5d934b, and confirmed no epic-symbol entries. No decision memory edited; close this phase only.

## Dependencies

- **Depends on:** [bob-cli-mf.9](bob-cli-mf.9.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.10/README.md) | [bob-cli-mf.10](bob-cli-mf.10.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9babe42`](https://github.com/bobs-org/bob-plugins/commit/9babe42d50746942ffa09ea0c94b69e136a81aec) | feat(ledger-tools): add schema arrangement cards | [bob-cli-mf.10](bob-cli-mf.10.md) | 2026-11-17 03:18:58 EST |
| bob-plugins | [`bob-plugins@9ae8142`](https://github.com/bobs-org/bob-plugins/commit/9ae8142d2950d24d5ea09dd555a10969dfdab822) | fix(ledger-tools): refresh saved arrangements and complete acceptance | [bob-cli-mf.10](bob-cli-mf.10.md) | 2026-11-17 04:26:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.10--b][1] | Verify the appended acceptance rerun note and leave the phase open | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mf.10.md

<!-- sase:referenced-by:end -->
