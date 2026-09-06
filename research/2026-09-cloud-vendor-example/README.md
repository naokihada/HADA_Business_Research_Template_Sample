# Cloud Backup Vendor Comparison — Sample Demo

**project_id:** 2026-09-cloud-vendor-example  
**Config:** config/research/2026-09-cloud-vendor-example/  
**evidence_mode:** simulated

## Objective / 調査目的

架空の小規模チーム向けにクラウドバックアップベンダーを比較する。
本プロジェクトは Sample リポジトリのデモであり、実在ベンダーデータは含まない。

## Principles / 原則

- 証拠に基づく評価 — 推測を事実として扱わない
- ゲート、スコア、信頼度、推薦区分を分離する
- マスターデータを外部調査で silently 更新しない
- UNKNOWN は有効な結果
- すべての証拠は SIMULATED（模擬）

## Candidate Universe / 候補

| ID | Name | Wave | Source |
|---|---|---|---|
| W1-001 | Nimbus Vault Backup | wave1 | vendor_directory_alpha |
| W1-002 | ArcStore Cloud | wave1 | vendor_directory_alpha |
| W1-003 | DataHaven Lite | wave1 | vendor_directory_alpha |
| W2-001 | SecureLoop Backup | wave2 | analyst_shortlist_beta |

## Directory Layout

| Path | Purpose |
|---|---|
| candidates/ | Dossiers |
| evidence/ | Simulated evidence and QC records |
| scoring/ | CSV aggregates |
| shortlist/ | Shortlist output |
| reports/ | Dated reports |
| sources/ | Discovery and entity resolution notes |

## Workflow Status (Demo)

Completed fictional pipeline for demonstration:

discovery → dossiers → entity resolution → evidence → gates → scoring →
confidence → QC → ranking → shortlist → report
