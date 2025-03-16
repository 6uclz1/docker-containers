# Python DevContainer

このリポジトリは、Python開発のためのDevContainer設定を含んでいます。DevContainerを使用することで、開発環境を簡単にセットアップし、依存関係を管理することができます。

想定としては、簡単なスクリプトを実行するための使い捨て環境です。

## ファイル構成

- `requirements.txt`: Pythonの依存パッケージをリストしたファイル。
- `sample.py`: サンプルのPythonスクリプト。
- `.devcontainer/`: DevContainerの設定ファイルを含むディレクトリ。
  - `devcontainer.json`: DevContainerの設定ファイル。
  - `Dockerfile`: DevContainer用のDockerイメージを定義するファイル。

## 使用方法

### 前提条件

- Dockerがインストールされていること。
- Visual Studio CodeとRemote - Containers拡張機能がインストールされていること。

### 手順

1. このリポジトリをクローンします。

2. Visual Studio Codeでリポジトリを開きます。

3. コマンドパレット（`Ctrl+Shift+P`）を開き、「Remote-Containers: Reopen in Container」を選択します。

4. DevContainerが起動し、必要な依存パッケージがインストールされます。

### Pythonのパス

Pythonのパスは`venv`を使った仮想環境上に設定されています

VSCodeでpipでインストールしたパッケージが使えない場合は
`Python: Select Interpreter`で`/workspace/.venv/bin/python`を選択してください。

### コマンド

使用出来るPythonコマンドはpython3など付いてないものです

例：

```sh
python {実行したいコード}.py
```

```sh
pip {インストールしたいパッケージ}
```
