# DataHaven Lite — Dossier

## 1. Identity

| Field | Value |
|---|---|
| candidate_id | W1-003 |
| display_name | DataHaven Lite |
| organization | DataHaven Lite |
| entity_type | ORGANIZATION |
| website | https://example.invalid/datahaven |
| research_date | 2026-09-06 |
| wave_id | wave1 |

## 2. Entity Resolution

Consumer backup product — not enterprise team admin focus.

## 3. Capability Matrix

| Requirement ID | Status | Classification |
|---|---|---|
| backup_scope | YES | VERIFIED (personal files only) |
| restore_options | LIKELY | STATED |
| encryption | YES | VERIFIED |
| api_available | NO | VERIFIED |
| sso_support | NO | VERIFIED |
| pricing_public | YES | VERIFIED |

## 4. Eligibility Gates

| Gate ID | Status |
|---|---|
| currently_operating | YES |
| core_service_match | NO |
| geographic_coverage | YES |
| enterprise_sso | NO |
| api_integration | NO |

## 5. Scoring Reference

| Field | Value |
|---|---|
| score_total | 38 |
| confidence | HIGH |
| recommendation | D |
| eligibility_status | NOT_ELIGIBLE |

## 6. Recommendation Summary

Consumer product — fails core_service_match for team enterprise backup scope.
