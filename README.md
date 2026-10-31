# ジバギョーネット案内サイト

- 公開URL: https://jibagyo.site/
- 本番アプリ: https://jibagyo-net.pascaline-system.workers.dev/
- CloudflareアカウントID: `b007d63f9496af1458c8a72931fb4034`
- 本番Worker: `jibagyo-homepage`
- 管理画面: https://dash.cloudflare.com/b007d63f9496af1458c8a72931fb4034/workers/services/view/jibagyo-homepage/production

このサイトはCloudflare Workersの静的アセットとして公開されています。Cloudflare Pagesのプロジェクトではありません。旧個人GoogleアカウントでCloudflareへログインして管理します。

## 本番更新

管理画面の「New deployment」で、`index.html`、`robots.txt`、`sitemap.xml`、`assets/`をアップロードして公開します。フォルダ構成を維持し、`wrangler.jsonc`、README、Git管理用ファイルはアップロード対象に含めません。

CLIで更新する場合は、このアカウントのWorkers編集権限で認証し、`npx wrangler deploy`を実行します。`wrangler.jsonc`には本番アカウントとカスタムドメインを明示しています。

既存のGitHub Actionsは誤ってPagesへ公開しようとしており、登録済みAPIトークンもPages向けです。2026年10月31日の更新は、正しいWorkerの管理画面から反映しました。GitHub Actionsの自動公開を復旧する際は、Workers用の認証権限とデプロイコマンドを揃える必要があります。

## 2026年10月31日の確認

ヘッダー・メイン・ページ下部の3か所を「アプリを使用」に統一し、本番アプリへのリンクに変更しました。本番HTMLが変更後の`index.html`と一致し、旧プレエントリー導線が残っていないことを確認しました。

画面下端には、提供された「支援一覧と掲載順.xlsx」の支援者一覧A2:C26をもとに、25件の掲載名・スポンサー区分を行順どおり表示するスポンサー帯を追加しました。240秒の連続スクロール、停止・再開、ホバー・キーボードフォーカスでの停止、動きを抑える端末設定に対応しています。支援金額・支援日・リターン説明はサイトへ含めません。
