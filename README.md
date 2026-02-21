<p align="center">
  <strong>地獄のAI</strong><br>
  <sub>人間 vs GPT — 謎解きRPG型体験イベント</sub>
</p>

<p align="center">
  <a href="https://jigoku-ai.conect.llc/">🌐 本番サイト</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/yukihiroyamaguchi569/Hell_AI_landing_page">📦 Repository</a>
</p>

---

### これは何？

**ChatGPT が鬼**を演じる、対話型謎解きRPGイベント「地獄のAI」のランディングページです。  
案内・チケット販売・開催予定を掲載する静的サイトで、GitHub Pages でホスティングしています。

- **本番**: [https://jigoku-ai.conect.llc/](https://jigoku-ai.conect.llc/)
- **ホスティング**: GitHub Pages（`CNAME` でカスタムドメイン）

---

### 技術スタック

| 項目 | 内容 |
|------|------|
| **スタイル** | Tailwind CSS（CDN v2.2.19）— ビルド不要 |
| **フォント** | Google Fonts（Noto Sans JP） |
| **スクリプト** | なし（静的HTMLのみ） |

---

### プロジェクト構成

| パス | 説明 |
|------|------|
| `index.html` | メインLP（チケットリンクは2箇所あるので更新時は両方修正） |
| `legal-information.html` | 特定商取引法に基づく表示 |
| `privacy-policy.html` | プライバシーポリシー |
| `images/` | ゲームプレイ写真・OGP（`images/ogp.jpg`）など |
| `CNAME` | カスタムドメイン用 |

画像のうち、鬼キャラ・メインビジュアルは Vercel Blob Storage の外部URLを参照しています。

---

### ローカルで確認する

ビルドは不要です。ルートでサーバーを立てて表示してください。

```bash
python3 -m http.server 8000
```

→ **http://localhost:8000** で確認

---

### 注意（編集時）

- チケットボタンは `index.html` 内に**2箇所**（上部・参加案内）あるため、リンク変更時は両方を更新すること。
