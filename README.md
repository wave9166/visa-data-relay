# visa-data-relay

Immigration data relay: official US government data, read by Muse's browser and published as JSON for cross-checking. Spec: 《移民数据中转规范 v1》.

## Files (repo root, `main` branch)

- `visa_relay.json` — US Visa Bulletin, U.S. Department of State (travel.state.gov). Schema `visa-relay-1`. Current bulletin month, Final Action Dates and Dates for Filing for EB-1/EB-2/EB-3 (China-mainland-born and All Chargeability Areas), previous month's charts, and whether next month's bulletin is published. Every value carries the verbatim row text from the official page (`raw`).
- `pt_relay.json` — USCIS processing times, Form I-140, EB-1A and EB-2 NIW (egov.uscis.gov/processing-times). Schema `pt-relay-1`. Created only on the first successful read of the USCIS tool; absent until then.
- `status.json` — run status. Schema `relay-status-1`. Records each run's attempt time and whether the visa bulletin and the processing-times tool were read successfully. When a source is blocked or unreadable, its data file is left unchanged and the failure is recorded here.
- `audit/audit_candidates.json` — weekly missed-news audit (schema `audit-1`).

## Rules

- Only numbers actually read on the two official pages are published. Nothing from search snippets, third-party articles, memory, or estimates.
- When a source cannot be read, its data file is not touched; only `status.json` is updated.
- No credentials, tokens, or email codes in this repo.

## Raw URLs (for server pulls)

- https://raw.githubusercontent.com/wave9166/visa-data-relay/main/visa_relay.json
- https://raw.githubusercontent.com/wave9166/visa-data-relay/main/pt_relay.json
- https://raw.githubusercontent.com/wave9166/visa-data-relay/main/status.json
