# 営業・顧客獲得部門 ルーター

## 部門ミッション
ECコンサル事業の新規クライアント獲得。リード開拓〜初回商談〜受注までを担当。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| リードハンター | `agents/sales/lead-hunter.md` | 見込み客の発掘・初回アプローチ |
| 提案書ライター | `agents/sales/proposal-writer.md` | 提案書・ヒアリングシート作成 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「〇〇ジャンルのリストを作って」「DM文面を作って」 | lead-hunter |
| 「商談用の提案書を作って」「ヒアリングシート欲しい」 | proposal-writer |
| 「新規開拓キャンペーン全体を設計」 | lead-hunter → proposal-writer（直列） |

## 参照マニュアル
- `guidelines/brand-voice.md`
- `guidelines/client-communication.md`
- `guidelines/compliance.md`

## 参照テンプレート
- `templates/proposal.md`
- `templates/meeting-minutes.md`

## 品質管理
提案書・外部送信物は必ず `agents/quality/reviewer.md` を通す。
