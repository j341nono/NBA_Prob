# backend/Dockerfile
FROM python:3.12-slim

# 必要なツールをインストール (curlはuvのインストールに必要)
RUN apt-get update && apt-get install -y curl git && rm -rf /var/lib/apt/lists/*

# uv のインストール
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/uv

# 作業ディレクトリ
WORKDIR /app

# 環境変数の設定 (uvが作成する仮想環境を有効化)
ENV VIRTUAL_ENV=/app/.venv
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# コンテナが落ちないように待機させる（開発中はここに入ってコマンドを打つため）
CMD ["sleep", "infinity"]
