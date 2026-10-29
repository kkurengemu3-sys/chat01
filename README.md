# Quvo Chat — GitHub用リポジトリ

©QuvoCorporation

Google Apps Script（GAS）とGoogleスプレッドシートを使用するチャットアプリの**テスト版**です。

## ファイル構成

- `index.html` — GitHub Pagesで表示できる入口ページ（チャット本体ではありません）
- `gas/Code.gs` — GASサーバーコード
- `gas/Index.html` — GAS上で動作するチャット画面
- `gas/appsscript.json` — GASプロジェクト設定

## 公開方法（スマホからでも可）

1. GitHubで新規リポジトリを作成し、このZIPの**中身**をアップロードします。
2. Google Apps Scriptで新しいプロジェクトを作ります。
3. `gas/Code.gs` の内容を `Code.gs` に貼り付けます。
4. GASでHTMLファイル `Index` を作り、`gas/Index.html` の内容を貼り付けます。
5. GASで `setup()` を一度実行し、必要な権限を許可します。
6. **デプロイ → 新しいデプロイ → ウェブアプリ** から、まず「自分のみ」でテストします。
7. GitHub Pagesを使う場合、ルートの `index.html` の `GAS_WEB_APP_URL` にGASのウェブアプリURLを設定します。
8. GitHubの **Settings → Pages → Deploy from a branch → main / (root)** で入口ページを公開できます。

## 重要

GitHub Pagesは静的サイト専用です。`Code.gs` や `google.script.run` をGitHub Pages上で直接実行することはできません。**GitHub Pagesだけではチャットは動きません。** この構成ではGitHub Pagesは入口、GASがチャット本体です。

このコードはテスト版です。画像・動画・ファイル送信、スタンプ、投票、管理画面、プッシュ通知などは含まれていません。一般公開前に認証・アクセス制御・レート制限・データ保護の確認が必要です。

**パスワード、APIキー、スプレッドシートの秘密情報、デプロイ用認証情報をGitHubにコミットしないでください。**
