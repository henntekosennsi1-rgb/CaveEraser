# CaveEraser - 水中洞窟埋め立てプラグイン

水中洞窟を検出して埋め立てるSpigotプラグインです。岩盤整地作業を効率化します。

---

## 機能

- 🔍 **洞窟スキャン** - 指定範囲内の水中洞窟を自動検出
- 🏗️ **埋め立て機能** - 検出した洞窟を指定ブロックで埋め立て
- 🧊 **チャンク埋め立て** - チャンク内の水・溶岩・空気を一括変換
- ⚡ **非同期処理** - TPSを維持しながら大規模処理
- 💎 **EmeraldBank連携** - 埋め立てコストをエメラルドで請求

---

## コマンド

| コマンド | 説明 |
|---------|------|
| `/caveerase scan [半径]` | 水中洞窟をスキャン |
| `/caveerase list` | 検出した洞窟一覧 |
| `/caveerase info <ID>` | 洞窟の詳細情報 |
| `/caveerase fill <ID> [ブロック]` | 洞窟を埋め立て |
| `/caveerase auto [半径] [ブロック]` | 自動スキャン＆埋め立て |
| `/caveerase chunkfill [半径] [ブロック]` | チャンク一括埋め立て |
| `/caveerase reload` | 設定再読み込み |

**エイリアス:** `/ce`

---

## 権限

**⚠️ 重要: OP権限だけでは使用できません！**

| 権限 | 説明 | デフォルト |
|------|------|-----------|
| `caveeraser.*` | 全権限 | false |
| `caveeraser.scan` | スキャン | false |
| `caveeraser.fill` | 埋め立て | false |
| `caveeraser.auto` | 自動埋め立て | false |
| `caveeraser.chunkfill` | チャンク埋め立て | false |
| `caveeraser.reload` | リロード | false |
```bash
# LuckPerms
/lp user <プレイヤー> permission set caveeraser.* true
```

---

## 検出制限

| 制限 | デフォルト | 説明 |
|------|-----------|------|
| 最大体積 | 100,000 | 整地済みエリアを除外 |
| 最小水ブロック | 1 | 水がない空洞を除外 |
| Y座標範囲 | -64〜320 | 全高度対応 |

---

## 動作環境

- Spigot/Paper 1.21.x
- Java 17以上
- EmeraldBank（オプション）

## コミュニティ

**Discord:** https://discord.gg/zYY55dzhjd

## ライセンス

MIT License
