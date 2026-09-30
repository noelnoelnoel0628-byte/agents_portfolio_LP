# MY AGENTS. | nao ポートフォリオ LP

> 困りごとから、エージェントが生まれる。

イラスト・Webデザイン／AIエージェント開発を行う **nao（でざいんていらー）** のポートフォリオ用ランディングページです。日々の困りごとをきっかけに自作した10体のAIエージェントを紹介し、制作相談・お仕事のご相談につなげます。

- 公開URL: https://nao-portfolio-lp.vercel.app/

## ページ構成

`index.html` 1枚で完結する、シングルページのLPです。

| セクション | 内容 |
| --- | --- |
| HERO | キャッチコピーとキービジュアル |
| ABOUT (`#about`) | なぜ自分でエージェントをつくるのか／プロフィール |
| WORKS (`#works`) | 自作AIエージェント10体のカード一覧、準備中のエージェント（COMING SOON） |
| CONTACT (`#contact`) | 問い合わせフォーム・LINE・SNSへの導線 |

### 掲載しているエージェント

| 名前 | ジャンル |
| --- | --- |
| manga-maker | 漫画制作（6体のAIチーム） |
| marketing-strategist | SNS運用・マーケティング |
| design-consultant | Webデザイン |
| security-guard | セキュリティ |
| customer-support-advisor | カスタマーサポート |
| accounting-helper | 経理 |
| research-assistant | リサーチ |
| legal-advisor | 契約・法務 |
| content-creator | コンテンツ制作 |
| chirashi-ai | チラシ制作（MVP） |

## ファイル構成

```
.
├── index.html   # ページ本体（HTML と CSS を1ファイルに記述）
└── images/      # 画像（PC/モバイル用のヒーロー・ABOUT、各エージェントのイラスト、favicon、OGP）
```

## 技術・特徴

- ビルド不要の静的サイト（HTML / CSS のみ。JavaScript フレームワークなし）
- レスポンシブ対応（760px 以下でモバイル用画像に切り替え）
- 画像は WebP（OGP のみ JPG）、遅延読み込み（`loading="lazy"`）
- Google Fonts（Zen Kaku Gothic New / Noto Sans JP / Poppins）を使用
- OGP / Twitter Card 設定済み

## 使い方

### ローカルで確認する

ビルドは不要です。`index.html` をブラウザで開くだけで表示できます。

```bash
# 簡易サーバーで確認したい場合
python3 -m http.server 8000
# → http://localhost:8000 を開く
```

### 内容を編集する

すべて `index.html` を編集します。

- **エージェントを追加・変更する**: `#works` 内の `<div class="work-card">` をコピーして、タグ・キャッチ・説明・名前・画像を書き換えます。画像は `images/` に置き、`<img src="images/xxx.webp">` で指定します。
- **プロフィールを変更する**: `#about` 内の `profile-row` を編集します。
- **問い合わせ先を変更する**: `#contact` 内のフォーム・LINE・SNS（X / Instagram / Facebook）のリンクを差し替えます。
- **配色・フォント**: `<style>` 冒頭の CSS 変数（`:root`）で調整できます。
- **公開時の見え方**: `<head>` 内の `<title>`、`description`、OGP（`og:*`）、`images/ogp-image.jpg` を更新します。

### 公開（デプロイ）する

静的ファイルだけなので、Vercel・GitHub Pages・Netlify などにそのまま配置できます。現在は Vercel で公開しています。リポジトリのルートを公開ディレクトリに指定してください。

## 画像について

`images/` 内のイラストは本ポートフォリオ用の素材です。無断での転載・再利用はご遠慮ください。

## お問い合わせ

お仕事・制作のご相談は、LP内の「話してみる」ボタン（Googleフォーム）または LINE からお願いします。
