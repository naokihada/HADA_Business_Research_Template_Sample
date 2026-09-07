# HADA Business Research Template — Sample

**This is a demonstration repository** — a complete fictional example of how to use the reusable [HADA Business Research Template](https://github.com/naokihada/HADA_Business_Research_Template) framework.

The scenario is a **fictional cloud backup vendor comparison** with simulated evidence. It is not a recommendation of real vendors. Do not use it as a basis for purchase decisions.

Japanese information is available further down this page.

| | |
|---|---|
| **Template (framework)** | [HADA_Business_Research_Template](https://github.com/naokihada/HADA_Business_Research_Template) — reusable generic engine, skeleton config, and tools |
| **Sample (this repo)** | Complete fictional research project with outputs |

---

## What this Sample demonstrates

A public demo of the full Business Research Template pipeline using **simulated evidence** and fictional data.

| Item | Value |
|---|---|
| Scenario | Small-team cloud backup vendor comparison |
| project_id | 2026-09-cloud-vendor-example |
| evidence_mode | **simulated** — all evidence is fictional |
| Candidates | 4 (fictional) |
| URLs | example.invalid only |

Sample is not a full independent copy of Template. It includes engine files needed for standalone validation (prompts, templates, tools, AGENTS.md) plus project-specific configuration and research outputs.

---

## Relationship to Template

| Repository | Role |
|---|---|
| **[HADA_Business_Research_Template](https://github.com/naokihada/HADA_Business_Research_Template)** | Reusable framework — starting point for new projects |
| **HADA_Business_Research_Template_Sample** | This repository — demonstrates Template usage |

To start a new research project, fork or clone the **Template** repository and run bootstrap. Use this Sample to see what a completed fictional project looks like.

---

## Pipeline demonstrated

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

## Fictional candidates

| ID | Name | Wave | Demo role |
|---|---|---|---|
| W1-001 | Nimbus Vault Backup | wave1 | Shortlist TIER_1 |
| W1-002 | ArcStore Cloud | wave1 | Mid-tier candidate |
| W1-003 | DataHaven Lite | wave1 | Consumer-oriented — requirement mismatch example |
| W2-001 | SecureLoop Backup | wave2 | Wave 2 discovery — TIER_2 |

All names are fictional. URLs use example.invalid only. Not real products.

---

## How to read the artifacts

Recommended reading order:

1. [research/2026-09-cloud-vendor-example/reports/2026-09-06-final-report-ja.md](research/2026-09-cloud-vendor-example/reports/2026-09-06-final-report-ja.md) — final report
2. [research/2026-09-cloud-vendor-example/shortlist/shortlist.md](research/2026-09-cloud-vendor-example/shortlist/shortlist.md) — shortlist
3. [research/2026-09-cloud-vendor-example/scoring/](research/2026-09-cloud-vendor-example/scoring/) — scoring, QC, and ranking CSVs
4. [research/2026-09-cloud-vendor-example/candidates/](research/2026-09-cloud-vendor-example/candidates/) — dossiers
5. [research/2026-09-cloud-vendor-example/evidence/](research/2026-09-cloud-vendor-example/evidence/) — simulated evidence
6. [config/research/2026-09-cloud-vendor-example/](config/research/2026-09-cloud-vendor-example/) — gates, rubric, QC config
7. [data/master/](data/master/) — master requirements and candidate CSV
8. [logs/research/2026-09-cloud-vendor-example.md](logs/research/2026-09-cloud-vendor-example.md) — research log

---

## Core concepts in this demo

| Concept | Where to see it |
|---|---|
| Gates | evidence/eligibility/, dossiers |
| Score | scoring/scoring_results.csv |
| Confidence | confidence column in scoring_results.csv |
| Recommendation | scoring_results.csv, unified_ranking.csv |
| QC | scoring/qc_source_quality_summary.csv |
| Ranking Safety | UNKNOWN handling — see [AGENTS.md](AGENTS.md) |

Evidence flow:

```text
Claim → Evidence → Source → Confidence → Gate / Score / Decision
```

---

## Reproduce and validate

```powershell
python tools/validate_research_data.py `
  --master data/master/candidates_master.csv `
  --config-dir config/research/2026-09-cloud-vendor-example `
  --scoring research/2026-09-cloud-vendor-example/scoring/scoring_results.csv `
  --ranking research/2026-09-cloud-vendor-example/scoring/unified_ranking.csv `
  --qc-summary research/2026-09-cloud-vendor-example/scoring/qc_source_quality_summary.csv

python tools/check_prompts.py
```

CI: [.github/workflows/validate.yml](.github/workflows/validate.yml) (no secrets required)

---

## Cursor / AI exploration

1. Read [AGENTS.md](AGENTS.md)
2. Follow the artifact reading order above
3. To start new research, use the [Template repository](https://github.com/naokihada/HADA_Business_Research_Template) and run bootstrap

**Prompt rule:** Do not use nested quotations in Cursor instructions or prompt files.

AI accelerates research; it does not replace evidence.

---

## Bundled engine files

For standalone understanding and validation, this Sample includes:

- AGENTS.md, prompts/, templates/, tools/, .cursor/rules/

Use the **Template** repository as the starting point for new projects.

---

## License

Apache License 2.0.

Copyright 2026 Naoki Hada.

See [LICENSE](LICENSE) (full license text) and [NOTICE](NOTICE) (attribution).

---

## Disclaimer

- This demo is for education and template illustration only
- Fictional vendor names and simulated evidence do not represent real entities
- Actual vendor selection requires your own research and judgment
- Full disclaimer: [DISCLAIMER.md](DISCLAIMER.md)

---

# 日本語

## この Sample とは

**デモンストレーション用リポジトリ** です。再利用可能な [HADA_Business_Research_Template](https://github.com/naokihada/HADA_Business_Research_Template) フレームワークの **完成した架空例** を示します。

シナリオは **模擬証拠（simulated evidence）** 付きの架空クラウドバックアップベンダー比較です。実在ベンダーの推薦ではありません。購入判断の根拠として使用しないでください。

| | |
|---|---|
| **Template（フレームワーク）** | [HADA_Business_Research_Template](https://github.com/naokihada/HADA_Business_Research_Template) — 汎用エンジン、スケルトン設定、ツール |
| **Sample（本リポジトリ）** | 完成した架空調査プロジェクトと成果物 |

| 項目 | 内容 |
|---|---|
| シナリオ | 小規模チーム向けクラウドバックアップベンダー比較 |
| project_id | 2026-09-cloud-vendor-example |
| evidence_mode | **simulated** — すべて模擬 |
| 候補数 | 4（架空） |
| URL | example.invalid のみ |

Sample は Template の完全な独立コピーではありません。単体検証に必要なエンジンファイル（prompts, templates, tools, AGENTS.md）とプロジェクト固有の設定・成果物を含みます。

---

## Template との関係

| リポジトリ | 役割 |
|---|---|
| **[HADA_Business_Research_Template](https://github.com/naokihada/HADA_Business_Research_Template)** | 再利用可能フレームワーク — 新規プロジェクトの起点 |
| **HADA_Business_Research_Template_Sample** | 本リポジトリ — Template の使い方デモ |

新規調査を始める場合は **Template** リポジトリを fork / clone して bootstrap を実行してください。本 Sample は完成した架空プロジェクトの見本として参照します。

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
| Ranking Safety | UNKNOWN 候補の扱い — [AGENTS.md](AGENTS.md) 参照 |

証拠の流れ:

```text
Claim → Evidence → Source → Confidence → Gate / Score / Decision
```

---

## 再現・検証

```powershell
python tools/validate_research_data.py `
  --master data/master/candidates_master.csv `
  --config-dir config/research/2026-09-cloud-vendor-example `
  --scoring research/2026-09-cloud-vendor-example/scoring/scoring_results.csv `
  --ranking research/2026-09-cloud-vendor-example/scoring/unified_ranking.csv `
  --qc-summary research/2026-09-cloud-vendor-example/scoring/qc_source_quality_summary.csv

python tools/check_prompts.py
```

CI: [.github/workflows/validate.yml](.github/workflows/validate.yml)（シークレット不要）

---

## Cursor / AI での探索

1. [AGENTS.md](AGENTS.md) を読む
2. 上記の成果物読み順でたどる
3. 新規調査を始める場合は [Template リポジトリ](https://github.com/naokihada/HADA_Business_Research_Template) で bootstrap を実行

**プロンプト規則:** nested quotation（引用の入れ子）禁止。

AI は調査を加速する補助であり、証拠の代替ではありません。

---

## 同梱エンジンファイル

単体で理解・検証するため、以下を同梱しています:

- AGENTS.md, prompts/, templates/, tools/, .cursor/rules/

新規プロジェクト開始の起点としては **Template リポジトリ** を使用してください。

---

## ライセンス

Apache License 2.0.

Copyright 2026 Naoki Hada.

詳細は [LICENSE](LICENSE)（ライセンス全文）および [NOTICE](NOTICE)（帰属表示）を参照してください。

---

## 免責事項

- 本デモは教育・テンプレート説明目的の **デモンストレーション** です
- 架空ベンダー名・模擬証拠は実在を示しません
- 実際のベンダー選定には独自の調査と判断が必要です
- 詳細は [DISCLAIMER.md](DISCLAIMER.md) を参照してください
