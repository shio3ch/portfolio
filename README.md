# portfolio

ポートフォリオサイト用リポジトリです。

## 現在の実装
- フレームワーク: Astro
- デプロイ想定: Cloudflare
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

## Cloudflare デプロイ
- 現在の `wrangler.toml` は **Workers static assets** 方式です
- `wrangler deploy` が `dist/` を静的アセットとして配信します
- Git 連携で Cloudflare 側からビルドする場合は、ビルドコマンドを `pnpm build`、出力ディレクトリを `dist` に設定してください
- ダッシュボード上で Pages ではなく Workers の Git 連携を使う場合も、この設定で配信できます

## 次の作業候補
1. Cloudflare の本番 URL / カスタムドメインを設定する
2. OGP / favicon / メタデータを整える
3. 必要なら実績ページや詳細ページを増やす
