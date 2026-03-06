# MAGI System - Project Guide

## 概要
エヴァンゲリオン風の意思決定UIアプリ。3つのAIパネル（BALTHASAR/CASPAR/MELCHIOR）がGemini APIで並列審議し、多数決で結論を出す。

## ファイル構成
- `index.html` — メインアプリ（現行バージョン）
- `magi.html` — 旧バージョン
- `magi2.html` — 実験バージョン

## 技術スタック
- 純粋な HTML / CSS / Vanilla JS（ビルド不要）
- Gemini API（`generativelanguage.googleapis.com`）でストリーミング
- APIキーはブラウザのみで処理、サーバー送信なし

## 開発サーバー
```
# Node.js で静的配信（ポート3000）
# .claude/launch.json 経由で preview_start "static-server" を使う
```

## コーディング規約
- フレームワーク・ビルドツールは使わない（シンプルに保つ）
- スタイルは `<style>` タグ内にまとめる
- JS は `<script>` タグ内にまとめる
- CSS 変数（`--amber` 等）でテーマカラーを管理
- モバイル対応必須（`max-width: 500px` のメディアクエリあり）

## Git / GitHub
- メインブランチ: `main`
- 機能追加は `feature/` ブランチで作業
- PR は `gh pr create` で作成済みワークフロー
