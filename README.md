# youchann.github.io

個人開発アプリのサポートページとプライバシーポリシーを配信する GitHub Pages のリポジトリ。

App Store Connect は提出時にプライバシーポリシーURLとサポートURLを必須で要求するため、その実体をここに置いている。独自ドメインは取得しておらず、ホスティング費用は¥0。

## 構成

| パス | URL | 内容 |
|---|---|---|
| `index.html` | `/` | アプリ一覧 |
| `hiit-forge/index.html` | `/hiit-forge/` | HIIT Forge サポート（日本語）**← ASC のサポートURL** |
| `hiit-forge/en/index.html` | `/hiit-forge/en/` | 同上（英語） |
| `hiit-forge/privacy/index.html` | `/hiit-forge/privacy/` | HIIT Forge プライバシーポリシー（日本語）**← ASC のプライバシーポリシーURL** |
| `hiit-forge/privacy/en/index.html` | `/hiit-forge/privacy/en/` | 同上（英語） |

## 方針

- 素の静的HTML。ビルド不要、依存なし（`.nojekyll` で Jekyll も通さない）
- 外部リソースを一切読み込まない。アクセス解析・フォント・CDN・JavaScript なし
  （「何も収集しない」と書いたページがトラッカーを積んでいたら本末転倒なので）
- 日本語と英語で**同一の事実**を書く。プライバシーポリシーで両言語の内容がずれるのは事故
- ポリシーの記述は実装より先に決まっている制約でもある。アプリ側の挙動を変えるときは、
  このページと矛盾しないか先に確認する（特に診断ログに含める項目）
