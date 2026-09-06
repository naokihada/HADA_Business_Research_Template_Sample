# HADA Business Research Template — Sample

**これはデモンストレーション用リポジトリです。**

本リポジトリは **HADA_Business_Research_Template** 公開リポジトリを使った
**架空のクラウドバックアップベンダー比較** の完成例です。
実在ベンダーの推薦ではありません。購入判断の根拠として使用しないでください。

---

## この Sample とは

Business Research Template の全パイプラインを、**模擬証拠（simulated evidence）**
付きの架空データで示す公開デモです。

| 項目 | 内容 |
|---|---|
| シナリオ | 小規模チーム向けクラウドバックアップベンダー比較 |
| project_id | 2026-09-cloud-vendor-example |
| evidence_mode | **simulated** — すべて模擬 |
| 候補数 | 4（架空） |
| URL | example.invalid のみ |

---

## Template との関係

| リポジトリ | 役割 |
|---|---|
| **HADA_Business_Research_Template** | 汎用エンジンとスケルトン — 新規プロジェクトの起点 |
| **HADA_Business_Research_Template_Sample** | 本リポジトリ — Template の使い方デモ |

Sample は Template の**完全な独立コピーではありません**。
デモ実行に必要なエンジンファイル（prompts, templates, tools, AGENTS.md）と
プロジェクト固有の設定・成果物を含みます。

Template v0.1.0 向けに準備済み（2026-09-06）。リリースタグは commit/push 後に作成予定。

---

## デモで示すパイプライン

```text
Discovery (Wave 1 + Wave 2)
    → Candidate normalization (master CSV)
    → Entity resolution
    → Dossier research
    → Evidence (simulated)
    → Eligibility gates
    → Capability evaluation
    → Scoring
    → Confidence assessment
    → QC (source quality)
    → Unified ranking
    → Shortlist
    → Final report (Japanese)
```

---

## 架空候補一覧

| ID | 名前 | Wave | デモ上の位置づけ |
|---|---|---|---|
| W1-001 | Nimbus Vault Backup | wave1 | ショートリスト TIER_1 |
| W1-002 | ArcStore Cloud | wave1 | 中位候補 |
| W1-003 | DataHaven Lite | wave1 | 消費者向け — 要件ミスマッチ例 |
| W2-001 | SecureLoop Backup | wave2 | 第2波発見 — TIER_2 |

すべて架空。example.invalid URL。実在製品ではありません。

---

## 成果物の見方

おすすめの読み順:

1. [research/2026-09-cloud-vendor-example/reports/2026-09-06-final-report-ja.md](research/2026-09-cloud-vendor-example/reports/2026-09-06-final-report-ja.md) — 最終レポート
2. [research/2026-09-cloud-vendor-example/shortlist/shortlist.md](research/2026-09-cloud-vendor-example/shortlist/shortlist.md) — ショートリスト
3. [research/2026-09-cloud-vendor-example/scoring/](research/2026-09-cloud-vendor-example/scoring/) — スコア・QC・ランキング CSV
4. [research/2026-09-cloud-vendor-example/candidates/](research/2026-09-cloud-vendor-example/candidates/) — ドシエ
5. [research/2026-09-cloud-vendor-example/evidence/](research/2026-09-cloud-vendor-example/evidence/) — 模擬証拠
6. [config/research/2026-09-cloud-vendor-example/](config/research/2026-09-cloud-vendor-example/) — ゲート・ルーブリック・QC 設定
7. [data/master/](data/master/) — マスター要件と候補 CSV
8. [logs/research/2026-09-cloud-vendor-example.md](logs/research/2026-09-cloud-vendor-example.md) — 調査ログ

---

## 主要概念（デモ内）

| 概念 | デモでの確認場所 |
|---|---|
| Gates | evidence/eligibility/, dossiers |
| Score | scoring/scoring_results.csv |
| Confidence | scoring_results.csv の confidence 列 |
| Recommendation | scoring_results.csv, unified_ranking.csv |
| QC | scoring/qc_source_quality_summary.csv |
| Ranking Safety | UNKNOWN 候補の扱い — AGENTS.md 参照 |

---

## 再現・検証

### バリデータ

```powershell
python tools/validate_research_data.py `
  --master data/master/candidates_master.csv `
  --config-dir config/research/2026-09-cloud-vendor-example `
  --scoring research/2026-09-cloud-vendor-example/scoring/scoring_results.csv `
  --ranking research/2026-09-cloud-vendor-example/scoring/unified_ranking.csv `
  --qc-summary research/2026-09-cloud-vendor-example/scoring/qc_source_quality_summary.csv

python tools/check_prompts.py
```

### Cursor / AI での探索

1. `AGENTS.md` を読む
2. 成果物を上記の順でたどる
3. 新規調査を始める場合は Template リポジトリを fork して bootstrap を実行

---

## 含まれるエンジンファイル（Standalone 用）

デモを単体で理解・検証するため、以下を同梱しています:

- AGENTS.md, prompts/, templates/, tools/, .cursor/rules/

新規プロジェクト開始の起点としては **Template リポジトリ** を使用してください。

---

## 免責

- 本デモは教育・テンプレート説明目的です
- 架空ベンダー名・模擬証拠は実在を示しません
- 実際のベンダー選定には独自の調査と判断が必要です

---

## ライセンス

Apache License 2.0 — [LICENSE](LICENSE) と [NOTICE](NOTICE) を参照。

NOTICE の著作権表示は確認待ちのプレースホルダーです。
