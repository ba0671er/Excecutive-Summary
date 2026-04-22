# Drive Map / ローデータ格納庫の地図

> 全エージェント必読。ローデータが必要なときは、まずここを見て該当フォルダIDを確認する。
> 大容量バイナリ・機密ファイルは全てここ（Google Drive）にあり、リポジトリには存在しない。

---

## ルートフォルダ

- 名称: **AI Company**
- ID: `1cmewlKNMgkwcJVUpUpjvPtzDBda_Bc30`
- URL: https://drive.google.com/drive/folders/1cmewlKNMgkwcJVUpUpjvPtzDBda_Bc30
- オーナー: ba0671er@gmail.com

---

## フォルダ構成とID一覧

| パス | 用途 | フォルダID |
|------|------|-----------|
| `01_clients/` | ECコンサル・クライアント別データ | `18jJLTvkanCVisQvbMcsN6SUV1mDUknGT` |
| `02_own-ec/` | 自社EC関連 | `1sKmj3jhLCdOYxrYbHYeyI9k9GhEjkbRN` |
| `02_own-ec/products/` | 商品仕様書・PDF・取説 | `1CXiHfHX_aNY99utgiAYmMM7XAjI300jt` |
| `02_own-ec/photos/` | 商品写真・撮影素材 | `13_SlRYZmCMWEemcluOZw5xLJnCbUra9v` |
| `02_own-ec/sales-data/` | 売上CSV・注文エクスポート | `1uNlF1waiUyghHr2YdVPFmGPUR4ScdtGb` |
| `02_own-ec/ads-data/` | 広告管理画面エクスポート | `1CHtE-Cz1pq1WU2vBhW1aTOWvcWC54XRA` |
| `03_research/` | 仕入れ・OEMリサーチ | `1ygj0bmbMKpVFwaHM6u6ohcz1tJt_MMTy` |
| `03_research/candidates/` | 仕入れ候補商品素材 | `1B_cE6QzwNGPl58VFBfPoO1uag-6wjmzK` |
| `03_research/suppliers/` | 仕入先・工場資料 | `1DyE6xbEFKa-5TIuRpu3_90lbpFyO_hzJ` |
| `03_research/oem-projects/` | OEM案件別フォルダ | `14k-u2yfFXClbiBwNvNGxo7OwvmzmlwQn` |
| `04_creative-assets/` | デザイン素材（PSD/動画/ロゴ） | `17Sw7YfMbtruH-N1LeCa8HJWm_ZH0bPgG` |
| `05_contracts/` | 契約書・NDA・見積原本（機密） | `1yr0iNEb_l7mu6MKq45rV8obXgAIMsWzk` |
| `06_inbox/` | 未分類データ一時置き | `1HVTzVhiMZX1Qs4ZXBj-DedaNj2JW09ov` |

---

## エージェントの利用ルール

### ローデータが欲しいとき
1. この地図で該当フォルダIDを特定
2. Drive MCP の `search_files` でフォルダ内を検索
   - クエリ例: `title contains '2026-04' and mimeType = 'text/csv'`
3. `get_file_metadata` でメタ情報確認
4. `read_file_content` / `download_file_content` で中身取得

### 加工後の扱い
- 加工・要約した結果は **このリポジトリの `knowledge/` または `outputs/`** に置く
- Driveには加工データを戻さない（役割分離）

### 新フォルダ追加時
- `create_file` に `mimeType: application/vnd.google-apps.folder` と `parentId` で作成
- 作成したら必ずこの地図に追記して commit する

---

## ここに何を置く / 置かない

| 置く | 置かない |
|------|---------|
| 画像・動画・PSD | 加工済み分析結果（→ `knowledge/`） |
| PDF・契約書スキャン | 成果物最終版（→ `outputs/`） |
| 大容量CSV | テキストメモ・議事録（→ `data/` または `outputs/`） |
| 奥付書類・設計図 | エージェント定義・マニュアル（→ `agents/`, `guidelines/`） |

---

## 命名規則

- ファイル名冒頭に日付: `YYYY-MM-DD_内容.拡張子`
  - 例: `2026-04-22_楽天売上_A社.csv`
- 月次データは `YYYY-MM_内容.ext` でも可
- スペース・記号は避け、アンダースコアで区切る

---

## 機密管理

- `05_contracts/` 配下は共有権限を最小に保つ
- 原則として共有範囲を広げる変更は **ユーザー承認必須**
- 各エージェントは `05_contracts/` を読むときに必要性をログに残す

---

## 更新履歴

- 2026-04-22: 初期構築。ルート + 6トップ + 7サブフォルダ + README 作成
