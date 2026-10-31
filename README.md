# Obsidian Idea Board

[Obsidian](https://obsidian.md/) 向けの、Markdownリスト（`- `）駆動型アイデア＆ストーリーボードプラグインです。  
Matthew Meyers 氏による [obsidian-kanban](https://github.com/mgmeyers/obsidian-kanban) をベースに、**「タスク管理ではなく、アイデア管理」** に特化するようカスタマイズされています。

---

## 主な特徴

### 1. チェックボックス不要の純粋リスト管理
- 通常のKanbanでは必須だった `- [ ]`（チェックボックス）の制約を排除しました。
- 純粋な箇条書きリスト（`- カード本文`）としてカードを保存・読み書きするため、アイデアなどを「未完了タスク」として扱わずに整理できます。

### 2. 公式 Kanban プラグインとの完全共存
- 本プラグインを導入しても、既存の `obsidian-kanban` と競合しません。
  - フロントマターが `kanban-plugin: board` のノート → **従来のKanban**（タスク管理用）で開く
  - フロントマターが `idea-board: board` のノート → **Idea Board**（ネタ・構成用）で開く
- 左右分割ペインで「タスク用Kanban」と「Idea Board」を同時に並べ、**カードをドラッグ＆ドロップで相互に行き来させる**ことも可能です。

### 3. 上部「粒度フィルターバー」常設
- ボード上部にクイックフィルターバーを搭載：
  - `すべて` / `💡 構想 (#idea)` / `💬 フレーズ (#phrase)` / `⚙️ 設定 (#setting)` / `🎭 キャラ (#char)`
- クリック一つで、ボード全体のカードから特定の粒度だけを瞬時に絞り込み表示できます。

### 4. カードごとの粒度メニュー＆カラーコーディング
- 各カードのメニュー（`...` または右クリック）の最上部から、ワンクリックで粒度タグを付与・切り替えできます。
- 粒度タグに応じた色分けボーダーがカード左端に適用され、視覚的に情報の種別を把握しやすくなります。

---

## 使い方

### ノートの作成
新規ノートを作成し、フロントマターに以下のように記述します：

```markdown
---
idea-board: board
---

## 💡 ネタ・着想
- ここに着想を記述

## 🎭 キャラ・動機
- キャラクターの設定

## 🎬 構成・展開
- シーン展開

## 📝 執筆中
- ドラフト

## 📦 保留・ボツ
- ストック
```

### コマンド
- コマンドパレット（`Ctrl + P` / `Cmd + P`）から：
  - **`Idea Board: Create new idea board`**: 新しいIdea Boardノートを作成
  - **`Idea Board: Toggle between Idea Board and markdown mode`**: マークダウン表示とボード表示の切り替え

---

## インストール方法

### 手動インストール
1. 本リポジトリの最新リリースから `main.js`, `manifest.json`, `styles.css` をダウンロードします。
2. ObsidianのVault内のフォルダ `.obsidian/plugins/obsidian-idea-board/` を作成し、3ファイルを配置します。
3. Obsidianの「設定」＞「コミュニティプラグイン」を開き、一覧の「Idea Board」を有効化します。

### BRAT（Beta Reviewers Auto-update Tester）を使用する場合
1. Obsidianプラグイン「Obsidian42 - BRAT」をインストール・有効化します。
2. コマンドパレットから `BRAT: Add a beta plugin for testing` を実行します。
3. 本リポジトリのURLを入力して追加します。

---

## ライセンス・謝辞 (Credits)

本プラグインは Matthew Meyers 氏による [obsidian-kanban](https://github.com/mgmeyers/obsidian-kanban)（MIT License）をフォーク・拡張して作成されました。  
優れた基盤コードを公開・メンテナンスされている原作者およびコミュニティに深く感謝いたします。

MIT License (c) 2020-2023 Matthew Meyers / (c) 2026 obsidian-idea-board contributors.
詳細は [LICENSE](LICENSE) をご覧ください。
