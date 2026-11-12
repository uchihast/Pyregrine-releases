# Pyregrine — Windows配布

高速AFMコントローラー **Pyregrine** のインストーラーと自動更新ファイルを配布するリポジトリです。開発コードは別の非公開リポジトリで管理しています。

[最新版のダウンロード](https://github.com/uchihast/Pyregrine-releases/releases/latest)

## インストール

1. Releasesから `Pyregrine-Setup-1.0.0-windows-x64.exe` をダウンロードします。
2. Pyregrineが動作中なら、測定を終えて安全に終了します。
3. インストーラーを実行します。Python・Gitの導入、GitHubアカウント、トークンの設定は不要です。

Windows x64向けです。通常のショートカットは模擬ボードで起動します。実機用はスタートメニューの **Pyregrine (Interface boards)** です。InterfaceボードのドライバーとPicoScope SDKは、必要なPCへ別途導入してください。

実機を初めて動かすときは、高圧アンプを切った状態で接続と装置設定を確認してください。配布物には他のPCの装置設定や測定データを含めていません。

## 自動更新

起動時にこのリポジトリの正式Releaseを確認します。新しい版があれば更新用ZIPを自動取得し、SHA-256と実機を使わない起動診断を確認してから新版を起動します。測定中に更新・再起動することはありません。

装置・操作者の設定と既定の保存先は `%LOCALAPPDATA%\Pyregrine`、アプリ本体は `%LOCALAPPDATA%\Programs\Pyregrine` です。更新・再インストール・アンインストールでは状態フォルダーを削除しません。

以前の非公開配布版1.0.0をインストールした場合は、この公開版1.0.0を一度インストールしてください。以降の正式版はトークンなしで更新できます。

## 配布ファイル

- `Pyregrine-Setup-<version>-windows-x64.exe`：初回導入用インストーラー
- `Pyregrine-<version>-windows-x64.zip`：自動更新用一式
- `pyregrine-release.json`：更新ファイルの版・サイズ・SHA-256
- `SHA256SUMS.txt`：配布資材のチェックサム

初版は **1.0.0**。Windowsコード署名は未設定です。模擬起動と更新経路を検証していますが、各PCでの実機接続は個別の確認が必要です。
