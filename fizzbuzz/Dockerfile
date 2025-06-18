# Python の公式イメージを使用
FROM python:3.9-slim

# 作業ディレクトリを作成
WORKDIR /app

# 必要なファイルをコンテナにコピー
COPY test1.py /app/

# コンテナ起動時に実行するコマンドを指定
ENTRYPOINT ["python", "test1.py"]
