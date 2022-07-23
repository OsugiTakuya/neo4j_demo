# 起動方法
1. dockerイメージを構築する
```
docker-compose build
```

2. dockerコンテナを起動する
```
docker-compose up
```
(バックグラウンドで起動する場合は下記コマンド)
```
docker-compose up -d  # 起動

docker-compose stop  # コンテナ停止
docker-compose down  # コンテナ停止、削除
```

# 使い方
+ Neo4j Browser
    + http://<IPアドレス>:57474
    + 最初のページで下記を入力してログイン
        + Connect URL: 「bolt://」「<IPアドレス>:57687」
        + Authentication type: 「Username / Password」
        + Username, Password: ともに「neo4j」
+ Jupyter Notebook
    + http://<IPアドレス>:58888
    + Pythonから下記コードでDBにアクセス可能
    ```demo.py:python
    from neo4j import GraphDatabase
    uri = 'bolt://neo4j:7687'
    user = 'neo4j'
    password = 'neo4j'
    driver = GraphDatabase.driver(uri, auth=(user, password))
    ```