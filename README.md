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
```

## 次の作業候補
1. Cloudflare 向けのデプロイ設定を追加する
2. OGP / favicon / メタデータを整える
3. 必要なら実績ページや詳細ページを増やす
