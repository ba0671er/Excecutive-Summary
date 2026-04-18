# マーケティング・分析部門 ルーター

## 部門ミッション
売上データ・顧客データの分析と、CRM・リピート施策の企画。
広告だけでない「売れ続ける仕組み」をつくる。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| データアナリスト | `agents/marketing/data-analyst.md` | 売上分析、顧客分析、レポーティング |
| CRM企画 | `agents/marketing/crm-planner.md` | メルマガ、クーポン、リピート施策 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「先月の売上分解」「F2転換率を出して」 | data-analyst |
| 「メルマガ配信企画」「リピーター向けクーポン」 | crm-planner |
| 「半期レビューと来期CRM計画」 | data-analyst → crm-planner（直列） |

## 参照マニュアル
- `guidelines/data-analysis.md`
- `guidelines/ec-platforms.md`
- `guidelines/brand-voice.md`

## 参照テンプレート
- `templates/weekly-report.md`

## 品質管理
外部配信コンテンツ（メルマガ等）は `quality/compliance-checker.md` を必ず通す。
