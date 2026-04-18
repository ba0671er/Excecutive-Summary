# 仕入れ・OEM部門 ルーター

## 部門ミッション
売れる商品の発掘、仕入れ先への営業、そしてOEM開発のプロジェクト管理。
「つくりての想い」に共感できるメーカー・工場と関係をつくる。

## 所属エージェント

| エージェント | ファイル | 担当 |
|------------|---------|------|
| 商品リサーチャー | `agents/procurement/product-researcher.md` | トレンド・売れ筋リサーチ、仕入れ候補選定 |
| OEMコーディネーター | `agents/procurement/oem-coordinator.md` | 工場折衝、仕様書作成、量産進行管理 |

## ルーティング指針

| ユーザー依頼の例 | 起動エージェント |
|-----------------|-----------------|
| 「〇〇カテゴリの売れ筋10選」「仕入れ候補リサーチ」 | product-researcher |
| 「OEM仕様書ドラフト」「工場への問い合わせ文」 | oem-coordinator |
| 「新ブランド立ち上げ」 | product-researcher → oem-coordinator（直列） |

## 参照マニュアル
- `guidelines/procurement-standards.md`
- `guidelines/oem-process.md`
- `guidelines/compliance.md`（景表法・PL法）

## 参照テンプレート
- `templates/product-research.md`

## 品質管理
**仕入れ確定・OEM発注はユーザー承認必須**。
外部送信文は `quality/reviewer.md` を通す。
