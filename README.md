# Monthly — Subscription Ledger

サブスクの月額と次の支払日を、ひと目で確認するための小さなアプリです（リポジトリ名は tsukizuki）。
公開先: https://sho3690.github.io/tsukizuki/

- 登録内容は端末のブラウザ（localStorage）にだけ保存され、外部には送信されません
- 支払日を過ぎると、次の支払日に自動で進みます
- 右上の歯車（Settings）の「Backup」から、JSONとして持ち出し・復元できます
- iPhoneでは「ホーム画面に追加」でアプリのように使えます（オフライン対応）
- ボタンや見出しは英語、説明文やお知らせは日本語で表示します

## 構成
- `index.html` … 画面と動作のすべて（依存ライブラリなし。フォントだけ Google Fonts の Inter / Space Grotesk を読み込み、オフライン時はシステムフォントで表示）
- `sw.js` … オフライン用のキャッシュ
- `manifest.webmanifest` / `icons/` … ホーム画面追加用（`icon.svg` が角丸、`icon-square.svg` が全面塗り。PNG はこの2つから書き出し）
