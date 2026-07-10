# news-triage-app

ニュース記事をスマホで1件ずつ評価（採用/候補/不採用）するための汎用静的アプリ。

- GitHub リポジトリの `data/<profile>/news_*.json` を Contents API で読み、
  評価結果を `reviews/<profile>/reviews.json` に書き戻す
- 認証は fine-grained PAT（ブラウザの localStorage にのみ保存）
- サーバー・ビルド不要の単一 HTML。GitHub Pages で配信
- `#demo=1` を URL に付けるとダミー記事で動作確認できる

対象リポジトリ等は初回に設定画面で入力する（URL ハッシュ
`#owner=..&repo=..&profile=..` で事前充填可）。このリポジトリ自体には
データ・認証情報は含まれない。
