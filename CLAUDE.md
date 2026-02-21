# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

「地獄のAI」イベントのランディングページ。ChatGPTが鬼を演じる謎解きRPG型イベントの案内・チケット販売・開催予定を掲載する静的HTMLサイト。

- **本番URL**: https://jigoku-ai.conect.llc/
- **ホスティング**: GitHub Pages（カスタムドメインは `CNAME` で設定）

## ローカル確認

ビルド不要。`index.html` をブラウザで直接開くか、ローカルサーバーを使用する：

```bash
python3 -m http.server 8000
# → http://localhost:8000 で確認
```

## 構成

| ファイル | 役割 |
|---|---|
| `index.html` | メインランディングページ |
| `legal-information.html` | 特定商取引法に基づく表示 |
| `images/` | ローカル画像（ゲームプレイ写真・OGP画像など） |
| `favicon.ico`, `apple-touch-icon.png` | ルートに配置（GitHub Pages の仕様上） |
| `CNAME` | カスタムドメイン設定 |

## 技術スタック

- **Tailwind CSS**: CDN 経由（v2.2.19）でロード。ビルドステップなし
- **Google Fonts**: `Noto Sans JP` を `<link rel="preconnect">` + `<link>` タグで読み込み（`@import` は使わない）
- **JavaScript**: 使用なし

## 画像について

- ゲームプレイ・記念写真 → `images/` ディレクトリのローカルファイル
- 鬼キャラクター・メインビジュアル → Vercel Blob Storage の外部URL（`hebbkx1anhila5yf.public.blob.vercel-storage.com`）
- `images/ogp.jpg` がOGP・Twitterカード用の画像

## 各ページの共通パターン

両ページとも同じ構成を持つ：
- `<head>`: OGP・Twitterカードのメタタグ、canonical URL、favicon、フォント
- ヘッダー: 「地獄のAI」ロゴ（`/` へのリンク）
- フッター: copyright + `legal-information.html` へのリンク（`index.html` のみ）
- 黒背景・赤アクセントのダークテーマ

## チケットリンク更新時の注意

チケットボタンは `index.html` 内に**2箇所ずつ**（ページ上部と参加案内セクション）同一内容が存在するため、更新時は両方を修正する。
