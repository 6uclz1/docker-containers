# Pythonの公式イメージをベースにする
FROM python:3.9-slim

# 作業ディレクトリを設定
WORKDIR /workspace

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    build-essential \
    libssl-dev \
    libffi-dev \
    python3-dev

# 仮想環境用のvenvを作成する
RUN python3 -m venv /workspace/.venv

# venvを使うように環境変数を設定
ENV VIRTUAL_ENV=/workspace/.venv
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# 必要に応じて依存パッケージをインストール
RUN pip install --upgrade pip
