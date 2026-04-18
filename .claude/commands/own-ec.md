# 自社EC運用部門 ルーター

## 部門ミッション
つながるEC自身が運営する自社ストアの日次運用・CS対応。
クライアントワークで培った知見を自社で実証する「R&D店舗」でもある。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| ストアオペレーター | `agents/own-ec/store-operator.md` | 商品登録、在庫管理、受注処理 |
| カスタマーサポート | `agents/own-ec/customer-support.md` | 問い合わせ対応、レビュー対応、返品処理 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「新商品を3モールに登録」「在庫アラート設計」 | store-operator |
| 「クレーム対応の返信文」「低評価レビュー対応」 | customer-support |
| 「繁忙期オペ設計」 | 両方 **並列** |

## 参照マニュアル
- `guidelines/ec-platforms.md`
- `guidelines/client-communication.md`（顧客対応の原則）
- `guidelines/compliance.md`

## 参照テンプレート
- `templates/weekly-report.md`
- `templates/meeting-minutes.md`

## 品質管理
返信テンプレ改変・レビュー公開対応は `quality/reviewer.md`。
