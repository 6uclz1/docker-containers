# Dockerコンテナによる開発環境

このリポジトリには、さまざまな開発環境用のDockerコンテナ設定が含まれています。これらの設定を使用することで、隔離された再現可能な開発環境を迅速にセットアップできます。

## プロジェクト構成

```
<environment>/
  .devcontainer/
    devcontainer.json
    Dockerfile
  sample.<ext>
```

## 必要条件

- Docker
- Visual Studio Code (推奨)
- Remote - Containers拡張機能 (VS Code)

## 環境のセットアップ

### ファイル

- `requirements.txt`: 依存パッケージをリストしたファイル。
- `sample.<ext>`: サンプルのスクリプトまたはドキュメント。
- `.devcontainer/`: DevContainer設定ファイルを含むディレクトリ。

### セットアップ手順

1. このリポジトリをクローンします。
2. Visual Studio Codeで起動したい環境のディレクトリを開きます。
3. コマンドパレット（`Ctrl+Shift+P`）を開き、「Remote-Containers: Reopen in Container」を選択します。
4. DevContainerが起動し、必要な依存パッケージがインストールされます。

### 使用方法

- 環境に応じたコマンドを使用してスクリプトやドキュメントを実行または編集します。
- `pip`やその他のパッケージマネージャを使用して追加のパッケージをインストールします。

## 追加情報

- 各環境は、指定された仮想環境またはコンテナ内で動作します。
- Dockerイメージや設定ファイルは、必要に応じてカスタマイズできます。
