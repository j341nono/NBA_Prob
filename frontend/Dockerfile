# frontend/Dockerfile
FROM node:22-slim

# gitなどのツールを入れておく（開発時に便利）
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# こちらも開発中はサーバを手動起動、または常駐させるため待機
CMD ["sleep", "infinity"]
