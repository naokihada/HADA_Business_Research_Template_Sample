# 調査レポート — クラウドバックアップベンダー比較（例示）

**Report date:** 2026-09-06  
**Project:** 2026-09-cloud-vendor-example  
**Language:** ja

---

## 1. 調査目的

架空の小規模チーム向けクラウドバックアップベンダーを、証拠に基づき比較する。
本レポートはテンプレート例示用であり、実在ベンダーではない。

## 2. 調査範囲

| 項目 | 内容 |
|---|---|
| 候補数 | 4（wave1: 3、wave2: 1） |
| QC | source_quality_review |
| 設定 | config/research/_example_project/ |

## 3. 方法

マスター候補リスト → ドシエ → ゲート → スコア → 信頼度 → QC → ショートリスト

## 4. 主要結果

### 適格性

| Status | Count |
|---|---|
| ELIGIBLE | 2 |
| CONDITIONAL | 1 |
| NOT_ELIGIBLE | 1 |

### 推薦区分

| Recommendation | Count |
|---|---|
| A | 1 |
| B | 2 |
| D | 1 |

## 5. 推奨候補

| Rank | ID | Name | Score | Confidence | Tier |
|---|---|---|---|---|---|
| 1 | W1-001 | Nimbus Vault Backup | 82 | MEDIUM | TIER_1 |
| 2 | W1-002 | ArcStore Cloud | 68 | MEDIUM | TIER_2 |
| 3 | W2-001 | SecureLoop Backup | 74 | LOW | TIER_2 |

## 6. 除外

| ID | Reason |
|---|---|
| W1-003 | 個人向け製品 — core_service_match NO |

## 7. 未確認事項

- W1-001: SSO の最終確認
- W2-001: 料金、SSO、日本 coverage

## 8. 次のステップ

1. TIER_1 候補に問い合わせ
2. UNKNOWN 項目の確認
3. トライアル実施

## 9. 免責

スコア、信頼度、推薦区分は別概念。高スコアは高信頼度を意味しない。
本レポートは意思決定支援であり、最終判断は人間が行う。

## 10. 参照

| Artifact | Path |
|---|---|
| Scoring | research/2026-09-cloud-vendor-example/scoring/scoring_results.csv |
| Shortlist | research/2026-09-cloud-vendor-example/shortlist/shortlist.md |
| Log | logs/research/2026-09-cloud-vendor-example.md |
