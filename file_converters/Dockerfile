FROM python:3.9

ENV APP_PATH=/code \
    PYTHONPATH=.
#　開発物のソースコードはcodeデイレクトリ下に配置する

WORKDIR $APP_PATH

RUN apt-get update && \
    apt-get upgrade -y && \
    pip install poetry
# コンテナのセットアップ

COPY . .

RUN poetry install
#　必要なパッケージ等をインストールする

EXPOSE 8000