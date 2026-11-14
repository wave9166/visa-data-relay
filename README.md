# visa-data-relay

Public data relay for a personal news monitor. Files here are machine-written
by automation and overwritten on each run. History is kept by Git.

- `visa_bulletin_cache.json`: US Visa Bulletin dates (China, EB-1/EB-2) and
  USCIS I-140 processing-time cache, in the monitor's cache format.
- `processing_times_cache.json`: USCIS I-140 processing times (EB-1A/NIW).
- `audit/audit_candidates.json`: weekly missed-report audit candidates for
  Amazon US cross-border sellers (tariffs, customs, compliance, fees,
  logistics, FX/oil), past 7 days only, official sources first.

All data is public. No accounts, passwords or tokens are stored in this repo.
