# FaceSeal - 顔モザイク

ブラウザで動作する顔自動検出・モザイク処理ツールです。サーバーへの画像送信は一切行わず、すべての処理がデバイス上で完結します。

**[→ 今すぐ使う](https://nyanko3141592.github.io/FaceSeal/)**

## 機能

- **自動顔検出** — face-api.js (SSD MobileNet V1) による高精度な顔認識
- **インタラクティブなモザイク操作** — 顔をタップして個別にモザイクのオン/オフを切り替え
- **ドラッグ&ドロップ対応** — ファイル選択またはドロップで画像をアップロード
- **PNG形式でダウンロード** — 処理済み画像を保存
- **完全ローカル処理** — 画像はサーバーに送信されない、プライバシー安全

## 使い方

1. 画像をアップロード（タップまたはドラッグ&ドロップ）
2. 顔が自動検出されモザイクが適用される
3. 顔をタップして個別にモザイクを切り替え
4. ダウンロードボタンで画像を保存

## 技術スタック

| 項目 | 内容 |
|------|------|
| フロントエンド | HTML / CSS / Vanilla JavaScript |
| 顔検出モデル | [face-api.js](https://github.com/justadudewhohacks/face-api.js) v0.22.2 + vladmandic/face-api v1.7.14 |
| ホスティング | GitHub Pages |
| ビルドツール | なし（ビルド不要） |

## ローカルで動かす

```bash
git clone https://github.com/nyanko3141592/FaceSeal.git
cd FaceSeal
# 任意のHTTPサーバーで index.html を配信（file:// では動作しない）
npx serve .
```

> [!NOTE]
> face-api.js のモデルはCDNから取得されるため、ネットワーク接続が必要です。

## ライセンス

MIT
