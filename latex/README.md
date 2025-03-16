# LaTeX with Docker

このプロジェクトは、Dockerを使用してLaTeX文書をコンパイルするための環境を提供します。

## プロジェクト構成

```
.devcontainer/
    devcontainer.json
    Dockerfile

sample.tex
```

## 必要条件

- Docker
- Visual Studio Code (推奨)
- LaTeX Workshop 拡張機能 (VS Code)

## セットアップ

1. プロジェクトをクローンしてきます

2. VS CodeのRemote - Containers拡張機能を使用して、`Reopen in Container`を選択します。

3. Buildが完了すると、LaTex環境が開きます

## 使用方法

1. `sample.tex`ファイルを編集します。

2. ファイルを保存すると、自動的にコンパイルが開始されます。

3. コンパイルされたPDFは、`out`ディレクトリに生成されます。

## ファイルの説明

- `sample.tex`: LaTeXソースファイル。
- `.devcontainer/Dockerfile`: Dockerイメージの設定ファイル。
- `.devcontainer/devcontainer.json`: VS CodeのDev Container設定ファイル。

## Dockerイメージの詳細

このプロジェクトでは、`danteev/texlive:latest`イメージをベースにしています。日本語フォントと必要なLaTeXパッケージをインストールしています。
