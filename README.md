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
- **現時点の文面は仮コンテンツです**
- 参考元として指定された Notion ページは、この実装時点ではアクセス制限のため本文確認ができていません
- そのため、現在は「前向きでやわらかい」トーンの暫定テキストを入れています
- Notion 原文が確認できしだい、このファイルの内容を差し替える想定です

## 開発コマンド
```bash
pnpm install
pnpm dev
pnpm build
pnpm preview
```

## 次の作業候補
1. Notion 原文を反映して文面を確定する
2. Cloudflare 向けのデプロイ設定を追加する
3. OGP / favicon / メタデータを整える
