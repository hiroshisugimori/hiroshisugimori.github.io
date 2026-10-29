# CUIL help maintenance

日本語: `get-started.html`, `features.html` / English: `../en/cuil/`（サイトルート基準では `en/cuil/`）。共通デザインはサイト直下の `style.css` と `cuil/help.css` を使用します。

2026-10-30、CUIL versionCode 75 / versionName 0.1.64 の作業ツリーを確認して作成。公開用のヘルプ原稿です。現在の実装に変更が入った場合は、日英両方の本文と確認日を更新してください。

## 照合した実装

アプリ側の `app/src/main/java/jp/hamsoft/cuil/terminal/`:

- `TerminalApps`, `TerminalActionHandler`, `TerminalCommandRegisterDialog`, `TerminalCommandGroups`: 候補検索、Enter、URI、コマンド登録とグループ。
- `TerminalBuiltinCommands`, `TerminalGestureShape`, `TerminalGestureRecognizer`, `TerminalGestureSettingsDialog`: 全ビルトインコマンド、登録可能なジェスチャー、判定と描き方。
- `TerminalHomeView`, `TerminalFrequentApps`: ホーム、添付、ボタン配置、よく使うアプリとジェスチャーの優先順位。
- `TerminalSearchShareTargets`, `TerminalSearchShareTargetsActivity`, `TerminalSearchHistoryActivity`, `TerminalPreferences`: 共有先、検索履歴と設定。
- `TerminalMemos`, `TerminalDraftActivity`, `TerminalFavoritesActivity`, `TerminalBoxActivity`: 定型文、下書き、お気に入り、Box。
- `TerminalHeaderSettings`, `TerminalHeaderSettingsActivity`, `TerminalStatusHeaderView`, `TerminalWallpaperActivity`, `TerminalTheme`: ヘッダー、壁紙、テーマ。
- `TerminalQrMakeDialog`, `TerminalCalculatorView`, `TerminalScreenshotDeletionPolicy`, `TerminalScreenshotDeletionRunner`: QR、計算、スクリーンショット削除。
- `TerminalAccessibilityService` と Manifest・サービスXML: システム操作と読み取り能力の制限。
- `CuilBackupSerializer`, `CuilBackupManager`: バックアップ対象の明示的な許可リスト。設定全体が対象とは記載しないでください。

`implementation-coverage.json` に32コマンド、22ジェスチャー、26章と5つの入門手順の対応一覧を保存しています。追加・削除時は実装と両言語の一覧を再照合してください。

## 公開前の確認

- 入門の5操作を実機で確認し、端末やOSに依存する画面名を確認する。
- スマートフォンとPCの表示、言語切替、目次リンクを確認する。
- 今回の図は操作の模式図で、実機スクリーンショットではありません。
- 公開URLは `/cuil/` と `/en/cuil/` を想定。公開後、必要に応じてアプリ設定にリンクを追加する。
- アプリのバージョン・更新履歴は、このヘルプ公開に伴って変更しません。
