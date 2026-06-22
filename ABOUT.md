# FRACTAL WORKOUT Meeting Archive

## 一言で言うと

FRACTAL WORKOUT の打ち合わせ議事録と図解画像を、日付別に見返せる共有用Webアーカイブです。生成・編集はCodex側で行い、このサイトは閲覧専用として使います。

## 何ができるのか

- 議事録を日付ごとに一覧表示
- 要約、議題、決定事項、アクション、課題、次回までの対応を閲覧
- image-gen2で作成した図解PNGを議事録に紐づけて表示
- 文字起こし全文がある場合は詳細内で閲覧
- GitHub Pagesで共有用サイトとして公開
- FRACTAL WORKOUTの正式ロゴと黒・グレー・白基調のトンマナで表示

## 構成

- `server/index.js` — ローカル確認用の読み取り専用Expressサーバー
- `public/index.html` — アプリ画面
- `public/styles.css` — 画面デザイン
- `public/app.js` — 日付別表示と詳細表示
- `public/records.json` — 公開する議事録一覧
- `public/records/` — image-gen2で作成した図解PNGや文字起こしTXTの保存先
- `public/brand/fractal-workout-logo-gray.png` — FRACTAL WORKOUTの正式ロゴ。このサイトではこのロゴ以外を使用しない
- `.github/workflows/pages.yml` — GitHub Pages公開用ワークフロー
- `DIAGRAM_POLICY.md` — 図解は必ずimage-gen2で作成するための運用ルール

## 使い方

```bash
npm install
npm run dev
```

起動後、ブラウザで以下を開きます。

```text
http://localhost:3000
```

## 状態

- ルートプロジェクト — 開発中
- `public/` — 稼働中。日付別アーカイブ、詳細表示、図解画像表示を実装済み
- `public/records.json` — 稼働中。AIMTG、06/08定例会議、06/22会議の議事録を登録済み
- `public/records/2026-05-25-ai-mtg/` — 稼働中。image-gen2生成のAIMTG図解を同梱済み
- `public/records/2026-06-08-pr-seminar-planning/` — 稼働中。06/08定例会議のimage-gen2図解を同梱済み
- `public/records/2026-06-22-exhibition-seminar-meta-ads/` — 稼働中。06/22会議のimage-gen2図解を同梱済み
- `server/` — 稼働中。ローカル確認用サーバーとして実装済み
- GitHub Pages公開 — 稼働中
