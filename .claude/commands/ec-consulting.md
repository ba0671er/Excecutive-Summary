# ECコンサル戦略部門 ルーター

## 部門ミッション
クライアントのEC売上を伸ばす戦略立案と、モール別の具体施策への落とし込み。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| 戦略プランナー | `agents/ec-consulting/strategy-planner.md` | 全体戦略・診断・KPI設計 |
| モール専門家 | `agents/ec-consulting/platform-specialist.md` | Y!/楽天/Qoo10/Amazon 各モールの実装論 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「このクライアントの現状診断して」「KPI設計して」 | strategy-planner |
| 「楽天スーパーSALEの打ち手」「Amazonのカート取得改善」 | platform-specialist |
| 「3ヶ月の改善ロードマップ」 | strategy-planner → platform-specialist（直列） |
| モール横断の戦略 | 両方を **並列** 起動して統合 |

## 参照マニュアル
- `guidelines/ec-platforms.md`（モール仕様・規約の一次情報）
- `guidelines/data-analysis.md`
- `guidelines/brand-voice.md`

## 参照テンプレート
- `templates/strategy-deck.md`
- `templates/weekly-report.md`

## 品質管理
戦略シートはクライアント提示前に `quality/reviewer.md` を通す。
