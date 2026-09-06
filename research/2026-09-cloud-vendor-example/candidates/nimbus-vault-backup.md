# Nimbus Vault Backup — Dossier

## 1. Identity

| Field | Value |
|---|---|
| candidate_id | W1-001 |
| display_name | Nimbus Vault Backup |
| organization | Nimbus Vault Inc |
| entity_type | ORGANIZATION |
| website | https://example.invalid/nimbus |
| research_date | 2026-09-06 |
| wave_id | wave1 |
| source | vendor_directory_alpha |

## 2. Entity Resolution

| Field | Value |
|---|---|
| canonical_entity | Nimbus Vault Inc |
| possible_duplicates | none |
| identity_confidence | HIGH |

## 3. Capability Matrix

| Requirement ID | Status | Classification | Evidence |
|---|---|---|---|
| backup_scope | YES | VERIFIED | example.invalid/nimbus/features |
| restore_options | YES | VERIFIED | point-in-time restore documented |
| encryption | YES | VERIFIED | AES-256 at rest stated |
| api_available | YES | VERIFIED | REST API docs linked |
| sso_support | LIKELY | STATED | SAML mentioned; not independently tested |
| pricing_public | YES | VERIFIED | pricing page with calculator |

## 4. Eligibility Gates

| Gate ID | Status | Evidence |
|---|---|---|
| currently_operating | YES | active product pages |
| core_service_match | YES | backup primary product |
| geographic_coverage | YES | US + JP regions listed |
| enterprise_sso | LIKELY | SAML stated |
| api_integration | YES | API docs |
| contract_flexibility | YES | monthly plan listed |

## 5. Scoring Reference

| Field | Value |
|---|---|
| score_total | 82 |
| confidence | MEDIUM |
| recommendation | A |
| eligibility_status | ELIGIBLE |

## 6. Recommendation Summary

Strong fictional fit for team backup with API and JP/US coverage.
SSO remains LIKELY — confirm before final selection.
