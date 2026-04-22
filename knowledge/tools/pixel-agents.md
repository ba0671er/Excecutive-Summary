# Pixel Agents 導入判断記録

> 決定: **採用**（2026-04-22）
> 判断者: ユーザー（代表）
> 監査者: 司令塔エージェント

---

## 対象

- 名称: **Pixel Agents**
- Publisher: `pablodelucca`
- リポジトリ: https://github.com/pablodelucca/pixel-agents
- Marketplace: https://marketplace.visualstudio.com/items?itemName=pablodelucca.pixel-agents
- ライセンス: MIT
- 監査時バージョン: 1.3.0

## 目的

Claude Code で動作している複数エージェントの状態を、VSCode 内で
ピクセルアート風に可視化する。観察専用（Claude Code 本体は改変しない）。

---

## セキュリティ監査結果（2026-04-22）

### 結論: 外部通信ゼロ。つながるEC の機密データ取扱条件下でも **採用可**。

### 確認事項

| 項目 | 結果 |
|------|------|
| 本番依存パッケージ（root）| 0個 |
| 本番依存パッケージ（server/）| 0個 |
| `extension.ts` 外部通信 | なし（fetch/http/openExternal 不使用）|
| `server.ts` のHTTPサーバー | 127.0.0.1限定・動的ポート・Bearer認証・64KB制限 |
| テレメトリ・アナリティクス | なし |
| 通信経路 | 全てローカル（Claude Code Hook ↔ 拡張） |
| ライセンス | MIT（改変・監査可）|

### 軽微な指摘（実害なし）

1. Webview に CSP / localResourceRoots 未設定（ただし内容はバンドル済みローカル）
2. `externalAssetDirectories` 設定はユーザー指定可能（悪意あるパスを指定しない限り無害）

---

## 運用ルール

1. **バージョン固定**: VSCode の自動更新を OFF。手動更新時は再監査
2. **純正のみ使用**: `pablodelucca` 名義を確認。typosquat 対策
3. **`externalAssetDirectories` は使わない**
4. **メジャーアップデート時**: 監査を再実施（この記録を更新）

---

## インストール手順（VSCode）

1. 拡張機能タブを開く
2. 「Pixel Agents」で検索
3. **Publisher が `pablodelucca` であることを必ず確認**
4. インストール
5. コマンドパレット → `Pixel Agents: Show Panel`
6. 設定で自動更新 OFF（機密取扱ポリシーに基づく）

---

## 将来のカスタマイズ候補

Pixel Agents は設定ファイルでオフィスレイアウトをカスタマイズ可能。
つながるEC の 8部門構成（sales/ec-consulting/ad-ops/creative/marketing/
own-ec/procurement/quality）に合わせた配置を検討する場合は別途対応。

---

## 監査履歴

| 日付 | バージョン | 監査者 | 結果 |
|------|-----------|--------|------|
| 2026-04-22 | 1.3.0 | 司令塔 | 合格・採用 |
