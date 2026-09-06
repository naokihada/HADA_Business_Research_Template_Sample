# Shortlist — 2026-09-cloud-vendor-example

**Generated:** 2026-09-06  
**Rules:** config/research/_example_project/shortlist_rules.yaml

## Summary

| Tier | Count |
|---|---|
| TIER_1 | 1 |
| TIER_2 | 2 |
| EXCLUDED | 1 |

## Tier 1 — First Contact

| Rank | candidate_id | Name | Score | Confidence | Recommendation | Key Strengths | Unresolved |
|---|---|---|---|---|---|---|---|
| 1 | W1-001 | Nimbus Vault Backup | 82 | MEDIUM | A | API, JP/US, encryption | SSO confirm |

## Tier 2 — Strong Alternative

| Rank | candidate_id | Name | Score | Confidence | Recommendation | Notes |
|---|---|---|---|---|---|---|
| 2 | W2-001 | SecureLoop Backup | 74 | LOW | B | Wave2; pricing unknown |
| 3 | W1-002 | ArcStore Cloud | 68 | MEDIUM | B | No SSO |

## Excluded

| candidate_id | Name | Reason |
|---|---|---|
| W1-003 | DataHaven Lite | NOT_ELIGIBLE — consumer product; core_service_match NO |

## Contact Priority

1. W1-001 — highest score + gates confirmed
2. W1-002 — higher confidence than W2-001 despite lower score
3. W2-001 — after pricing/SSO confirmation

Priority differs from pure score order: W1-002 ranked before W2-001 due to confidence.

## Rules Applied

Shortlist is not score-only. W1-003 excluded by hard gate failure despite completing research.
