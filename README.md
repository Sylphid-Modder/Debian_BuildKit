# Debian BuildKit
Debian live-buildの実行をmakeにより自動化するMakefile。
Debian 12 Bookwormのビルドに対応済み。

## 使用要件
- Debian 12 Bookworm以降
- live-build パッケージ
- make(build-essential)
- p7zip

**Ubuntuでは正常動作しません。**これはDebootstrapなどのツールの仕様が一部違うためです。

## 使用方法
初期設定: make setup DISTRO_NAME=(ディストリビューション名) VERSION=(バージョン)

設定のインポート: make import-config
※setup実行済み・archived_config.zipが必須です。

設定のエクスポート: make export-config

エクスポートされた設定の削除: make delete-config
※archived_config.zipが必須です。export-config実行前の実行を推奨します。

ISOの生成: sudo make build

リセット: sudo make clean

## 設定ファイルの書き換え方
準備中
