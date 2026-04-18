# 広告運用部門 ルーター

## 部門ミッション
モール内広告（RPP、アイテムマッチ、スポンサープロダクト等）と
モール外広告（GDN/Meta/LINE等）の設計・運用・改善。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| 広告オペレーター | `agents/ad-ops/ad-operator.md` | 入稿設計、キーワード設計、日次運用 |
| 広告アナリスト | `agents/ad-ops/ad-analyst.md` | 効果分析、改善仮説、レポート作成 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「RPPのキーワード設計」「入稿表を作って」 | ad-operator |
| 「先週の広告レポート」「CPA悪化の要因分析」 | ad-analyst |
| 「月次レビュー＋来月の改善案」 | ad-analyst → ad-operator（直列） |

## 参照マニュアル
- `guidelines/ad-operations.md`
- `guidelines/ec-platforms.md`
- `guidelines/data-analysis.md`

## 参照テンプレート
- `templates/ad-report.md`

## 品質管理
予算変更・新規媒体は必ずユーザー確認。レポートは `quality/reviewer.md`。
