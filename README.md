# portfolio

ポートフォリオサイト用リポジトリです。

## 現在の実装
- フレームワーク: Astro
- デプロイ想定: Cloudflare Pages
- デザイン方針: glasshopper 系の暖色 + ミントアクセント + 透明感のある UI
- 構成: 1ページのポートフォリオ（Hero / About / Values & Skills / Works / How I Work / Contact）
- ダークモード切り替えあり

## コンテンツについて
- `src/data/siteContent.ts` に文面を集約しています
- Notion の以下ページをもとに、公開向けに前向きな表現へ再構成しています
  - キャリア
  - 経歴
  - モチベーション
  - キャリアチェンジの動機
  - ポートフォリオ
- 取得には Notion API を利用しています
- そのままの転載ではなく、公開用ポートフォリオとして読みやすく整形しています

## 開発コマンド
```bash
pnpm install
pnpm dev
pnpm build
pnpm preview
pnpm cf:build
pnpm cf:deploy
pnpm cf:deploy:prod
```

## Cloudflare Pages
- `wrangler.toml` で `pages_build_output_dir = "dist"` を設定しています
- プロジェクト名は `shio3ch-portfolio` を想定しています
- 本番デプロイは `pnpm cf:deploy:prod` で実行できます

## 次の作業候補
1. Cloudflare Pages の本番 URL / カスタムドメインを設定する
2. OGP / favicon / メタデータを整える
3. 必要なら実績ページや詳細ページを増やす
