# Bead: bob-cli-8f.1 — bob ref today

[Bead Pages](../README.md) / [bob-cli-8f](README.md) / bob-cli-8f.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7y.md) · **Assignee:** `bob-cli-8f.1` · **Size:** medium
**Created:** 2026-10-16 10:04:17 EDT · **Closed:** 2026-10-16 11:15:57 EDT
**Plan:** [202610/refs\_link\_to\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_link_to_today.md)

## Description

cli: add `bob ref today <REF>` to bob-cli. It resolves a reference and its v2 reading task, then reuses capture's existing-task Pomodoro link planner and atomic commit. Capture's ledger selection gains exact-name and stale-safe entry-ref targets. The command emits a schema-1 JSON envelope (open Pomodoros with running/default/linked flags plus capture's own pomodoro_link item object) with stable error codes. Ships docs, help text, and parity tests against `bob capture '^route:block-id[#name]'`.

## Notes

[2026-10-16T14:59:51Z · bob-cli-8f.1] mac_core JSON fixtures from `bob ref today -f json` on a scratch vault (BOB_NOW=2026-10-16 09:15:00). Compact schema-1 envelopes: listing (dry-run), linked, created (`-p focus`), moved (Q→FOCUS), already_current, link_guard, multiple_running.
🔒 README.md
🔒 listing.json
🔒 linked.json
🔒 created.json
🔒 moved.json
🔒 already\_current.json
🔒 link\_guard.json
🔒 multiple\_running.json

[2026-10-16T15:00:18Z · bob-cli-8f.1] mac_core JSON fixtures (`bob ref today -f json`, scratch vault, BOB_NOW=2026-10-16 09:15:00). Compact schema-1 envelopes; paste these as fake-bob fixtures.

\## listing
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"dry_run","changed":true,"ref":{"path":"ref/papers/attention.md","link":"[[ref/papers/attention]]","title":"Attention Is All You Need","marker_id":"attention"},"task":{"path":"sase.md","block_id":"ref-attention","link":"[[sase#^ref-attention]]","status_symbol":" ","status_name":"Ready"},"pomodoros":[{"ref":"2:4e8b857b","line":2,"name":"CURRENT","slug":"current","time_range":"0900-0930","placeholder":false,"starts_at":"2026-10-16T09:00","ends_at":"2026-10-16T09:30","running":true,"default":true,"linked":false,"task_link_count":0},{"ref":"4:ddf7159c","line":4,"name":"READING","slug":"reading","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":false,"linked":false,"task_link_count":0}],"capture":{"block_id":"ref-attention","block_link":"[[sase#^ref-attention]]","created":"2026-10-16","creates_pomodoro":false,"day_file":"/tmp/bob-cli-8f.1-json/vaults/listing/day.md","dry_run":true,"kind":"pomodoro_link","ok":true,"placement":"linked","pomodoro_link_action":"linked","pomodoro_link_destination":{"line":2,"name":"CURRENT","role":"current","time_range":"0900-0930"},"pomodoro_link_placement":"inserted","pomodoro_name":"CURRENT","previous_status_name":"Ready","previous_status_symbol":" ","previous_task_line":"- [ ] #task #ref [[ref/papers/attention]] ^ref-attention","relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"status_changed":true,"status_name":"Next","status_symbol":"*","target":"/tmp/bob-cli-8f.1-json/vaults/listing/sase.md","task_line":"- [*] #task #ref [[ref/papers/attention]] [fresh:: 2026-10-16] ^ref-attention","text":""}}
\```

\## linked
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"write","changed":true,"ref":{"path":"ref/papers/attention.md","link":"[[ref/papers/attention]]","title":"Attention Is All You Need","marker_id":"attention"},"task":{"path":"sase.md","block_id":"ref-attention","link":"[[sase#^ref-attention]]","status_symbol":" ","status_name":"Ready"},"pomodoros":[{"ref":"2:4e8b857b","line":2,"name":"CURRENT","slug":"current","time_range":"0900-0930","placeholder":false,"starts_at":"2026-10-16T09:00","ends_at":"2026-10-16T09:30","running":true,"default":true,"linked":true,"task_link_count":1},{"ref":"5:ddf7159c","line":5,"name":"READING","slug":"reading","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":false,"linked":false,"task_link_count":0}],"capture":{"block_id":"ref-attention","block_link":"[[sase#^ref-attention]]","created":"2026-10-16","creates_pomodoro":false,"day_file":"/tmp/bob-cli-8f.1-json/vaults/linked/day.md","dry_run":false,"kind":"pomodoro_link","ok":true,"placement":"linked","pomodoro_link_action":"linked","pomodoro_link_destination":{"line":2,"name":"CURRENT","role":"current","time_range":"0900-0930"},"pomodoro_link_placement":"inserted","pomodoro_name":"CURRENT","previous_status_name":"Ready","previous_status_symbol":" ","previous_task_line":"- [ ] #task #ref [[ref/papers/attention]] ^ref-attention","relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"status_changed":true,"status_name":"Next","status_symbol":"*","target":"/tmp/bob-cli-8f.1-json/vaults/linked/sase.md","task_line":"- [*] #task #ref [[ref/papers/attention]] [fresh:: 2026-10-16] ^ref-attention","text":""}}
\```

\## created
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"write","changed":true,"ref":{"path":"ref/papers/attention.md","link":"[[ref/papers/attention]]","title":"Attention Is All You Need","marker_id":"attention"},"task":{"path":"sase.md","block_id":"ref-attention","link":"[[sase#^ref-attention]]","status_symbol":" ","status_name":"Ready"},"pomodoros":[{"ref":"2:4e8b857b","line":2,"name":"CURRENT","slug":"current","time_range":"0900-0930","placeholder":false,"starts_at":"2026-10-16T09:00","ends_at":"2026-10-16T09:30","running":true,"default":false,"linked":false,"task_link_count":0},{"ref":"4:d8711593","line":4,"name":"FOCUS","slug":"focus","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":true,"linked":true,"task_link_count":1},{"ref":"6:ddf7159c","line":6,"name":"READING","slug":"reading","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":false,"linked":false,"task_link_count":0}],"capture":{"block_id":"ref-attention","block_link":"[[sase#^ref-attention]]","created":"2026-10-16","creates_pomodoro":true,"day_file":"/tmp/bob-cli-8f.1-json/vaults/created/day.md","dry_run":false,"kind":"pomodoro_link","ok":true,"placement":"linked","pomodoro_link_action":"linked","pomodoro_link_destination":{"line":4,"name":"FOCUS","role":"created"},"pomodoro_link_placement":"inserted","pomodoro_name":"FOCUS","previous_status_name":"Ready","previous_status_symbol":" ","previous_task_line":"- [ ] #task #ref [[ref/papers/attention]] ^ref-attention","relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"status_changed":true,"status_name":"Next","status_symbol":"*","target":"/tmp/bob-cli-8f.1-json/vaults/created/sase.md","task_line":"- [*] #task #ref [[ref/papers/attention]] [fresh:: 2026-10-16] ^ref-attention","text":""}}
\```

\## moved
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"write","changed":true,"ref":{"path":"ref/papers/attention.md","link":"[[ref/papers/attention]]","title":"Attention Is All You Need","marker_id":"attention"},"task":{"path":"sase.md","block_id":"ref-attention","link":"[[sase#^ref-attention]]","status_symbol":" ","status_name":"Ready"},"pomodoros":[{"ref":"2:4e8b857b","line":2,"name":"CURRENT","slug":"current","time_range":"0900-0930","placeholder":false,"starts_at":"2026-10-16T09:00","ends_at":"2026-10-16T09:30","running":true,"default":false,"linked":false,"task_link_count":0},{"ref":"3:d8711593","line":3,"name":"FOCUS","slug":"focus","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":true,"linked":true,"task_link_count":1},{"ref":"6:ddf7159c","line":6,"name":"READING","slug":"reading","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":false,"linked":false,"task_link_count":0}],"capture":{"block_id":"ref-attention","block_link":"[[sase#^ref-attention]]","created":"2026-10-16","creates_pomodoro":true,"day_file":"/tmp/bob-cli-8f.1-json/vaults/moved/day.md","dry_run":false,"kind":"pomodoro_link","ok":true,"placement":"linked","pomodoro_link_action":"moved","pomodoro_link_destination":{"line":3,"name":"FOCUS","role":"created"},"pomodoro_link_placement":"inserted","pomodoro_link_source":{"line":2,"name":"CURRENT","time_range":"0900-0930"},"pomodoro_name":"FOCUS","previous_status_name":"Ready","previous_status_symbol":" ","previous_task_line":"- [ ] #task #ref [[ref/papers/attention]] ^ref-attention","relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"status_changed":true,"status_name":"Next","status_symbol":"*","target":"/tmp/bob-cli-8f.1-json/vaults/moved/sase.md","task_line":"- [*] #task #ref [[ref/papers/attention]] [fresh:: 2026-10-16] ^ref-attention","text":""}}
\```

\## already_current
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"write","changed":false,"ref":{"path":"ref/papers/attention.md","link":"[[ref/papers/attention]]","title":"Attention Is All You Need","marker_id":"attention"},"task":{"path":"sase.md","block_id":"ref-attention","link":"[[sase#^ref-attention]]","status_symbol":"*","status_name":"Next"},"pomodoros":[{"ref":"2:4e8b857b","line":2,"name":"CURRENT","slug":"current","time_range":"0900-0930","placeholder":false,"starts_at":"2026-10-16T09:00","ends_at":"2026-10-16T09:30","running":true,"default":false,"linked":false,"task_link_count":0},{"ref":"4:ddf7159c","line":4,"name":"READING","slug":"reading","time_range":null,"placeholder":true,"starts_at":null,"ends_at":null,"running":false,"default":true,"linked":true,"task_link_count":1}],"capture":{"block_id":"ref-attention","block_link":"[[sase#^ref-attention]]","created":"2026-10-16","creates_pomodoro":false,"day_file":"/tmp/bob-cli-8f.1-json/vaults/already_current/day.md","dry_run":false,"kind":"pomodoro_link","ok":true,"placement":"linked","pomodoro_link_action":"already_current","pomodoro_link_destination":{"line":4,"name":"READING","role":"next_up"},"pomodoro_link_source":{"line":4,"name":"READING"},"pomodoro_name":"READING","previous_status_name":"Next","previous_status_symbol":"*","previous_task_line":"- [*] #task #ref [[ref/papers/attention]] ^ref-attention","relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"status_changed":false,"status_name":"Next","status_symbol":"*","target":"/tmp/bob-cli-8f.1-json/vaults/already_current/sase.md","task_line":"- [*] #task #ref [[ref/papers/attention]] ^ref-attention","text":""}}
\```

\## link_guard
\```json
{"ok":true,"schema_version":1,"command":"ref today","generated_at":"2026-10-16T09:15:00","mode":"write","changed":true,"ref":{"path":"ref/papers/attention.md"

… and 3880 more characters

## Attachments

- 🔒 README.md · text/markdown · 778 bytes (private attachment)
- 🔒 already\_current.json · application/json · 1.68945 KiB (private attachment)
- 🔒 created.json · application/json · 1.8584 KiB (private attachment)
- 🔒 link\_guard.json · application/json · 1.5293 KiB (private attachment)
- 🔒 linked.json · application/json · 1.69434 KiB (private attachment)
- 🔒 listing.json · application/json · 1.69824 KiB (private attachment)
- 🔒 moved.json · application/json · 1.92773 KiB (private attachment)
- 🔒 multiple\_running.json · application/json · 969 bytes (private attachment)

## Dependencies

- **Blocks:** [bob-cli-8f.2](bob-cli-8f.2.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8f.1/README.md) | [bob-cli-8f.1](bob-cli-8f.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3c2721`](https://github.com/bobs-org/bob-cli/commit/a3c27210555bfaea7a309cf3772ff39a1fcdfd7d) | feat(ref): add bob ref today to link a reading task under today's Pomodoro | [bob-cli-8f.1](bob-cli-8f.1.md) | 2026-10-16 11:17:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8f.1][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-8f.2][2] | Need real CLI ref-today JSON fixtures and completed contract details | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8f.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8f.2/README.md

<!-- sase:referenced-by:end -->
